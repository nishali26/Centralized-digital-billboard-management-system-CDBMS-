# 📺 Centralized Digital Billboard Management System (CDBMS)

**CDBMS** is an end-to-end IoT and full-stack digital signage platform designed to remotely manage, schedule, and broadcast multimedia advertisements across distributed digital billboards powered by **Raspberry Pi** display nodes.

[![Live Frontend](https://img.shields.io/badge/Frontend-Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://bilboard-project.vercel.app/)
[![Live Backend](https://img.shields.io/badge/Backend-Render-46E3B7?style=for-the-badge&logo=render&logoColor=black)](https://cdbms-backend-w86i.onrender.com/)
[![Hardware](https://img.shields.io/badge/Edge_Node-Raspberry_Pi-A22846?style=for-the-badge&logo=raspberrypi&logoColor=white)]()
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)]()

---

## 🌐 Live Deployments

| Service | Platform | Live URL |
| :--- | :--- | :--- |
| **Web Dashboard (Frontend)** | Vercel | [https://bilboard-project.vercel.app/](https://bilboard-project.vercel.app/) |
| **REST API & Media Server (Backend)** | Render | [https://cdbms-backend-w86i.onrender.com/](https://cdbms-backend-w86i.onrender.com/) |
| **GitHub Repository** | GitHub | [Centralized-digital-billboard-management-system-CDBMS-](https://github.com/nishali26/Centralized-digital-billboard-management-system-CDBMS-) |

---

## 📸 System Preview & Screenshots

> *Replace the placeholders below with your actual dashboard and Raspberry Pi hardware setup screenshots.*

### 🖥️ Admin Control Dashboard
![Admin Dashboard Preview](docs/images/dashboard-preview.png)
<!-- Replace path above with your dashboard screenshot -->

### 📅 Campaign Scheduling & Playlist Manager
![Campaign Scheduler Preview](docs/images/scheduler-preview.png)
<!-- Replace path above with your scheduling interface screenshot -->

### 🍓 Raspberry Pi Edge Display Node
![Raspberry Pi Billboard Setup](docs/images/raspberry-pi-setup.png)
<!-- Replace path above with a photo of your Raspberry Pi connected to the display screen -->

---

## 🎯 Problem Statement & Solution

Traditional digital billboards often rely on manual USB updates or isolated local media players, making multi-location ad updates slow, error-prone, and difficult to monitor.

**CDBMS solves this by centralizing content distribution:**
- **Remote Content Delivery:** Upload images and videos once from a web dashboard and push them to targeted billboard screens instantly.
- **Automated Scheduling:** Define start/end dates, time slots, and playback durations without manual intervention at the physical site.
- **Edge Synchronization:** Lightweight client software running on **Raspberry Pi** devices polls/syncs with the cloud backend, caches media locally for uninterrupted playback, and reports real-time device health.

---

## 🏗️ System Architecture

```text
+-------------------------------------------------------------------+
|                     ADMIN / OPERATOR (Browser)                    |
|              React Frontend (Hosted on Vercel)                    |
|          [https://bilboard-project.vercel.app/](https://bilboard-project.vercel.app/)                     |
+---------------------------------+---------------------------------+
                                  |
                                  | HTTPS / REST API
                                  v
+---------------------------------+---------------------------------+
|                   CENTRAL CLOUD SERVER (Backend)                  |
|            Node.js / Express API (Hosted on Render)               |
|          [https://cdbms-backend-w86i.onrender.com/](https://cdbms-backend-w86i.onrender.com/)                 |
|                                                                   |
|   [ Auth & RBAC ]   [ Media Storage ]   [ Schedule Engine ]       |
+---------------------------------+---------------------------------+
                                  |
                                  | Secure Media Sync & Heartbeat
                                  v
+---------------------------------+---------------------------------+
|                 EDGE DISPLAY NODES (Field Hardware)               |
|             Raspberry Pi OS + Kiosk Media Player                  |
|                                                                   |
|   [ Local Cache ] ---> [ Fullscreen HDMI Billboard Display ]      |
+-------------------------------------------------------------------+