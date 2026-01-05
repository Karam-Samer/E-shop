# 📚 BookStore System

### UML Analysis & Design Project

This repository contains the **System Analysis and Design documentation** for an online **BookStore System**, along with a **Frontend Prototype** that visually represents the designed architecture and system behavior.

> **Academic Focus:**
> This project primarily emphasizes **UML-based system modeling and behavioral analysis**.
> The frontend implementation serves as a conceptual prototype aligned with the UML diagrams rather than a full production system.
> *This project was developed as part of a **System Analysis and Design** university course.*

---

## 📘 Project Overview

The BookStore System is a web-based application designed to manage online book browsing, purchasing, and order processing.
The system supports multiple roles including **Customer**, **Admin**, and **Shipper**, each interacting with the system through well-defined workflows and responsibilities.

The project aims to:

* Model the system structure and behavior using UML standards.
* Analyze system interactions through detailed sequence flows.
* Provide a clear architectural foundation for future implementation.

---

## 🎯 System Objectives

* Enable customers to browse, search, and purchase books online.
* Allow admins to manage books, orders, and system content.
* Support shipping and order delivery workflows.
* Clearly define system interactions using UML diagrams.

---

## 📊 System Architecture (UML Diagrams)

### 1. Structural Modeling

|                           Class Diagram                           |
| :---------------------------------------------------------------: |
|       ![Class Diagram](Diagrams/diagram_class_structure.jpg)      |
| *Defines system classes, attributes, methods, and relationships.* |

---

### 2. Behavioral Modeling (Sequence Diagrams)

Sequence diagrams describe **detailed interactions for each website use case**, illustrating communication between:
**User → Frontend → Backend → Database**

* **Sequence 01:** User Authentication (Login / Signup)
* **Sequence 02:** Book Purchase & Checkout
* **Sequence 03:** Admin Management Actions
* **Sequences 04–07:** Additional system operations
  *(Available in the `Diagrams/` folder)*

---

### 3. Activity Diagrams

Activity charts illustrate the flow of control for major system processes.

|                    Activity Chart 01                   |                    Activity Chart 02                   |
| :----------------------------------------------------: | :----------------------------------------------------: |
| ![Activity 01](Diagrams/diagram_activity_chart_01.jpg) | ![Activity 02](Diagrams/diagram_activity_chart_02.jpg) |

---

### 4. Use Case Diagram

* **Actors:** Customer, Admin, Shipper
* **Purpose:** Defines system functionality from the user perspective

![Use Case Diagram](Diagrams/diagram_use_case.jpg)

---

### 5. Data Flow Diagram (DFD)

* **Level 1 DFD:** Illustrates data movement between system components

![DFD Level 1](Diagrams/diagram_data_flow_01.jpg)

---

## 🧾 Sequence Diagrams – Detailed Descriptions

All sequence diagrams are accompanied by **full textual use case descriptions**, explaining:

* Preconditions and postconditions
* Step-by-step message flow
* System logic and responses
* Error handling (where applicable)

📂 Located in: `sequence-descriptions/`

---

## 👤 My Contribution

My primary responsibility in this project was:

* **Designing all Sequence Diagrams**
* **Providing full use case descriptions for each website page**
* Modeling detailed interactions between users and system components
* Ensuring alignment between UML behavior and frontend prototype flows

This work demonstrates a strong understanding of **UML behavioral modeling**, **software analysis**, and **system design principles**.

---

## 💻 Frontend Prototype

A bilingual (**English / Arabic**) frontend was developed to visually represent the system requirements.

### Implemented Pages

* Home & Book Browsing
* Login & Registration
* Shopping Cart & Checkout
* Admin & Shipper Interfaces

### Technologies Used

* **HTML5**
* **CSS3**
* **JavaScript**

> The frontend serves as a **conceptual visualization**, not a complete backend-integrated system.

---

## 📂 Repository Structure

```
Diagrams/                → UML diagrams and system models
sequence-descriptions/   → Detailed sequence diagram explanations
HTML/                    → Frontend structure
CSS/                     → Styling files
```

---

## ✅ Conclusion

This project provides a comprehensive UML-based analysis of an online BookStore system, focusing on system behavior, structure, and interaction flows.
It serves as a strong academic reference for **Software Engineering**, **System Analysis**, and **UML Design**.

---

*Last Updated: 2026-01-05*
