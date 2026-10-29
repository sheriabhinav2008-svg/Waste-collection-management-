# Waste Collection Management System

**Project name:** Waste Collection Management System  
**Demo name:** SmartBin 360

A beginner-friendly, frontend-only project with a **User Login page** (`login.html`), **User Portal** (`index.html`), and a separate **Administrator Portal** (`admin.html`). The user-facing pages contain no administrator dashboard or administrator login option. Citizens can report waste and water-related issues, receive a complaint ID, and track progress.

## Project Overview

The system provides a simple way to record a problem with a required before-collection photo, add after-collection photo evidence, and monitor whether the reported work is pending, in progress, completed, or not completed. It is designed as a student project and demonstration prototype.

## Features

- User-only Login page (`login.html`) with username + 10-digit phone number fields; it routes only to the User Portal
- Separate User Portal (`index.html`) for reporting and tracking complaints
- Separate Administrator Portal (`admin.html`) for complaint review and management
- Separate page layouts: the User Portal focuses on complaint submission and tracking; the Administrator Portal focuses on review, assignment, photo verification, and status management
- The User Portal has no administrator dashboard or administrator portal link; administrators use the separate `admin.html` page
- Submit a report with the reporter's name, location, issue type, and description
- Report different issues, including overflowing bins, water leakage or stagnant water, illegal dumping, missed collection, and waste segregation
- Require a **before-collection photo** when submitting every complaint
- Require an **after-collection photo** from the officer/collector before allowing the status to become **Completed**
- Display before-and-after photos side by side for visual comparison
- Validate both images and limit each photo to 1 MB
- Generate a unique complaint ID
- Assign a collection worker to a report
- Track **Pending**, **In Progress**, **Completed**, and **Not Completed** statuses
- Search for a complaint using its unique complaint ID
- View a complaint timeline showing submission, officer-seen time, collector assignment changes, and status changes
- Record when an administrator marks a complaint as seen by an officer on the separate administrator page
- Show the current status, assigned collector, officer-viewed state, and update history in the citizen tracking panel
- Save demonstration reports in the browser's local storage

- Select an interface language: English, Telugu, Hindi, Tamil, Kannada, Malayalam, Marathi, Bengali, Gujarati, Punjabi, Odia, or Urdu
- Regional-script font support using Noto fonts when an internet connection is available
- Voice input for the name, location, and issue description using the browser's speech-recognition support
- Read the page aloud using browser text-to-speech in the selected language when a matching device voice is available


## Technologies Used

- **HTML5** — page structure and report form
- **CSS3** — styling and responsive layout
- **JavaScript** — form validation, photo preview, complaint submission, and complaint ID tracking
- **Browser localStorage** — local demo data persistence and saved language preference
- **Web Speech API** — browser-supported speech recognition and text-to-speech

No framework, package installation, or build step is required for this frontend demo.

## Getting Started

### Option 1: Run locally

1. Clone this repository:

   ```bash
   git clone https://github.com/sheriabhinav2008-svg/Waste-collection-management-.git
   ```

2. Open the downloaded project folder.
3. Open `login.html` in a modern browser such as Chrome, Edge, or Firefox. Enter a username and 10-digit phone number to continue to the User Portal.
4. Fill in the report form and attach the required before-collection photo.
5. Submit the complaint. The page displays the generated complaint ID, fills it into the tracker, and shows the current status.
6. The separate Administrator Portal is available at `admin.html`; it is not linked from the user-facing pages.

### Option 2: Download from GitHub

1. Open this repository on GitHub.
2. Select **Code → Download ZIP**.
3. Extract the ZIP file.
4. Start at `login.html`; it routes only to the User Portal (`index.html`). The Administrator Portal is a separate page at `admin.html`.

## How It Works

1. A citizen enters their name, the issue location, issue type, and description.
2. The citizen must upload a before-collection photo. The selected image is previewed before submission.
3. JavaScript creates a unique complaint ID and initially marks the report as **Pending**.
4. The report and required before-collection photo are saved in the browser's localStorage.
5. After submission, the user portal displays the generated complaint ID and opens the complaint tracking timeline.
6. Administrators use the separate `admin.html` page to assign a collector, mark reports as seen, upload after-collection photos, and update statuses.
7. Use the language selector and microphone buttons for supported language and voice features.
8. A citizen can enter the complaint ID in **Track your complaint** to see the latest status and recorded timeline.

## Basic System Architecture

```text
User Login (login.html)
        |
        v
User Portal (index.html)
  |                 |
  v                 v
Report issue     Track by Complaint ID
+ before photo   + status timeline
  |
  v
Browser localStorage (demo only)

Administrator Portal (admin.html)
separate page; not linked from user pages
  |
  v
Review reports, assign collectors,
upload after photos, update statuses
```

## Important Limitations

This is a **frontend-only student prototype**.

- Data is stored in the browser where the project is being used; it is not automatically shared with other users or devices. The citizen tracker only finds reports saved in that same browser profile.
- The User Login is only a frontend demo: username and phone number are not verified. The administrator page is not linked from user pages, but anyone who knows its URL can still open it. Add backend authentication and server-side role checks before using this for real users.
- The **Mark as seen** control is a demo action on the separate administrator page; the prototype does not authenticate officers or independently verify that an officer opened a report.
- Timeline timestamps are generated by the browser and are suitable for demonstration, not as an authoritative audit log.
- Before and after photos are stored as data in localStorage, so storage space is limited. Each image is limited to 1 MB; use small demo images.
- There is no backend API, shared database, secure login, live GPS tracking, route optimization, real notification service, or IoT sensor integration.
- Browser speech recognition is not available in every browser/device and may require microphone permission or an internet connection. Text-to-speech voices vary by operating system. Regional fonts may need internet access to load from Google Fonts. Some interface phrases have translated labels while remaining descriptive/dynamic text can still appear in English; this is a student-demo localization layer, not certified full translation.
- Do not use this prototype to store sensitive personal information or for production operations.

## Future Enhancements

- Add a backend using Node.js and Express
- Store reports in a shared database such as MongoDB or Firebase
- Add secure role-based citizen, admin, and collector accounts so citizens can track reports from different devices
- Store a secure, server-side audit history for submission, officer viewing, assignment, and every status change
- Upload photos to dedicated image storage
- Add map-based issue locations and optimized collection routes
- Add email or SMS notifications when report status changes
- Integrate IoT bin-fill sensors and automated alerts

## Repository

[Waste Collection Management System on GitHub](https://github.com/sheriabhinav2008-svg/Waste-collection-management-)

## Project Title

**Waste Collection Management System — SmartBin 360**
