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

 1. Abstract
Digital Agriculture Management System (DAMS) is a software application intended to help organize and manage farm-related information in a structured digital form. The system can provide a centralized interface for maintaining farm, crop, activity, inventory, sales, expense, and report information, depending on the modules implemented by the project team. The proposed system uses HTML and CSS for the frontend, Java for backend processing, and MySQL for persistent data storage. Its purpose is to reduce manual record keeping, improve data organization, and make stored agricultural information easier to retrieve and review.
2. Introduction and Purpose
Agricultural records may be maintained in notebooks, separate files, or informal methods, which can make it difficult to find updated information and prepare summaries. DAMS is intended to centralize selected farm records through a user interface backed by application logic and a relational database. The exact functions available depend on the modules implemented by the project team.
2.1 Scope
•	Provide a user interface for accessing the system and its available modules.
•	Maintain farm and farmer information where included in the implementation.
•	Maintain crop details such as crop name, area, sowing date, season, and status where supported.
•	Record farm activities such as irrigation, fertilizer application, pesticide application, and harvesting if these modules are included.
•	Maintain inventory information for seeds, fertilizers, tools, or other farm supplies if implemented.
•	Record agricultural expenses and sales/income information if included.
•	Store and retrieve records through a Java backend and MySQL database.
•	Provide search, listing, update, and deletion functions according to user permissions and implemented modules.
•	Generate summaries or reports only for data supported by the actual implementation.
2.2 Out of Scope / Assumptions
•	IoT sensor integration, live weather forecasting, satellite analysis, AI crop diagnosis, and online marketplace functions are not assumed to exist unless separately implemented.
•	The system does not guarantee crop yield, market price, weather outcomes, or agricultural advice.
•	Authentication, multiple user roles, and remote deployment should be documented according to the actual code; they are not treated as confirmed implementation details here.
•	The final module list must be aligned with the team's actual project code and approved project brief.
3. Users and Access
The following are proposed user categories. Keep only the roles supported by the actual application.
User category	Possible responsibilities
Administrator (if implemented)	Manage user accounts and system-level records; oversee data and access settings.
Farmer / Farm User	Enter and maintain farm, crop, activity, inventory, and financial records available to the account.
Staff / Data Entry User (optional)	Enter or update permitted records and help maintain day-to-day information.
Viewer (optional)	Read permitted records and summaries without changing data.

4. System Architecture and Core Modules
4.1 High-Level Architecture
The frontend is built using HTML and CSS. User actions are sent to the Java backend, which validates inputs, applies application rules, and reads or writes records in MySQL. The backend returns results to the interface. The exact communication method (for example, servlets, JSP, Spring, or REST endpoints) must match the implemented backend.
 
Figure 1. Proposed high-level architecture.
4.2 Frontend / User Interface
The frontend presents navigation, forms, tables, and result pages for the supported agriculture modules. It should provide clear field labels, input validation messages, consistent page layout, and understandable success/error messages.
4.3 Backend Processing
The Java backend receives user requests, validates the data, applies business rules, and coordinates database operations. It should avoid accepting invalid or incomplete records and should return useful feedback to the frontend.
4.4 Database Management
MySQL stores structured application data. Tables and relationships should be designed to reduce duplication and preserve consistency. Database access should use parameterized queries or the project's equivalent safe persistence mechanism.
4.5 Reports and Summaries
Where included in the project, reports may summarize crop records, farm activities, inventory, expenses, or sales. A report must use stored data and should not present unsupported predictions as verified facts.
5. Functional Requirements
ID	Requirement
FR-01 — Application access	The system shall provide an interface through which users can access the implemented modules.
FR-02 — Farm records	If included, the system shall allow authorized users to add, view, update, and delete farm details.
FR-03 — Crop records	If included, the system shall store and retrieve crop details such as crop name, season, area, and dates.
FR-04 — Activity records	If implemented, the system shall record farm activities and their dates/details.
FR-05 — Inventory	If implemented, the system shall maintain item names, quantities, and related inventory details.
FR-06 — Financial records	If implemented, the system shall store expense and sales/income entries with dates and amounts.
FR-07 — Data validation	The system shall validate required fields and reject invalid input before saving records.
FR-08 — Database persistence	The system shall store and retrieve supported records through the Java backend and MySQL database.
FR-09 — Search and listing	Where included, the system shall display saved records and allow users to locate records using available filters/search fields.
FR-10 — Update and delete	Where included, the system shall permit authorized users to update or delete records and provide confirmation/error feedback.
FR-11 — Reports	Where implemented, the system shall produce summaries or reports from stored agricultural records.
FR-12 — Error handling	The system shall show understandable messages when validation, database, or application operations fail.

