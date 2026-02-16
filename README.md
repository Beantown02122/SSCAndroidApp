# Senior Connect & Safety+

![Platform](https://img.shields.io/badge/Platform-Android-green)
![Language](https://img.shields.io/badge/Language-Kotlin-purple)
![Architecture](https://img.shields.io/badge/Architecture-MVVM-blue)
![Database](https://img.shields.io/badge/Database-Room-orange)
![Min API](https://img.shields.io/badge/Min%20API-27-red)

Secure Android Safety & Communication Application

---

## Overview

Senior Connect & Safety+ is a structured Android application designed to support older adults with:

• Emergency readiness  
• Caregiver communication  
• Medication management  

The application prioritizes accessibility, reliability, and secure local data persistence.  
It is built using modern Android architecture principles and lifecycle-aware components.

---

## Key Features

### Emergency Access
- One-tap 911 calling
- Optional caregiver quick-call
- Minimal navigation depth for urgent use
- Clear, large-button interface

### Trusted Contacts
- Add, edit, delete contacts
- Live RecyclerView updates
- Confirmation dialogs for edits
- Structured local storage

### Caregiver Management
- Multiple caregiver profiles
- SMS and call preference options
- Immediate call access
- Persistent data storage

### Medication Reminders
- Create and manage reminders
- Title, time, and notes fields
- Immediate UI refresh
- Edit and delete functionality

---

## Technical Stack

- Kotlin
- MVVM Architecture
- ViewModel + LiveData
- Room Database
- RecyclerView
- Material Design Components
- Offline-first design

Minimum API: 27  
Recommended API: 30–34  

---

## Architecture Overview

The application follows clean architectural separation:

UI Layer  
↓  
ViewModel  
↓  
Repository  
↓  
Room Database  

This structure ensures:

- Clear separation of concerns  
- Lifecycle safety  
- State preservation  
- Improved testability  
- Reduced memory leaks  

---

## Application Screenshots

### App Icon

<p align="center">
  <img src="ssc_icon.png" width="160"/>
</p>

---

### Login Screen

<p align="center">
  <img src="sscloginsucces.png" width="260"/>
</p>

---

### Main Dashboard

<p align="center">
  <img src="sscmainscreen.png" width="260"/>
</p>

---

### Emergency Module

<p align="center">
  <img src="sscemergencyscrren.png" width="260"/>
</p>

---

### Caregiver Management

<p align="center">
  <img src="ssccaregiverscreen1.png" width="250"/>
  <img src="ssccaregiverscreensaved caregivers.png" width="250"/>
</p>

---

### Trusted Contacts

<p align="center">
  <img src="ssctrustedcontactscreen.png" width="250"/>
  <img src="ssctrustedcontact.png" width="250"/>
  <img src="ssctrustedcontactsavechangesconfirm.png" width="250"/>
</p>

---

### Medication Reminders

<p align="center">
  <img src="sscmedicationreminder.png" width="250"/>
  <img src="sscmedicationremindersaved.png" width="250"/>
  <img src="sscmedicationreminderwithlist.png" width="250"/>
</p>

---

## Security & Stability

- Input validation on all forms  
- Confirmation dialogs for destructive actions  
- Structured navigation arguments  
- Offline data persistence  
- Safe handling of configuration changes  
- Lifecycle-aware components  

---

## Demo Video

<p align="center">
  <a href="PASTE_YOUTUBE_LINK_HERE">
    <img src="sscmainscreen.png" width="300"/>
  </a>
</p>

Click the image above to watch the demo.


---

## Build Instructions

1. Open Android Studio  
2. Select “Open Existing Project”  
3. Choose project folder  
4. Allow Gradle sync  
5. Run on emulator/device API 27+  

No external third-party libraries required.

---

## Skills Demonstrated

- Android Application Development  
- Kotlin Programming  
- MVVM Architecture Implementation  
- Room Database Integration  
- RecyclerView Implementation  
- State Management  
- UI/UX Accessibility Design  
- Offline-first Application Design  
- Mobile App Testing  

---

## Project Impact

Senior Connect & Safety+ demonstrates the ability to design and implement a structured Android application using modern architecture patterns.

The project focuses on usability, reliability, and maintainable code structure suitable for real-world deployment scenarios.
