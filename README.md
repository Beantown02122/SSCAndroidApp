# Senior Connect & Safety+
Android Safety & Communication Application (Offline-First)

## Project Overview
Senior Connect & Safety+ is a mobile application designed to support older adults with emergency readiness, caregiver communication, and medication reminders.

The app focuses on accessibility, simple navigation, and reliable local data storage. It uses a structured Android architecture with lifecycle-aware components.

---

## Core Features

### Emergency Access
- One-tap 911 access
- Optional caregiver call
- Minimal navigation depth for urgent use
- Back navigation for controlled flow

### Trusted Contacts Management
- Add, edit, delete contacts
- Fields: name, phone number, relationship
- Live-updating list (RecyclerView)
- Confirmation dialogs to prevent accidental changes

### Caregiver Management
- Multiple caregiver profiles
- SMS and call preference options
- Quick-call functionality
- List management with delete controls

### Medication Reminders
- Create and manage reminder entries
- Persistent local storage
- Immediate UI updates
- Edit and delete functionality

---

## Technical Architecture
- Language: Kotlin
- Architecture Pattern: MVVM
- State Management: ViewModel + LiveData
- Local Persistence: Room Database
- UI Framework: Material Design Components
- Minimum API Level: 27
- Recommended API: 30–34

Separation of concerns:
- UI layer renders screens and handles interaction
- ViewModel layer holds state and business logic
- Data layer persists information using Room (Entity + DAO + Database)

---

## Architecture Diagram

### High-Level MVVM Flow (ASCII)

User
  |
  v
UI (Activity/Fragment + XML)
  |
  v
ViewModel (LiveData)
  |
  v
Repository (optional)
  |
  v
Room (DAO -> SQLite)
  ^
  |
LiveData updates UI

---

## Data Flow
User Action
→ UI Event
→ ViewModel Processing
→ Room Database Operation
→ LiveData Update
→ UI Refresh

---

## Database Schema

This project uses Room to store data locally. Typical tables include:

Contacts
- id (PK)
- name
- phone
- relationship

Caregivers
- id (PK)
- name
- phone
- relationship
- smsEnabled (boolean)
- callEnabled (boolean)

MedicationReminders
- id (PK)
- title
- time
- notes

If your actual Entity field names differ, keep the concept but update the column names to match your code.

---

## Security and Stability Practices
- Input validation on user forms
- Confirmation dialogs for destructive actions
- Offline-first design with local storage
- Lifecycle-aware state to reduce crashes during configuration changes

If you want to claim stronger security (encryption, auth hardening), you need to implement and document it.

---

## Application Structure
The project contains:
- Kotlin source files
- Room entities and DAO interfaces
- ViewModels
- RecyclerView adapters
- XML layout resources
- Gradle build configuration

No third-party libraries are required beyond standard Android components.

---

## User Flow
From the home screen, users can access:
- Emergency Access
- Trusted Contacts
- Caregiver Management
- Medication Reminders

Each module is reachable through clear, controlled navigation.

---

## Application Screenshots

Place these image files in the repository root (same folder as this README),
or update the paths below to match your project.

### App Icon
![App Icon](ssc_icon.png)

### Login Screen
![Login Screen](sscloginsucces.png)

### Main Dashboard
![Main Screen](sscmainscreen.png)

### Emergency Screen
![Emergency Screen](sscemergencyscrren.png)

### Caregiver Management

Add Caregiver
![Caregiver Entry](ssccaregiverscreen1.png)

Saved Caregivers List
![Saved Caregivers](ssccaregiverscreensaved caregivers.png)

### Trusted Contacts

Add Contact
![Trusted Contact Screen](ssctrustedcontactscreen.png)

Edit Confirmation Dialog
![Save Changes Dialog](ssctrustedcontactsavechangesconfirm.png)

### Medication Reminders

Create Reminder
![Medication Entry](sscmedicationreminder.png)

Reminder Saved
![Medication Saved](sscmedicationremindersaved.png)

Reminder List View
![Medication List](sscmedicationreminderwithlist.png)

---

## Build and Run

1. Open Android Studio
2. Select "Open Existing Project"
3. Choose the project folder (SeniorConnectSafetyPlus)
4. Allow Gradle to sync
5. Select an emulator or device running API 27+
6. Press Run

---

## Skills Demonstrated
- Android application development
- Kotlin programming
- MVVM architecture implementation
- Room database design
- Accessibility-focused UI design
- Local data persistence
- State management with LiveData

---

## Roadmap (Future Improvements)
- Add scheduled notification alarms for medication reminders (AlarmManager or WorkManager)
- Add emergency contact customization (choose primary caregiver)
- Add stronger data protection (encrypted storage for sensitive fields)
- Improve form validation (phone formatting, required fields, error messages)
- Add basic UI testing (Espresso) and ViewModel unit tests
- Add accessibility checks (TalkBack labels, larger text scaling)
