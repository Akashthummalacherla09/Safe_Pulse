# Safe_Pulse

# 🏥 SafePulse — Healthcare Management & Patient Monitoring Platform

**SafePulse** is a full-stack healthcare management and patient monitoring platform designed to provide a centralized environment for health assessment, daily health tracking, patient data management, risk evaluation, reporting, and administrative monitoring.

The system combines an **Android mobile application**, **web-based dashboards**, and a **Django REST backend** to provide an integrated, data-driven healthcare solution.

---

## 📌 Overview

SafePulse enables users to perform multiple health assessments, track daily health metrics, view health scores and trends, and access generated reports.

The platform supports assessment modules for:

* 🫀 Heart Health
* 🫘 Kidney Health
* 🫁 Lung Health
* 🧬 Liver Health
* 🎗️ Cancer Risk
* 🧠 Alzheimer's / Brain Health

A centralized assessment engine processes the collected information and generates assessment scores, risk levels, stages, and results based on predefined evaluation rules.

The system also provides administrative dashboards for monitoring users, assessments, reports, alerts, and overall platform activity.

---

## ✨ Key Features

### 👤 User Management

* User registration and login
* User authentication
* Profile management
* Role-based access
* Secure access to personal health information

### 🩺 Health Assessments

Dedicated assessment workflows for:

* Kidney health
* Heart health
* Liver health
* Lung health
* Cancer risk
* Alzheimer's / brain health

The assessment engine processes user inputs and generates:

* Health scores
* Risk levels
* Assessment stages
* Assessment results
* Historical assessment records

### 📊 Daily Health Tracker

Users can record and monitor:

* Water intake
* Daily steps
* Sleep
* Calories
* Smoking status
* Weight
* Blood pressure

The platform calculates daily health scores based on recorded health and lifestyle information.

### 📈 Health Analytics

SafePulse provides:

* Overall health score
* Assessment history
* Personal health trends
* Daily progress
* Risk-level monitoring
* Assessment statistics

### 🚨 Risk Notifications

The Android application uses background processing to identify potentially important assessment results and generate notifications for high, critical, severe, or advanced-stage risks.

### 👨‍⚕️ Patient & Clinical Data Management

The backend manages structured patient and clinical information, including:

* Patient profiles
* Age and gender
* Blood group
* Contact information
* Address
* Weight
* Height
* BMI
* Blood pressure
* Heart rate
* Temperature
* Respiratory rate
* SpO2

### 🖥️ Admin Dashboard

Administrators can monitor:

* Registered users
* Assessment statistics
* Diagnostic reports
* High/critical risk alerts
* Active users
* Recent assessment activity
* Analytics and trends
* Patient information

### 📄 Report Generation

The platform supports structured health and assessment reports, including PDF-based reporting functionality.

### 🔄 Data Synchronization

The Android application communicates with the backend through REST APIs.

The synchronization architecture combines:

* Local SQLite storage
* SharedPreferences
* REST APIs
* Retrofit
* Repository-based data management
* Server-side MySQL persistence

This allows application data to be maintained locally while also synchronizing with the central backend.

---

## 🏗️ System Architecture

```text
                    ┌─────────────────────────┐
                    │       User / Admin      │
                    └────────────┬────────────┘
                                 │
                    ┌────────────▼────────────┐
                    │    Android Application  │
                    │                         │
                    │ Java + Android SDK      │
                    │ AndroidX                │
                    │ Retrofit / OkHttp       │
                    │ SQLite / SharedPrefs    │
                    └────────────┬────────────┘
                                 │
                            REST APIs
                                 │
                    ┌────────────▼────────────┐
                    │     Django Backend      │
                    │                         │
                    │ Django REST Framework   │
                    │ Authentication          │
                    │ Assessment Engine       │
                    │ Tracking                │
                    │ Reports                 │
                    │ Administration          │
                    └────────────┬────────────┘
                                 │
                    ┌────────────▼────────────┐
                    │       MySQL Database    │
                    │                         │
                    │ Users                   │
                    │ Patients                │
                    │ Assessments             │
                    │ Clinical Records        │
                    │ Tracking Data           │
                    │ Reports                 │
                    └─────────────────────────┘
```

---

## 🛠️ Technology Stack

### Programming Languages

* **Java**
* **Python**
* **SQL**
* **JavaScript**

### Android