6. Non-Functional Requirements
Area	Requirement
Usability	Pages and forms should be understandable to intended users, with clear labels and navigation.
Performance	Common data-entry and retrieval operations should complete in a reasonable time under the expected project workload.
Reliability	The system should handle invalid input and database errors without silently corrupting records.
Data integrity	Required fields, suitable data types, and database constraints should be used where applicable.
Security	Database credentials should not be exposed in public source code; user access controls should match implemented functionality.
Maintainability	Frontend, Java backend, and database responsibilities should be organized so modules can be maintained separately.
Compatibility	The interface should work in the browsers and operating environments selected for project testing.
Backup	Database backup and recovery procedures should be documented if required by deployment.

7. Technology Stack
Area	Technology / notes
Frontend	HTML5 and CSS3 (as specified for the agriculture project).
Backend	Java (the exact framework or runtime should match the actual implementation).
Database	MySQL.
Database administration	A database client such as MySQL Workbench or phpMyAdmin may be used as a management tool; it is not the database server itself.
Development tools	Use the IDE, build tools, and server actually used by the team; fill in exact versions before submission.

8. System Workflow and Diagrams
8.1 Main Workflow
A typical workflow is to open the application, sign in if authentication is implemented, select a module, enter or update agricultural data, validate it, save it through the Java backend into MySQL, and review the saved record or report.
  
                                                            Figure 2. Proposed application workflow.
8.2 Database Entity Relationship Diagram
The following is a conceptual ER diagram for a possible DAMS data model. The final table names, keys, and relationships must be adjusted to match the actual MySQL schema.
 
                                                                 Figure 3. Conceptual ER diagram.
8.3 Data Flow
1.	The user opens the application and selects an available function.
2.	The frontend collects information through a form.
3.	The Java backend validates the input and applies business rules.
4.	Valid data is stored or updated in MySQL.
5.	The backend returns a success message, saved record, or error response.
6.	The frontend displays the result; reports are generated only if that feature is implemented.
9. Database and Data Management
The following tables are conceptual examples for a Digital Agriculture Management System, not a claim about an existing schema. Use the actual table names from the project's database when finalizing this SRS.
Suggested entity/table	Possible data
USERS	user_id, name, contact, login fields/role if authentication is implemented.
FARMS	farm_id, owner/user reference, farm name, location, area.
CROPS	crop_id, farm reference, crop name, season, area, sowing/harvest dates, status.
ACTIVITIES	activity_id, crop/farm reference, activity type, date, notes.
INVENTORY	item_id, farm reference, item name, quantity, unit.
SALES_EXPENSES	record_id, farm reference, record type, date, amount, description.
REPORTS (optional)	report_id, report type, period, creation date, or report metadata.

10. Testing and Challenges
Area	Potential challenge	Verification approach
Forms and validation	Missing or invalid field values.	Test empty required fields, invalid numbers/dates, and valid submissions.
Database operations	Connection errors or failed insert/update/delete.	Test successful operations, database-unavailable behavior, and data persistence after restart.
Record consistency	Duplicate or mismatched farm/crop references.	Check primary keys, foreign keys, required fields, and update/delete behavior.
User interface	Layout problems or unclear error messages.	Test each page at target screen sizes and review success/error states.
Access control (if implemented)	Users may access records beyond their permission.	Test allowed and disallowed actions for each implemented role.
Reports (if implemented)	Summary values may not match stored records.	Compare report totals with known test data.

