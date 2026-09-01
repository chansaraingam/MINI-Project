# QR Based Product Usage: Client-Server Architecture

A web-based QR Verification System developed as a mini-project for **RT 524 Digital Agriculture** at **IIT Guwahati**[cite: 1]. The system allows users to record and store QR code data securely with automatic timestamping[cite: 1].

---

## 📌 Project Overview

This project provides a web application built using the LAMP stack[cite: 1]. It enables users to submit QR codes either manually or by uploading an image file[cite: 1]. The backend stores these records in a MySQL database alongside user information, auto-generated timestamps, and status indicators[cite: 1].

---

## 👥 Contributors

* **Anshuman Ghosh** (25415001)[cite: 1]
* **Chansa Raingam** (254154003)[cite: 1]
* **Program:** M.Tech, SART, IIT Guwahati[cite: 1]

---

## 🛠️ Technologies Used

* **Linux**: Operating System[cite: 1]
* **Apache**: Web Server managing client-server HTTP requests[cite: 1]
* **MySQL / MariaDB**: Relational Database Management System[cite: 1]
* **PHP**: Server-side processing[cite: 1]
* **phpMyAdmin**: Database Administration Tool[cite: 1]
* **HTML/CSS**: Frontend Interface[cite: 1]

---

## ⚙️ Database Schema

Database Name: `qr_project`[cite: 1]  
Table Name: `scans`[cite: 1]

| Field | Type | Extra / Constraints | Description |
| :--- | :--- | :--- | :--- |
| **id** | `INT` | PRIMARY KEY, AUTO_INCREMENT | Unique identifier for each entry[cite: 1] |
| **qr_id** | `VARCHAR(100)` | — | Manually entered code or image filename[cite: 1] |
| **user** | `VARCHAR(50)` | — | Identifier of the submitting user[cite: 1] |
| **timestamp** | `TIMESTAMP` | Default: `CURRENT_TIMESTAMP` | Automatic record timestamp[cite: 1] |
| **status** | `VARCHAR(20)` | Default: `pending` | Verification status[cite: 1] |

---

## 🔄 System Workflow

1. **Client (Browser):** User inputs a manual QR string or uploads an image file via the HTML form[cite: 1].
2. **HTTP Request:** Form submits a `POST` request to the server[cite: 1].
3. **Apache & PHP:** Process the input validation and handle file handling[cite: 1].
4. **Database (MySQL):** Inserts a record into the `scans` table with status set to `pending` and an automatic timestamp[cite: 1].
5. **Response:** Server returns feedback confirming data submission[cite: 1].

---

## 🚀 Future Enhancements

* Add live QR code scanning via mobile camera integration[cite: 1].
* Implement an Admin Panel for verification approval and rejection workflows[cite: 1].
* Integrate backend QR image decoding libraries instead of relying on filenames[cite: 1].
* Add user authentication and role-based login capabilities[cite: 1].
