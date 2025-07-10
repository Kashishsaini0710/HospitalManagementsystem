# 🏥 Hospital Management System (Java + MySQL)

A **console-based Java application** for managing hospital data including doctors, patients, and appointments using **JDBC and MySQL**.

## 📌 Features

- ✅ Add / View / Update / Delete Patients
- ✅ Add / View / Update / Delete Doctors
- ✅ Book and Manage Appointments
- ✅ Menu-driven console interface
- ✅ MySQL database integration using JDBC

## 📂 Project Structure
📦HospitalManagementSystem
┣ 📄 Doctor.java
┣ 📄 Patient.java
┣ 📄 HospitalManagementSystem.java
┣ 📄 DBConnection.java (optional, if used for JDBC setup)
┗ 📄 README.md

## 🛠️ Tech Stack

- **Java** (JDK 8+)
- **MySQL** (5.7+ or 8+)
- **JDBC** (Java Database Connectivity)
- **IDE**: VS Code / Eclipse / IntelliJ

## 🗃️ Database Setup

1. Open MySQL and run the following:

```sql
CREATE DATABASE hospital_db;

USE hospital_db;

CREATE TABLE doctors (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100),
    specialization VARCHAR(100),
    experience INT
);

CREATE TABLE patients (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100),
    age INT,
    disease VARCHAR(100)
);

CREATE TABLE appointments (
    id INT PRIMARY KEY AUTO_INCREMENT,
    patient_id INT,
    doctor_id INT,
    appointment_date DATE,
    FOREIGN KEY (patient_id) REFERENCES patients(id),
    FOREIGN KEY (doctor_id) REFERENCES doctors(id)
);
Update your DB credentials in the JDBC connection string in the code.




