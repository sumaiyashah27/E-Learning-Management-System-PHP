# PHP E-Learning Management System

## Introduction
This is a fully functional **E-Learning Management System** built with PHP and MySQL. The system allows users to register as both **students and teachers**, enroll in courses, upload video lectures, take quizzes, earn certificates, and track progress. Admins can manage courses, students, teachers, and payments.

## Features
- **User Roles**: Students & Teachers
- **Course Management**: Create, edit, delete, and publish courses
- **Video Lectures & Study Materials**: Upload and manage course content
- **Quiz & Assessment System**: Interactive quizzes with scoring
- **Certificates**: Auto-generated certificates upon course completion
- **Teacher Dashboard**: Manage courses, earnings, and students
- **Student Dashboard**: Track progress, enrolled courses, and quiz scores
- **Payment Gateway Integration**: Secure payments for paid courses

## Prerequisites
Before installing, ensure you have:
- **XAMPP** (Apache, MySQL, PHP)
- **PHP**
- **MySQL**
- **phpMyAdmin** (for database management)

## Installation & Setup

### 1. Clone the Repository
```sh
git clone https://github.com/sumaiyashah27/E-Learning-Management-System-PHP.git
cd E-Learning-Management-System-PHP
```

### 2. Configure Database
1. Start **XAMPP** and ensure Apache & MySQL services are running.
2. Open **phpMyAdmin** (`http://localhost/phpmyadmin/`).
3. Create a new database named `course-db`:
```sql
CREATE DATABASE course-db;
```
4. Import the provided SQL file:
   - Click on the database `course-db`.
   - Go to the **Import** tab and upload `database/course-db.sql`.

### 3. Configure Database Connection
Modify `config.php` to match your XAMPP settings:
```php
<?php
$servername = "localhost";
$username = "root";
$password = ""; // Default is empty in XAMPP
$dbname = "course-db";
$conn = new mysqli($servername, $username, $password, $dbname);
if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}
?>
```

### 4. Start the Server
1. Move the `E-Learning-Management-System-PHP` folder to `htdocs` inside your XAMPP installation.
2. Open **XAMPP Control Panel** and start **Apache** & **MySQL**.
3. Open your browser and visit:
   ```
   http://localhost/E-Learning-Management-System-PHP/
   ```

## Troubleshooting
- Ensure **XAMPP’s Apache & MySQL** services are running.
- If a **database connection error** appears, verify `config.php` settings.
- If the site **does not load**, ensure the project folder is inside `htdocs`.
- Check for **errors in `error_log`** or enable debugging in `php.ini` by setting `display_errors=On`.

## 📧 Contact
For any queries or support, feel free to reach out:
-  **Email:** [sumaiyashah647@gmail.com](mailto:sumaiyashah647@gmail.com)
-  **LinkedIn:** [Sumaiya Shah](https://www.linkedin.com/in/sumaiya-shah-7a0706224/)

