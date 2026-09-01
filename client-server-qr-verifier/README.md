# QR-Based Product Usage Verification System

A web-based client-server application developed for tracking and managing QR code data with automated timestamping. Developed for the RT 524 Digital Agriculture course at the Indian Institute of Technology Guwahati.

## Overview

The QR Verification System uses a LAMP stack architecture to record and store product usage records. Users submit data by manually entering a QR identifier or uploading a QR image file. The system records the input along with user identification, time of submission, and verification status in a relational database[cite: 1].

## Project Details

* **Institution:** Indian Institute of Technology Guwahati.
* **Course:** RT 524 Digital Agriculture
* **Department:** M.Tech, SART
* **Authors:** Anshuman Ghosh (25415001), Chansa Raingam (254154003)

## Technical Stack

* **Operating System:** Linux
* **Web Server:** Apache
* **Database Management System:** MySQL / MariaDB
* **Server-Side Scripting:** PHP
* **Database Administration:** phpMyAdmin
* **User Interface:** HTML

## Database Schema

Database Name: `qr_project`
Table Name: `scans`

| Field Name | Data Type | Attributes / Constraints | Description |
| :--- | :--- | :--- | :--- |
| `id` | `INT` | Primary Key, Auto Increment | Unique record identifier |
| `qr_id` | `VARCHAR(100)` | Standard | Manual QR string or uploaded image filename |
| `user` | `VARCHAR(50)` | Standard | User account or session identifier |
| `timestamp` | `TIMESTAMP` | Default: `CURRENT_TIMESTAMP` | Automatic submission timestamp |
| `status` | `VARCHAR(20)` | Default: `pending` | Verification workflow status |

## System Workflow

1. **Data Input:** The user submits a manual QR code string or uploads a QR image file through the web interface.
2. **Request Handling:** The browser sends an HTTP POST request containing the form data to the Apache web server.
3. **Backend Processing:** The PHP script validates input data and handles uploaded files.
4. **Data Persistence:** The server writes a new record into the MySQL database with an automatic timestamp and an initial status of `pending`.
5. **Client Response:** The server returns a status message displaying the submission result to the user.

## Future Work

* Integration of camera-based QR scanning directly within the client interface.
* Implementation of an administrative control panel for reviewing, approving, or rejecting submissions.
* Addition of server-side QR image decoding libraries to parse uploaded image content directly.
* Implementation of full user authentication and role-based access control.
