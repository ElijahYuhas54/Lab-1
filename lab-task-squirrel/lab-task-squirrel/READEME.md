# TaskSquirrel 🐿️  
_A Scavenger Hunt Chore App for Kids_

## 👤 Name: Elijah Yuhas  
## 🆔 Z#: Z23666230

---

## 📖 Project Description

**TaskSquirrel** is an interactive iOS app designed to help parents assign chores (or scavenger hunt tasks) to their children and verify completion with photo evidence. The app allows users to create and manage a list of tasks, attach photos as proof of completion, and display the location where each photo was taken on a map. 

By utilizing the device’s photo library and photo metadata, TaskSquirrel makes it fun and visual for kids to complete tasks—and lets parents easily track them using maps.

---

## ✅ Features

- 📋 View a list of scavenger hunt tasks.
- ➕ Create new tasks with title and description.
- 📸 Attach a photo from the photo library to mark a task as complete.
- 🌍 Extract and display the location of the attached photo using **MapKit**.
- 📌 Drop a **custom annotation** (thumbnail of photo) at the location on the map.
- 👀 View the full image in a dedicated photo viewer screen.
- 🧠 Real-time UI updates upon task completion.
- 🔐 Handles permission requests for accessing photos and location metadata.
- 🔁 Seamless navigation between views using segues and data passing.

---

## 🎥 Demo

> 📌 **GIF showing full functionality of the app will be added here later.**

---

## 📁 How to Run the Project

1. Clone or download this repository.
2. Open the `.xcodeproj` or `.xcworkspace` file using Xcode.
3. Run on a **physical device** for full photo metadata functionality (location).
4. Build & Run.

---

## 📦 Dependencies & Frameworks Used

- **UIKit**
- **MapKit**
- **PhotosUI**
- **CoreLocation**

---

## 📌 Notes

- Ensure your device or simulator has photos **with location metadata** for full functionality.
- Add photos to simulator using drag-and-drop into the Photos app.
- All tasks are stored in-memory and will reset on app relaunch (no persistence yet).

---

## 🔐 Permissions Required

- `NSPhotoLibraryUsageDescription` added to Info.plist:
  > “We need access to your photos in order to add a photo to complete a task.”

---

## 📎 Project Structure

- `Task.swift` – Data model for tasks.
- `TaskListViewController.swift` – Lists all tasks.
- `TaskComposeViewController.swift` – Add new task.
- `TaskDetailViewController.swift` – Task details, attach photo, show map.
- `PhotoViewController.swift` – Display full-screen photo.
- `TaskAnnotationView.swift` – Custom map annotation view.
- `Main.storyboard` – UI layout and view controllers.

---

## ✅ Rubric Checklist

| Criteria | Status |
|---------|--------|
| Name and Z# in README | ✅ |
| Detailed Description in README | ✅ |
| Feature List in README | ✅ |
| Embedded GIF | ⏳ (To be added) |
| Project Properly Uploaded in Repo | ✅ |

---