* Android SDK
* AndroidX
* Material Components
* ConstraintLayout
* Retrofit
* OkHttp
* Gson
* WorkManager
* SQLite
* SharedPreferences

### Backend

* Python
* Django
* Django REST Framework
* REST APIs
* JSON

### Database

* MySQL
* SQLite
* Relational Database Design

### Web

* HTML
* CSS
* JavaScript
* Dashboard interfaces

### Development & Tools

* Git
* GitHub
* API-based client-server communication
* Debugging and testing

---

## 📂 Main Components

The project is organized around several major components:

### Android Application

Responsible for the user-facing mobile experience, including:

* Authentication
* User profiles
* Health assessments
* Daily tracking
* Health scores
* Reports
* Notifications
* Data synchronization

### Assessment Engine

The centralized assessment engine processes inputs from the different health modules and produces structured assessment results.

This helps maintain consistent assessment logic across the application.

### Django REST Backend

Provides APIs for:

* Authentication
* User management
* Health assessments
* Daily tracking
* Patient management
* Clinical records
* Reports
* Synchronization
* Administration

### Database Layer

MySQL provides centralized persistent storage for application data, while SQLite provides local storage for the Android application.

---

## 🔐 Authentication & Authorization

SafePulse implements authenticated access to application resources.

The system supports:

* User registration
* Login
* Token-based authentication
* Protected API endpoints
* User-specific data access
* Administrator functionality
* Role-based access control

---

## 🔄 Application Data Flow

```text
User Input
    ↓
Android Application
    ↓
Local Data Storage
    ↓
Assessment / Tracking Engine
    ↓
Health Score & Risk Evaluation
    ↓
REST API
    ↓
Django REST Backend
    ↓
MySQL Database
    ↓
Reports / Dashboard / Analytics
```

---

## 📊 Health Assessment Workflow

```text
Select Health Module
        ↓
Enter Assessment Information
        ↓
Validate Input
        ↓
Assessment Engine
        ↓
Calculate Score
        ↓
Determine Risk Level
        ↓
Store Assessment Result
        ↓
Display Result & Trends
        ↓
Generate Report / Notification
```

---

## 🧑‍💻 Development Highlights

During the development of SafePulse, the project involved practical implementation of:

* Object-oriented programming
* Android application development
* Backend API development
* RESTful architecture
* Relational database design
* CRUD operations
* Authentication and authorization
* Data validation
* Local and server-side data storage
* Client-server communication
* Data synchronization
* Background task processing
* Dashboard development
* Health data processing
* Report generation
* Debugging and testing
* Modular application architecture

---

## 🎯 Project Objectives

The primary objectives of SafePulse are to:

1. Provide a centralized healthcare management platform.
2. Enable users to perform multiple health assessments.
3. Track important daily health and lifestyle metrics.
4. Generate health scores and risk classifications.
5. Maintain historical assessment information.
6. Provide administrators with centralized monitoring capabilities.
7. Synchronize mobile application data with a backend server.
8. Generate structured health reports.
9. Provide notifications for potentially important risk results.
10. Demonstrate the implementation of a complete client-server healthcare application.

---

## 🚀 Future Enhancements

Potential improvements to the platform include:

* Integration with wearable health devices
* Real-time IoT health monitoring
* Advanced machine-learning-based prediction models
* Doctor-patient communication
* Online appointment management
* Cloud deployment
* Advanced analytics
* Automated clinical recommendations
* More comprehensive health-data visualization
* Enhanced security and privacy controls

---

## 📚 Skills Demonstrated

**Java | Python | SQL | Android Development | Django | Django REST Framework | MySQL | SQLite | REST APIs | Retrofit | OkHttp | Gson | WorkManager | Authentication | CRUD Operations | Database Design | Data Synchronization | Dashboard Development | Data Analytics | Object-Oriented Programming | Git**

---

## 👨‍💻 Project Purpose

SafePulse was developed as an academic software engineering project to gain practical experience in designing and implementing a multi-layered, full-stack application. The project provided hands-on experience across mobile development, backend engineering, database management, API integration, data processing, authentication, reporting, and dashboard development.

---

## ⭐ Project Summary

**SafePulse demonstrates the development of a complete healthcare technology platform connecting an Android client, RESTful backend, relational database, assessment engine, analytics dashboards, reporting system, and notification services into a single integrated application.**
