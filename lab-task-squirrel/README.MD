# 🐿️ Task Squirrels  

Task Squirrels is an iOS app that lets parents assign chores/tasks to their children. Each task can be completed by attaching a photo, and the app will display the location where the photo was taken on a map.  

---

## 📌 Features  

### Required Features  
- View a list of tasks to be completed.  
  - Each task has a `title`, `description`, `image` (optional), and a computed `isComplete` property.  
  - The list shows task titles, with a completion indicator on the left.  

- View task details:  
  - Shows the task’s title, description, and completion status.  
  - If no photo is attached: show an **Attach Photo** button.  
  - If photo is attached: hide the button and show a map view.  

- Attach a photo from the photo library:  
  - Uses **PHPickerViewController**.  
  - Requests photo library access (via `NSPhotoLibraryUsageDescription`).  
  - Loads the photo and its location metadata (latitude/longitude).  
  - Marks the task as complete and updates the UI in both the detail and list screens.  

- Display location of attached photo on a map:  
  - Zooms into the photo’s location using **MapKit**.  
  - Drops a pin annotation at the location.  
  - Replaces the default pin with a **custom annotation view** showing the chosen photo.  

- View attached photo in a new screen:  
  - A **"View Photo"** button appears once a task has an attached image.  
  - Tapping the button segues to a **PhotoViewController** that displays the selected photo.  

---

## 🛠️ Implementation Steps  

### Step 0: Setup Project  
- Download starter project (`lab_1.zip`).  
- Explore `TaskListViewController`, `TaskDetailViewController`, and `TaskComposeViewController`.  
- Tasks are initially mocked in `Task.swift`.  

### Step 1: Request Photo Library Access  
- Imported **PhotosUI**.  
- Added `PHPhotoLibrary.authorizationStatus` check and request.  
- Added `NSPhotoLibraryUsageDescription` key in `Info.plist`.  

### Step 2: Present Photo Picker  
- Implemented `presentImagePicker()` using **PHPickerConfiguration**.  
- Conformed to `PHPickerViewControllerDelegate`.  

### Step 3: Get Photo Location Metadata  
- Fetched **PHAsset** using asset identifier.  
- Extracted and printed latitude/longitude of photo.  

### Step 4: Load Selected Photo  
- Loaded the chosen photo as a **UIImage** using `NSItemProvider`.  
- Updated task model with image and location.  
- Updated UI (`updateUI`, `updateMapView`).  

### Step 5: Display Location on Map  
- Used **MKMapView** to zoom into photo location.  
- Configured region span for zoom level.  

### Step 6: Add Annotation  
- Dropped a pin (`MKPointAnnotation`) at the photo’s location.  

### Step 7: Custom Annotation View  
- Created custom `TaskAnnotationView` subclass of `MKAnnotationView`.  
- Registered it in `viewDidLoad()`.  
- Implemented `mapView(_:viewFor:)` to return custom annotation with attached photo.  

### Step 8: View Photo in New Screen  
- Added **"View Photo"** button in storyboard.  
- Created `PhotoViewController` with an `UIImageView`.  
- Passed the selected task’s image from `TaskDetailViewController` via segue.  

---

## 📸 Demo Flow  
1. Add a new task or use an existing one.  
2. Open the task → Tap **Attach Photo**.  
3. Select a photo (with location metadata).  
4. Task updates to completed → Map view displays with photo location and custom annotation.  
5. Tap **View Photo** to see full image.  

---

## 🧰 Tech Stack  
- **Swift**  
- **UIKit**  
- **PhotosUI**  
- **MapKit**  

---

## 🔐 Permissions  
Add the following key to `Info.plist`:  
```xml
<key>NSPhotoLibraryUsageDescription</key>
<string>We need access to your photos in order to add a photo to complete a task.</string>
```

---

## 🚀 Future Improvements  
- Support multiple photos per task.  
- Allow users to take a photo with the camera.  
- Store tasks persistently (e.g., Core Data or CloudKit).  
- Share completed tasks with others.  
