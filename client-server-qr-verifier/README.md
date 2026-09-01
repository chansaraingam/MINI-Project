# QR-Based Product Usage Verification System

A web-based client-server application developed for tracking and managing QR code data with automated timestamping[cite: 1]. Developed for the RT 524 Digital Agriculture course at the Indian Institute of Technology Guwahati[cite: 1].

## Overview

The QR Verification System uses a LAMP stack architecture to record and store product usage records[cite: 1]. Users submit data by manually entering a QR identifier or uploading a QR image file[cite: 1]. The system records the input along with user identification, time of submission, and verification status in a relational database[cite: 1].

## Project Details

* **Institution:** Indian Institute of Technology Guwahati[cite: 1]
* **Course:** RT 524 Digital Agriculture[cite: 1]
* **Department:** M.Tech, SART[cite: 1]
* **Authors:** Anshuman Ghosh (25415001), Chansa Raingam (254154003)[cite: 1]

## Technical Stack

* **Operating System:** Linux[cite: 1]
* **Web Server:** Apache[cite: 1]
* **Database Management System:** MySQL / MariaDB[cite: 1]
* **Server-Side Scripting:** PHP[cite: 1]
* **Database Administration:** phpMyAdmin[cite: 1]
* **User Interface:** HTML[cite: 1]

## Database Schema

Database Name: `qr_project`[cite: 1]  
Table Name: `scans`[cite: 1]

| Field Name | Data Type | Attributes / Constraints | Description |
| :--- | :--- | :--- | :--- |
| `id` | `INT` | Primary Key, Auto Increment | Unique record identifier[cite: 1] |
| `qr_id` | `VARCHAR(100)` | Standard | Manual QR string or uploaded image filename[cite: 1] |
| `user` | `VARCHAR(50)` | Standard | User account or session identifier[cite: 1] |
| `timestamp` | `TIMESTAMP` | Default: `CURRENT_TIMESTAMP` | Automatic submission timestamp[cite: 1] |
| `status` | `VARCHAR(20)` | Default: `pending` | Verification workflow status[cite: 1] |

## System Workflow

1. **Data Input:** The user submits a manual QR code string or uploads a QR image file through the web interface[cite: 1].
2. **Request Handling:** The browser sends an HTTP POST request containing the form data to the Apache web server[cite: 1].
3. **Backend Processing:** The PHP script validates input data and handles uploaded files[cite: 1].
4. **Data Persistence:** The server writes a new record into the MySQL database with an automatic timestamp and an initial status of `pending`[cite: 1].
5. **Client Response:** The server returns a status message displaying the submission result to the user[cite: 1].

## Future Work

* Integration of camera-based QR scanning directly within the client interface[cite: 1].
* Implementation of an administrative control panel for reviewing, approving, or rejecting submissions[cite: 1].
* Addition of server-side QR image decoding libraries to parse uploaded image content directly[cite: 1].
* Implementation of full user authentication and role-based access control[cite: 1].
