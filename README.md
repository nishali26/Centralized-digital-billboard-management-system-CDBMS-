# 📺 Centralized Digital Billboard Management System (CDBMS)

<p align="center">

**A Full-Stack IoT-Enabled Digital Signage and Billboard Management Platform**

A centralized platform for managing digital billboards, advertisers, advertisement bookings, campaign schedules, payments, and remote multimedia display operations.

</p>

<p align="center">

![React](https://img.shields.io/badge/Frontend-React.js-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Node.js](https://img.shields.io/badge/Backend-Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/API-Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/Database-MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)

![Raspberry Pi](https://img.shields.io/badge/Hardware-Raspberry%20Pi-A22846?style=for-the-badge&logo=raspberrypi&logoColor=white)
![Arduino](https://img.shields.io/badge/Hardware-Arduino%20Uno-00878A?style=for-the-badge&logo=arduino&logoColor=white)
![Vercel](https://img.shields.io/badge/Deployment-Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![Render](https://img.shields.io/badge/Deployment-Render-46E3B7?style=for-the-badge&logo=render&logoColor=black)

![License](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)

</p>

---

## 🌐 1. Project Overview

The **Centralized Digital Billboard Management System (CDBMS)** is a full-stack digital signage and advertisement management platform developed to simplify and automate the management of digital billboard advertising.

The system provides a centralized environment where administrators and advertisers can manage billboard availability, upload multimedia advertisements, reserve advertising slots, process payments, approve campaigns, and control advertisement playback.

Instead of relying on traditional manual advertisement updates, CDBMS introduces a centralized web-based solution that connects the management dashboard, cloud backend, database, and physical display infrastructure.

The platform combines modern web technologies with hardware-assisted display functionality to provide an integrated digital advertising workflow.

### Core Objectives

- Centralize the management of multiple digital billboards.
- Simplify billboard registration and availability management.
- Allow advertisers to upload and manage promotional content.
- Automate advertisement booking and scheduling.
- Introduce secure online payment processing.
- Provide administrative approval and campaign management.
- Connect digital display infrastructure with the centralized backend.
- Reduce manual intervention in advertisement management and playback.

---

## 🔗 2. Live Deployments & Project Resources

| Service | Platform | Link |
|---|---|---|
| Web Application | Vercel | [Open CDBMS Dashboard](https://bilboard-project.vercel.app/) |
| Backend API | Render | [Backend Server](https://cdbms-backend-w86i.onrender.com/) |
| Source Code | GitHub | [View Repository](https://github.com/nishali26/Centralized-digital-billboard-management-system-CDBMS-) |

---

## 📸 3. Application Interface & System Preview

The following sections are intended to showcase the major components of the CDBMS platform.

Replace the image paths with actual screenshots from the application.

### 3.1 Admin Dashboard

The administrative dashboard provides centralized access to billboard management, advertiser accounts, booking requests, and campaign approvals.

![Admin Dashboard](docs/images/admin-dashboard.png)

### 3.2 Advertiser Dashboard

Advertisers can access their accounts, manage advertising content, explore available billboards, and monitor their booking activities.

![Advertiser Dashboard](docs/images/advertiser-dashboard.png)

### 3.3 Billboard Management

The billboard management interface allows administrators to manage registered display locations and their associated advertising slots.

![Billboard Management](docs/images/billboard-management.png)

### 3.4 Advertisement Booking & Scheduling

The booking interface allows advertisers to select billboards, check available time slots, and submit advertising requests.

![Booking Management](docs/images/booking-management.png)

### 3.5 Payment & Transaction Interface

The payment workflow integrates Stripe Checkout to facilitate advertisement booking payments.

![Payment Interface](docs/images/payment-interface.png)

### 3.6 Digital Billboard Display

The display interface retrieves approved and currently scheduled advertisements for playback on the designated screen.

![Billboard Display](docs/images/billboard-display.png)

### 3.7 Hardware Integration

The project includes hardware-related components for connecting digital display infrastructure with the centralized management platform.

![Hardware Setup](docs/images/hardware-setup.png)

---

## 🎯 4. Problem Statement

Traditional digital billboard management often involves manual advertisement updates, disconnected media players, and limited centralized control.

Managing multiple billboards becomes increasingly difficult when administrators need to coordinate advertisers, availability, scheduling, payments, and advertisement approvals.

Common challenges include:

- Manual advertisement updates.
- Difficulty managing multiple billboard locations.
- Conflicts between advertising reservations.
- Lack of centralized booking management.
- Manual payment verification.
- Delays in advertisement approval.
- Limited integration between software and physical displays.

### Our Solution

CDBMS addresses these challenges through a centralized digital platform that connects advertisers, administrators, backend services, databases, and billboard display infrastructure.

The system provides an integrated workflow:

1. Advertisers create accounts and access the platform.
2. Advertisers explore available billboards.
3. They select advertising dates and available time slots.
4. The system processes booking requests.
5. Payments are handled through Stripe Checkout or the configured demonstration payment mode.
6. Administrators review and approve paid bookings.
7. Approved advertisements become eligible for scheduled display.
8. The billboard display component retrieves and presents the active advertisement.

This workflow improves advertisement management, reduces manual coordination, and provides a structured approach to digital billboard operations.

---

## 🏗️ 5. System Architecture

CDBMS follows a modular architecture consisting of a frontend application, backend API, database, payment integration, and hardware/display components.

### High-Level Architecture

```text
                  ADMIN / ADVERTISER
                          |
                          |
                          v
              +------------------------+
              |    REACT FRONTEND      |
              |                        |
              |  Admin Dashboard       |
              |  Advertiser Dashboard  |
              |  Booking Management    |
              |  Billboard Display     |
              +-----------+------------+
                          |
                          |
                     REST API
                          |
                          v
              +------------------------+
              |    NODE.JS BACKEND     |
              |      EXPRESS.JS        |
              |                        |
              | Authentication         |
              | Billboard Management   |
              | Booking Management     |
              | Advertisement Handling |
              | Payment Integration    |
              | Scheduling Logic        |
              +-----------+------------+
                          |
               +----------+----------+
               |                     |
               v                     v
       +---------------+     +----------------+
       |   MongoDB     |     | Stripe Checkout|
       |               |     |                |
       | Users         |     | Payments       |
       | Billboards     |     | Verification   |
       | Bookings       |     | Refund Workflow|
       +---------------+     +----------------+
                          |
                          |
                          v
              +------------------------+
              |  DIGITAL DISPLAY LAYER |
              |                        |
              | Display Simulator      |
              | Raspberry Pi Client    |
              | Arduino USB Bridge     |
              +-----------+------------+
                          |
                          v
                 DIGITAL BILLBOARD
                   / DISPLAY SCREEN
```

### Architecture Components

| Component | Responsibility |
|---|---|
| React Frontend | User interface and dashboard management |
| Node.js | Backend application runtime |
| Express.js | REST API and server-side routing |
| MongoDB Atlas | Persistent application data |
| Stripe | Payment processing |
| Raspberry Pi | Dedicated edge display hardware |
| Arduino Uno | USB-based hardware status/demo bridge |
| Vercel | Frontend hosting |
| Render | Backend hosting |

---

## ✨ 6. Key Features & Functionalities

### 🔐 6.1 Authentication & Access Management

The platform provides account authentication and role-based access for different application users.

Features include:

- Secure user registration and login.
- JWT-based authentication.
- Password hashing using bcrypt.
- Administrator account initialization.
- Protected application routes.
- Separate administrator and advertiser workflows.

### 🖥️ 6.2 Centralized Billboard Management

Administrators can manage digital billboard information through a centralized interface.

Features include:

- Billboard registration and management.
- Billboard availability by location and time slot.
- City-based billboard organization.
- Billboard identification and management.
- Dedicated display access through billboard-specific URLs.

### 👥 6.3 Advertiser Management

Advertisers can register and use the platform to manage their advertising activities.

Features include:

- Advertiser registration.
- Account authentication.
- Advertisement submission.
- Billboard selection.
- Booking history and status tracking.
- Campaign management.

### 🎞️ 6.4 Advertisement & Media Management

The system supports promotional media management for digital billboard campaigns.

Features include:

- Advertisement uploads.
- Image and video content support.
- Billboard-specific advertisement assignment.
- Scheduled advertisement retrieval.
- Media playback through the display interface.

### 📅 6.5 Automated Booking & Scheduling

The booking module allows advertisers to reserve available billboard advertising slots.

The system supports:

- Billboard selection.
- Date and time-slot selection.
- Availability checking.
- Booking request creation.
- Double-booking prevention.
- Booking status management.
- Scheduled advertisement activation.

**Booking lifecycle:**

```text
PENDING
   |
   v
PAID
   |
   v
APPROVED
   |
   v
ACTIVE
```

Administrator rejection and payment refund handling are also supported in the configured Stripe workflow.

### 💳 6.6 Online Payment Integration

CDBMS integrates Stripe Checkout for advertisement booking payments.

Payment workflow:

1. Advertiser selects a billboard and time slot.
2. Frontend requests a payment session from the backend.
3. Backend creates a Stripe Checkout session.
4. Advertiser completes the payment through Stripe.
5. The application verifies the payment session.
6. The booking is updated to paid status.
7. Administrator reviews and approves the booking.
8. Configured Stripe Connect functionality can initiate a payout to a connected account.

Additional payment functionality:

- Stripe-hosted checkout.
- Payment verification.
- Configurable demonstration payment mode.
- Refund handling for eligible rejected bookings.
- Optional connected-account payout integration.

**Note:** Demonstration payment mode simulates payment operations and does not transfer real money.

### 📺 6.7 Digital Billboard Display System

The display module connects the application with the digital advertisement playback environment.

Its responsibilities include:

- Billboard-specific display access.
- Retrieving active advertisement information.
- Checking scheduled advertisement availability.
- Displaying currently eligible advertisements.
- Fullscreen display support.
- Browser-based display simulation.

### 🍓 6.8 Hardware Integration

The project includes hardware-related components for connecting physical display infrastructure to the centralized software platform.

**Raspberry Pi integration**

The Raspberry Pi component is intended for dedicated display operation, including media playback through the configured Python-based player and HDMI-connected screen.

**Arduino Uno integration**

The Arduino component provides a USB-based hardware bridge for status and demonstration functionality. The browser-based display simulator handles advertisement retrieval and rendering.

These are separate hardware integration approaches and should not be confused with one another.

### 💾 6.9 Display Reliability

The display infrastructure is designed to support continuous advertisement presentation.

The Raspberry Pi playback setup can use locally available media and a fullscreen player, reducing dependence on continuous manual interaction.

---

## 🛠️ 7. Technology Stack

The project uses a combination of modern frontend, backend, database, payment, and hardware technologies.

| Layer | Technologies |
|---|---|
| Frontend | React.js, JavaScript, HTML5, CSS3 |
| Frontend Tooling | Vite |
| Backend | Node.js, Express.js |
| API Architecture | RESTful APIs |
| Database | MongoDB Atlas |
| Authentication | JWT, bcrypt |
| Payment Processing | Stripe Checkout, Stripe Connect |
| Hardware | Raspberry Pi, Arduino Uno |
| Hardware Programming | Python, Arduino C/C++ |
| Display Playback | VLC, Chromium Kiosk |
| Deployment | Vercel, Render |
| Version Control | Git, GitHub |
| Development | VS Code, npm |

---

## 📂 8. Repository Structure

The repository is organized into separate modules to maintain a clear separation between frontend development, backend services, and hardware integration.

```text
Centralized-digital-billboard-management-system-CDBMS/
│
├── backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── config/
│   ├── server.js
│   └── package.json
│
├── react-frontend/
│   ├── public/
│   ├── src/
│   ├── index.html
│   └── package.json
│
├── raspberry-pi/
│   └── Raspberry Pi display client files
│
├── arduino/
│   ├── CDBMS_UNO_DisplayBridge.ino
│   └── README.md
│
├── .gitignore
├── package.json
├── render.yaml
├── DEPLOYMENT_CHECKLIST.md
├── start-cdbms.cmd
├── start-cdbms-public.cmd
├── start-cdbms-public.ps1
└── README.md
```

*Note: The structure above is a logical overview. Some internal filenames and folders may vary with the current repository version.*

---

## ⚙️ 9. Local Development Setup

Follow these steps to configure and run CDBMS locally.

### Prerequisites

Install the following software before starting:

- Node.js 18 or later.
- npm.
- Git.
- MongoDB Atlas account or MongoDB connection.
- Stripe account for payment testing.
- Arduino IDE (if testing Arduino integration).
- Raspberry Pi OS (if testing the dedicated Raspberry Pi display client).

### Step 1: Clone the Repository

```bash
git clone https://github.com/nishali26/Centralized-digital-billboard-management-system-CDBMS-.git

cd Centralized-digital-billboard-management-system-CDBMS-
```

### Step 2: Install Dependencies

From the project root directory:

```bash
npm run install:all
```

This installs the dependencies for the application modules using the configured root scripts.

### Step 3: Configure Backend Environment Variables

Navigate to the backend directory and create a `.env` file.

```bash
cd backend
```

Configure the required environment variables:

```env
PORT=5000

MONGO_URI=your_mongodb_connection_string

JWT_SECRET=your_secure_jwt_secret

DEMO_PAYMENT_MODE=true

STRIPE_SECRET_KEY=your_stripe_secret_key

STRIPE_PUBLISHABLE_KEY=your_stripe_publishable_key

STRIPE_CONNECTED_ACCOUNT_ID=your_connected_account_id

ADMIN_NAME=Administrator

ADMIN_EMAIL=admin@example.com

ADMIN_PASSWORD=your_admin_password
```

**Important:**

- Replace placeholder values with your own credentials.
- Keep all secret keys private.
- Never commit `.env` files to GitHub.
- Stripe connected-account configuration is optional for payout functionality.
- Use Stripe test credentials when developing and testing payments.

### Step 4: Configure Frontend Environment Variables

Navigate to the frontend directory:

```bash
cd react-frontend
```

Create a `.env` file:

```env
VITE_API_URL=http://localhost:5000/api
```

This variable specifies the backend API endpoint used by the frontend.

### Step 5: Run the Application

Return to the project root directory.

```bash
npm run dev
```

Alternatively, on Windows, use:

```bash
start-cdbms.cmd
```

The development environment starts the frontend and backend services.

| Service | Local URL |
|---|---|
| React Frontend | http://localhost:5173 |
| Backend API | http://localhost:5000 |
| Display Simulator | http://localhost:5173/display-simulator.html |

### Step 6: Configure the Display System

For browser-based display testing:

1. Open the frontend application.
2. Access the billboard management interface.
3. Select the desired billboard.
4. Open its dedicated display URL.
5. Use the browser fullscreen option to simulate a digital billboard.

For hardware testing, configure the appropriate Raspberry Pi or Arduino component using its respective setup instructions.

---

## 💳 10. Payment Workflow

CDBMS uses a structured payment and approval workflow.

### Stripe Payment Process

```text
Advertiser Selects Billboard
           |
           v
     Select Time Slot
           |
           v
   Create Booking Request
           |
           v
    Stripe Checkout
           |
           v
   Payment Verification
           |
           v
    Booking Marked Paid
           |
           v
    Admin Approval
           |
           v
     Booking Active
           |
           v
   Advertisement Display
```

### Demonstration Payment Mode

The application also supports a configurable demonstration payment workflow.

When enabled:

- Advertisers can complete a simulated card-style payment process.
- Bookings can be marked as paid for demonstration purposes.
- Administrator approval simulates payout processing.
- Rejected bookings simulate refund handling.
- No real financial transactions occur.

---

## 🔌 11. Hardware Integration & Display Workflow

The hardware component extends the web application beyond a traditional dashboard.

### Raspberry Pi Display Architecture

The Raspberry Pi can serve as a dedicated edge device connected to an external digital display through HDMI.

The intended setup consists of:

- Raspberry Pi hardware.
- Raspberry Pi OS.
- Network connectivity.
- Python-based display client.
- VLC media playback.
- HDMI-connected display.

The configured playback environment can use fullscreen media playback and local media files.

### Arduino USB Integration

The Arduino Uno integration provides a hardware status and demonstration bridge.

The browser communicates with the Arduino through USB using the Web Serial interface in supported browsers.

The Arduino is not responsible for independently retrieving online advertisement content or rendering the billboard interface.

### Display Management Workflow

1. Administrator registers and manages billboard information.
2. Advertiser submits an advertisement booking.
3. The system processes the booking and payment.
4. Administrator approves the booking.
5. The display component retrieves the appropriate active advertisement.
6. The screen presents the scheduled content.

---

## 🚀 12. Deployment & Infrastructure

CDBMS uses cloud deployment services to make its frontend and backend accessible over the internet.

### Frontend Deployment — Vercel

The React frontend is hosted on Vercel.

Deployment responsibilities:

- Frontend hosting.
- Production build management.
- Public dashboard accessibility.
- Environment variable configuration.

Live application:

https://bilboard-project.vercel.app/

### Backend Deployment — Render

The Node.js and Express backend is hosted on Render.

Deployment responsibilities:

- REST API hosting.
- Database connectivity.
- Authentication services.
- Booking and payment operations.
- Advertisement management.

Backend URL:

https://cdbms-backend-w86i.onrender.com/

### Database — MongoDB Atlas

MongoDB Atlas provides cloud database connectivity for application data, including user accounts, billboard information, and booking records.

---

## 🔒 13. Security & Data Management

Security is an important part of the CDBMS architecture.

Implemented security-related functionality includes:

- JWT-based authentication.
- Password hashing using bcrypt.
- Protected application routes.
- Backend-side payment verification.
- Environment-based secret configuration.
- Booking availability validation.
- Double-booking prevention.
- Server-side request handling.

Sensitive credentials such as database connection strings, JWT secrets, and payment API keys must be stored in environment variables rather than committed to the repository.

---

## 🧪 14. Testing & Validation

The application should be validated across its major workflows before production deployment.

Recommended functional validation areas include:

| Area | Validation |
|---|---|
| Authentication | Registration and login |
| Authorization | Admin and advertiser access |
| Billboard Management | Billboard creation and management |
| Booking | Slot availability and booking creation |
| Scheduling | Date and time-based activation |
| Payments | Stripe checkout and verification |
| Approval | Admin approval and rejection |
| Display | Active advertisement retrieval |
| Hardware | Display connectivity and playback |
| Deployment | Frontend and backend accessibility |

---

## 🚀 15. Future Enhancements

Although CDBMS provides a centralized billboard management workflow, several enhancements can further extend its capabilities.

### 📊 Proof-of-Play Analytics

Introduce automated playback records, advertisement duration tracking, and campaign performance reports.

### 🤖 AI-Powered Advertisement Selection

Integrate artificial intelligence to analyze contextual information and recommend relevant advertisements.

For example, the system could use aggregated contextual signals, such as time of day or campaign settings, to select suitable promotional content.

### 📡 Advanced Device Monitoring

Introduce centralized device health monitoring, connectivity alerts, synchronization reports, and device-level diagnostics.

### 🌦️ Dynamic Content Integration

Support dynamic information such as weather updates, time-based announcements, and contextual digital signage.

### ⚡ Priority Display Management

Introduce an authorized priority content mechanism for urgent announcements and important public information.

### 📈 Advertiser Performance Dashboard

Provide advertisers with campaign-level statistics, booking history, and advertisement performance reports.

---

## 🎓 16. Project Outcomes & Technical Learning

Developing CDBMS involved integrating several areas of software engineering into one working application.

Key technical areas demonstrated by the project include:

- Full-stack web application development.
- REST API design and integration.
- Database modeling and management.
- Authentication and access control.
- Online payment integration.
- Booking and scheduling logic.
- Hardware and software integration.
- Digital media management.
- Cloud deployment.
- Version control and project organization.

The project demonstrates how web technologies, cloud services, payment systems, and hardware components can work together to build a centralized digital signage solution.

---

## 👩‍💻 17. Author & Project Information

**Author:** Nisha Ali

**Project Name:** Centralized Digital Billboard Management System (CDBMS)

**Project Type:** Final Year Project

**Domain:** Full-Stack Development | IoT | Digital Signage | Cloud Computing

**GitHub:** [@nishali26](https://github.com/nishali26)

**Repository:** [Centralized Digital Billboard Management System](https://github.com/nishali26/Centralized-digital-billboard-management-system-CDBMS-)

---

## 📄 18. License

This project is distributed under the MIT License.

See the `LICENSE` file for additional information.

---

<p align="center">

**Centralized Digital Billboard Management System**

*Connecting Advertisers, Cloud Technology, and Digital Display Infrastructure.*

</p>