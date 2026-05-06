# GPU Resource Management System

> A web application for managing GPU computing resource requests at KLE Technological University's Central Computing Facility (CCF).

---

## Overview

The GPU Resource Management System streamlines the process of allocating GPU workstations and DGX servers to students and faculty. Instead of manual coordination, users submit verified requests online, and administrators review, allocate, and track resources through a dedicated dashboard — all in real time.

The system is actively used within the university network.

> **Access is restricted to the university intranet.** Live access is not publicly available.  

---

## Features

### User-Facing
- Email OTP verification (only `@kletech.ac.in` addresses allowed)
- Resource request form (Workstation / DGX Server)
- Real-time slot availability check before submission
- Request queue cap — users are not allowed to request when queue exceeds 10 pending requests
- Automated email confirmation on request submission

### Admin Dashboard
- Live pending requests table with auto-refresh
- Accept requests — single slot or multiple slots from the same resource
- Reject requests with optional reason
- Resource overview with per-slot utilization visualization
- Credential management — assign username/password per slot
- Active allocations view with remaining days counter
- Allocation history with date-range filtering
- Automated email on accept/reject with access credentials
- Access expiry reminders and auto-release of expired slots

---

## Tech Stack

| Layer | Technology                                         |
|-------|----------------------------------------------------|
| Frontend | Angular 17 (Standalone Components)                 |
| Styling | Custom CSS                                         |
| Backend | Java Spring Boot                                   |
| Database | PostgreSQL / ORACLE                                |
| Email | Spring Mail (JavaMailSender) + Thymeleaf templates |
| Auth | OTP-based email verification                       |
| Hosting | University college server (intranet only)          |

---

## Screenshots

### Home Page
![Home page](home.png)
### OTP Verification
![OTP mail](otp-mail.png)

### Admin — Pending Requests
![OTP mail](pending-request.png)
### Admin — Slot Selection
![OTP mail](slot-selection.png)

### Admin — Resource Overview
![OTP mail](resource-overview.png)

---

## Usage

### For Students / Faculty

1. Open the application on the university network.
2. Enter your `@kletech.ac.in` email address.
3. Verify your email using the OTP sent to your inbox.
4. Fill in the request form, select resource type, number of days.
5. Submit and wait for admin approval via email.

### For Administrators

1. Navigate to `/admin` and log in.
2. View pending requests on the dashboard.
3. Click **Accept** to open the slot allocation modal:
   - Select a resource and one or more slots.
   - Set a default (3-day) or custom access duration.
   - Optionally update the slot password before sending.
4. Click **Reject** with an optional reason.
5. All actions trigger automatic email notifications to users.

---

## Role / Contribution

**Solo Developer — Full Stack**

Solely responsible for the entire project lifecycle:

- Designed the database schema and REST API architecture
- Built all backend services, controllers, and scheduled jobs in Spring Boot
- Developed the Angular frontend including admin dashboard, modals, and user forms
- Integrated OTP-based email verification and automated transactional emails
- Implemented real-time slot availability checks and request queue management
- Deployed and configured the application on the university server

---


## License

This project is proprietary and intended for internal use at KLE Technological University — Central Computing Facility. No open-source license is applied.

---

## Contact

###### Email: ars.archit6@gmail.com
###### LinkedIn:[ linkedin.com/in/architrshet](https://linkedin.com/in/architrshet)
###### GitHub: [github.com/Arcsgit](https://github.com/Arcsgit)

Built by [Archit Shet]

---

*Built for KLE Technological University — Central Computing Facility*
