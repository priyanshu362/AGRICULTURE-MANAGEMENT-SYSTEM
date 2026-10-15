# Digital Agriculture Management System (AMS)

A Java-based web application designed to help organize and manage farm-related information, crop cycles, operational activities, and financial records through a centralized digital web interface.

## Quick Access — Project Links

| Resource | Access |
| :--- | :--- |
| **GitHub Source Code** | [Digital Agriculture Management System Repository](https://github.com/your-username/digital-agriculture-management-system) |
| **Local Frontend** | Access the user interface via HTML5/CSS3 templates configured in your local environment |
| **Local Backend API / Server** | Java Web / Application Server running on Apache Tomcat |
| **Database Management** | MySQL Database Server managed via MySQL Workbench |
| **Project Documentation (SRS & Diagrams)** | [View Complete SRS Document & System Diagrams](https://drive.google.com/drive/folders/your-folder-link) |

> **Deployment Note:** The frontend and Java backend require local or server-side configuration of your MySQL database connection (JDBC URL, username, and password) before launching production or testing environments.


## Week 1: Team Formation + Guide Selection + Abstract

   Team Members and Responsibilities 

| Name / Roll No. | Gmail | Role | Assigned Module & Responsibilities |
| :--- | :--- | :--- | :--- |
| **Krishan Kumar** |25EARCS703 | sinhakumar060@gmail.com | Frontend | Develop user interface using HTML and CSS; create pages, forms, navigation, responsive layouts, and connect screens to backend endpoints. |
| **Amit Pathak** | 25EARCS701 | amitpathak772004@gmail.com| Backend| Implement Java business logic, authentication/authorization if included, validation, and application workflows. |
| **Abhimanu Kumar** | 25EARCS7OO | Sabhimanusingh3071@gmail.com | Database| Design MySQL schema, tables, relationships, queries, constraints, and persistence operations. |
| **Sachin Kumar** |25EARCS710 | sachink9845k@gmail.com | Testing & Integration | Integrate frontend, backend, and database; prepare test cases; verify workflows and fix integration defects. |
| **Priyanshu Yadav** | 25EARCS707 | yadavpriyanshu362@gmail.com | Documentation & Database| Prepare SRS, diagrams, project report, setup instructions, test evidence, user documentation, and assist with database design. |


## 1. Abstract & Purpose
- **Digital Agriculture Management System (DAMS)** organizes and manages farm-related information in a structured digital form. Digital Agriculture Management System (DAMS) is a software application intended to help organize and manage farm-related information in a structured digital form. The system can provide a centralized interface for maintaining farm, crop, activity, inventory, sales, expense, and report information, depending on the modules implemented by the project team. The proposed system uses HTML and CSS for the frontend, Java for backend processing, and MySQL for persistent data storage. Its purpose is to reduce manual record keeping, improve data organization, and make stored agricultural information easier to retrieve and review.
- Centralizes farm, crop, activity, inventory, sales, expense, and report information to reduce manual record keeping.

## 2. Project Scope & Assumptions
- **In-Scope:** Frontend user interface, farm/farmer records, crop details, farm activities, inventory tracking, financial records, Java backend persistence, and search/listing functions.
- **Out-of-Scope:** IoT sensor integration, live weather forecasting, satellite analysis, AI crop diagnosis, and online marketplace functions unless separately implemented.



# Week 2: Software Requirements Specification (SRS)



## 3. Users and Access 
- **Administrator:** Manage user accounts and system-level records.
- **Farmer / Farm User:** Enter and maintain farm, crop, activity, inventory, and financial records.
- **Staff / Data Entry User (Optional):** Enter or update permitted day-to-day records.
- **Viewer (Optional):** Read permitted records and summaries without modification.

## 4. Functional & Non-Functional Requirements 
- **Functional Requirements (FR-01 to FR-12):** Covers application access, farm/crop/activity records, data validation, database persistence, search/listing, updates, and error handling.
- **Non-Functional Requirements:** Covers usability, performance, reliability, data integrity, security, maintainability, and compatibility.
---


## 1. System Architecture 
- **Client Tier / Presentation Layer:** Built with HTML5, CSS3, and JavaScript, featuring dashboards, crop management views, and administrative panels.
- **Application / Web Server Tier:** Java Web application server running on Apache Tomcat, handling HTTP/REST controllers, business services, and JDBC persistence operations.
- **Data Tier:** MySQL Database Server managing user tables, crop records, soil data, and weather/market caches.

## 2. System Workflow and Data Flow Diagrams 
- **Main Workflow:** Users access the web interface, authenticate via the Java backend, select modules, and execute CRUD operations against the MySQL database.
- **Data Flow:** Captures input collection via frontend forms, server-side validation, database persistence, and formatted response rendering.

## 3. Database Entity Relationship Diagram (ERD) 
- Conceptual data models include tables for `USERS`, `FARMS`, `CROPS`, `ACTIVITIES`, `INVENTORY`, and `SALES_EXPENSES`.
- Establishes primary and foreign key constraints to maintain referential integrity across related farm entities.

## 4. Technology Stack (Section 7)
- **Frontend:** HTML5 and CSS3.
- **Backend:** Java (servlets/JSP or Spring framework mapping implementation).
- **Database:** MySQL managed via MySQL Workbench.

## Week 3: UML & System Design
<img width="1312" height="1199" alt="image" src="https://github.com/user-attachments/assets/b1a67295-3ef1-4fd2-822c-3d1e9b2140f9" />

