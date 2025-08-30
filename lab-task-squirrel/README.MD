# 🐿️ Task Squirrels

**Name:** Elijah Yuhas  
**Z Number:** Z23666230  
**University:** Florida Atlantic University (FAU)
**GitHub:** https://github.com/ElijahYuhas54/Lab-1/tree/main/lab-task-squirrel
---

## 📱 Project Description

**Task Squirrels** is an iOS app designed to help parents assign and track chores for their children. Each task can be completed by attaching a photo as proof, and the app uses location metadata from the photo to display where it was taken on a map. This lab project demonstrates the use of photo selection, metadata extraction, and map annotation in a Swift UIKit application.

---

## ✨ Features Added

- **Photo Attachment via PHPickerViewController**  
  Users can select a photo from their library to attach to a task. The app requests photo library access and loads the selected image.

- **Location Metadata Extraction**  
  The app extracts the location (latitude and longitude) from the selected photo using `PHAsset`.

- **MapKit Integration**  
  Once a photo is attached, the app displays a map centered on the photo’s location. A custom annotation pin shows the image at the location.

- **Custom Annotation View**  
  Replaces the default map pin with a custom view that displays the attached photo.

- **View Photo Screen**  
  A "View Photo" button appears when a task is completed. Tapping it navigates to a new screen that displays the full image.

- **Conditional UI Updates**  
  The "Attach Photo" button is hidden once a photo is attached, and the "View Photo" button is shown only when the task is marked complete.

---

## 📸 Demo

Include a GIF below that demonstrates the full app flow:
- Selecting a photo
- Viewing the map with annotation
- Navigating to the photo viewer screen

!Task Squirrels Demo