10.1 Suggested Test Checklist
•	Application opens without runtime errors.
•	Forms display the expected fields and validation messages.
•	Valid records can be saved and retrieved.
•	Updates and deletions behave as intended.
•	Data remains available after restarting the application and database.
•	Invalid inputs and database failures produce understandable messages.
•	Any implemented reports match the underlying stored data.
11. Installation and Usage
Exact installation commands depend on the Java framework, server, and build configuration used in the project. Replace the placeholders below with the actual project setup.
11.1 Prerequisites
•	Java Development Kit version used by the project.
•	MySQL server and a database client.
•	A browser for the frontend.
•	The IDE/build tool and Java web server or framework required by the implementation.
11.2 Database Setup
Start the MySQL server, create a database for the project, and execute the actual schema SQL supplied by the team. Configure the Java application's database URL, username, and password using local configuration. Do not include real passwords in the submitted report or public repository.
11.3 Start the Application
7.	Open the project in the configured IDE or build environment.
8.	Set the database connection values in the project's configuration.
9.	Start the Java backend or web server using the project's actual run configuration.
10.	Open the frontend page or the URL printed by the server.
11.	Enter test data and verify that it is saved and retrieved from MySQL.
11.4 Typical User Workflow
12.	Open the Digital Agriculture Management System.
13.	Sign in if the project includes authentication.
14.	Choose the required module, such as farm or crop records, if implemented.
15.	Enter data and submit the form.
16.	Review the validation result and confirm the saved record.
17.	Open a summary/report if the project includes reporting.
12. Project Directory Structure
The actual directory structure was not included in the supplied agriculture project details. The following is a suggested logical structure and must be edited to match the repository.
digital-agriculture-management-system/
├── frontend/ (HTML, CSS, client-side assets)
├── backend/ (Java source code and configuration)
├── database/ (schema.sql, sample data, database notes)
├── docs/ (SRS, diagrams, test cases, user guide)
└── README.md

13. Module-wise Work Distribution
Member / role	Module	Key deliverables
Member 1 — Frontend	User interface	HTML/CSS pages, forms, navigation, layouts, and front-end validation.
Member 2 — Backend	Java application logic	Request handling, business rules, validation, and frontend/backend integration.
Member 3 — Database	MySQL data layer	Schema, tables, keys, queries, persistence, and consistency checks.
Member 4 — Testing and Integration	Integration and QA	Connect components, test end-to-end workflows, record defects, and verify fixes.
Member 5 — Documentation	Project documentation	SRS, diagrams, setup instructions, test report, and user guide.

14. Development Phases
No verified dated commit history or week-by-week work log for the Digital Agriculture Management System was provided with the source material. The following phases are a proposed planning structure, not a claim that these activities have already been completed.
Phase	Planned work	Expected output
Phase 1 — Requirements	Confirm users, modules, fields, and project boundaries.	Approved requirements and module list.
Phase 2 — UI design	Create page layouts, navigation, and data-entry forms.	Frontend screens and styling.
Phase 3 — Database design	Create tables, keys, relationships, and sample records.	MySQL schema and data model.
Phase 4 — Backend development	Implement Java logic and database operations.	Working backend functions.
Phase 5 — Integration and testing	Connect UI, backend, and database; run test cases.	Integrated and tested workflows.
Phase 6 — Documentation	Finalize diagrams, SRS, setup guide, and report.	Submission-ready documentation.

15. UI Screenshots
Screenshots of the running Digital Agriculture Management System were not provided in the supplied material. Insert authentic screenshots after running the project, for example:
•	Home / Dashboard page
•	Farm or crop entry page (if implemented)
•	Saved records or report page (if implemented)
Do not label placeholder images as actual application screenshots.
16. Future Scope
•	Add weather information integration if required and supported by a reliable data source.
•	Add crop calendar reminders and activity scheduling.
•	Add inventory alerts for low stock.
•	Add reporting and export features for farm activities and financial records.
•	Add secure multi-user access and role permissions if not already present.
•	Add mobile-friendly layouts and language options.
•	Explore sensor/IoT or advisory integrations only after defining their data sources, validation, and limitations.
17. Conclusion
The Digital Agriculture Management System is intended to organize selected agricultural records through an HTML/CSS frontend, Java backend, and MySQL database. This SRS provides a structured requirements baseline, architecture and workflow diagrams, a conceptual data model, test considerations, and documentation guidance. Before submission, the team should replace placeholders and proposed modules with the exact guide name, repository link, team details, database schema, implemented features, and verified screenshots.
Appendix A. Requirements Traceability
Reference point	SRS section
Project title, guide, repository, and team roles	Cover and Team Members
Purpose and scope	Sections 1–2
User categories	Section 3
Architecture and core modules	Section 4
Functional requirements	Section 5
Non-functional requirements	Section 6
Technology stack	Section 7
Workflow and diagrams	Section 8
Database entities	Section 9
Testing and installation	Sections 10–11
Directory structure and team allocation	Sections 12–13
Development phases, screenshots, future scope	Sections 14–16

