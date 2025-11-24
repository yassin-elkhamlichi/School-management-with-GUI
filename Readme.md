# 🎓 School Management System (Desktop GUI)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![GUI Framework](https://img.shields.io/badge/Framework-PyQt5-green)
![Architecture](https://img.shields.io/badge/Pattern-MVC-orange)
![Database](https://img.shields.io/badge/Database-SQLite-lightgrey)

## 📖 Overview
A comprehensive desktop application designed to streamline administrative tasks for educational institutions.

Unlike simple scripts, this application is engineered using the **MVC (Model-View-Controller)** architectural pattern to ensure separation of concerns between the User Interface (PyQt5) and the Business Logic. It provides a robust solution for managing **Professors**, **Modules**, and **Departments** with persistent data storage using **SQLite**.

## 🚀 Key Features

### 🏛️ Academic Management
* **Professor Directory:** Create, update, and manage faculty records with detailed profiles.
* **Module Allocation:** Assign courses (Modules) to professors and track academic offerings.
* **Department Organization:** Structure the institution by departments (e.g., Computer Science, Math) to maintain data hierarchy.

### 💻 Technical Highlights
* **MVC Architecture:** Strict separation of data (`models/`), logic (`controllers/`), and UI (`views/`) for maintainable code.
* **Data Persistence:** Integrated **SQLite** database for reliable, local storage without requiring a server setup.
* **Responsive GUI:** Built with **PyQt5** (Qt Framework) offering a native, responsive desktop experience compared to standard Tkinter apps.

---

## 🏗️ Project Architecture

The project follows a modular structure to facilitate testing and scalability:

```bash
School-Management-System/
├── main.py                 # Application Entry Point
├── createTables.py         # Database Initialization Script
├── scolarite.db            # SQLite Database (Auto-generated)
│
├── models/                 # [DATA LAYER] Direct Database Interactions
│   ├── database.py         # DB Connection Handler
│   └── (prof, module, department).py
│
├── controllers/            # [LOGIC LAYER] Bridges View and Model
│   └── (prof, module, department)_controller.py
│
└── view/                   # [PRESENTATION LAYER] PyQt5 UI Definitions
    ├── main_window.py      # Main Dashboard
    └── (prof, module, department)_view.py
