# SmartBin 360 — Waste Collection Management

A beginner-friendly prototype for a Smart Waste Collection Management System.

## Project overview
SmartBin 360 lets a citizen submit a waste complaint and gives an admin-style dashboard to assign collection workers and update task status.

## Features
- Submit waste reports with name, location, issue type, and description
- Generate a unique complaint ID
- Track Pending, In Progress, Completed, and Not Completed statuses
- Clearly mark whether an assigned collection task was completed or not
- Dashboard counters include a separate Not Completed count
- Assign a collector to each report
- Filter reports by status
- Dashboard counters for total and status-wise reports
- Load sample data for a project demonstration
- Save demo data in browser localStorage

## Technologies
- HTML — page structure
- CSS — responsive styling
- JavaScript — form handling and dashboard logic
- localStorage — browser-local demo persistence

## How to run
1. Open the repository on GitHub and download the source, or clone it:
   `git clone https://github.com/sheriabhinav2008-svg/Waste-collection-management-.git`
2. Open the project folder.
3. Open `index.html` in Chrome, Edge, or Firefox.
4. Submit a complaint or click **Load sample reports**.
5. Assign a collector and use the status dropdown to choose **Completed** or **Not Completed** (or keep it Pending / In Progress).
6. Check the dashboard counters to see how many jobs are completed and not completed.

No package installation or build step is needed for this frontend demo.

## How it works
1. A citizen fills out the report form.
2. JavaScript creates a complaint ID and starts the report at Pending.
3. The report is saved in the browser's localStorage.
4. The dashboard displays the report and updates its counters.
5. A user can assign a collector and set the task to Completed or Not Completed. The dashboard updates the relevant counters immediately.

## System architecture
```text
Citizen / Admin / Collector
          |
          v
   HTML + CSS + JavaScript
          |
          v
  Browser localStorage
          |
          v
Complaint list and dashboard
```

## Important limitations
This is a frontend-only student prototype. Data is stored only in the current browser and is not shared between users or devices. It does not yet include secure login, a backend API, a central database, live GPS, route optimization, real notifications, or IoT sensors. Do not use it to store real personal information.

## Future improvements
- Node.js and Express backend
- MongoDB or Firebase shared database
- Role-based citizen, admin, and collector login
- Map integration and route optimization
- IoT bin-fill sensors and automatic alerts
- Image upload and verification workflow

## Project title
**SmartBin 360 — An Intelligent Waste Collection and Monitoring System**
