# City Tram Conveyance Management System

## Overview

The City Tram Conveyance Management System is a comprehensive database solution designed to efficiently manage all aspects of a city's tram service. This centralized database stores, organizes, and maintains critical data related to tram routes, passengers, tickets, and drivers associated with the tram service.

## Features

- Centralized storage and management of tram-related data.
- Data-driven insights for optimizing tram operations.
- Enhanced customer experience through efficient scheduling and clear routes.
- Cost conservation through automated billing and fare optimization.
- Robust data security measures to protect user and system data.
- Scalability to support the growth of the tram company and adapt to changing city dynamics.

## Business Problems Addressed

Through this database system, we aim to address the following business problems:

- **Integrate All Tram-Related Information:** Consolidate all tram-related information in one place, making it easy for staff and passengers to find and interpret the respective requirements.

- **Data-Driven Insights:** Provide both historical and real-time data to derive significant insights related to customer usage, tram performance, and staff reviews.

- **Enhanced Commuter Experience:** Assist tram staff in being punctual and ensure user engagement is user-friendly, enhancing the commuters' experience.

- **Efficient Digital Operations:** Keep processes digital and well-organized, implementing automated paperless billing and mediating value-for-money rides from passengers as well as the company's perspective.

- **Data Security:** Prioritize the protection of user and travel-associated data, ensuring only authorized personnel have access.

- **Adaptability:** Form an adaptable system that can accommodate the changing dynamics of the city to support the tram company's growth and future alterations.

## SQL Scripts

You can find the following SQL scripts in this repository:

- [P4 Insert Statements.sql](P4%20Insert%20Statements.sql): SQL script for inserting data into the database.

- [P4 Non Clustered Indexes.sql](P4%20Non%20Clustered%20Indexes.sql): SQL script for creating non-clustered indexes.

- [P4 Stored Procedures.sql](P4%20Stored%20Procedures.sql): SQL script containing stored procedures for database operations.

- [P4 Table Level Check Constraints.sql](P4%20Table%20Level%20Check%20Constraints.sql): SQL script for defining table-level check constraints.

- [P4 User Defined Function.sql](P4%20User%20Defined%20Function.sql): SQL script for creating user-defined functions.

- [P4 Views.sql](P4%20Views.sql): SQL script for defining database views.

- [P4 Column Data Encryption.sql](P4%20Column%20Data%20Encryption.sql): SQL script for encrypting column data.

- [P4 DDL Statements.sql](P4%20DDL%20Statements.sql): SQL script containing database schema definition statements.

- [P4 DML Trigger.sql](P4%20DML%20Trigger.sql): SQL script for defining data manipulation language (DML) triggers.

Please refer to these scripts for database setup, data manipulation, and additional database features.

## Data Visualization

We have also provided data visualization files to help you analyze and understand the data. You can find the following visualization files:

- [Visualization.pdf](Data%20Visualization/Visualization.pdf): A PDF document containing data visualizations created using Power BI.

- [Visualization.pbix](Data%20Visualization/Visualization.pbix): A Power BI Desktop file that allows you to interact with and explore the data visualizations.

  ![image](https://github.com/sanalpillai/City-Tram-Conveyance-Management-System/assets/30967322/7f533983-3861-4480-8d7e-f554411b0d6a)

Please use these files to gain insights from the data in a visual format.

## GUI Application

We have developed a Python GUI application that provides CRUD (Create, Read, Update, Delete) database functions for the following tables:

- [mainscreen.py](GUI/mainscreen.py): Main screen of the GUI application.

- [passenger.py](GUI/passenger.py): GUI for managing passenger data.

- [route.py](GUI/route.py): GUI for managing tram route data.

- [tram.py](GUI/tram.py): GUI for managing tram data.

- [locality.py](GUI/locality.py): GUI for managing locality data.

These GUI files allow for easy interaction with the database and performing essential operations on passenger, route, tram, and locality data.

## Entities

| Sr No. | Entity Description |
| --- | --- |
| 1 | Tram |
| 2 | Route |
| 3 | Driver |
| 4 | Locality |
| 5 | Maintenance |
| 6 | Accident |
| 7 | Tracking |
| 8 | Feedback |
| 9 | Ticket |
| 10 | Passenger |
| 11 | Booking Detail |
| 12 | Schedule |

## Cardinalities

- Tram to Route: Many to Many (M:N)
- Tram to Driver: Many to One (M:1)
- Tram to Schedule: One to Many (1:M)
- Tram to Maintenance: One to Many (1:M)
- Tram to Accident: One to Many (1:M)
- Route to Schedule: One to Many (1:M)
- Route to Locality: Many to Many (M:N)
- Route to Ticket: One to Many (1:M)
- Ticket to Feedback: One to One (1:1)
- Ticket to Booking Detail: One to One (1:1)
- Ticket to Passenger: One to Many (1:M)

## Business Rules

- A locality is associated with multiple routes, and one route can pass through multiple localities.
- A tram can provide services through multiple routes, and a distinct route can have multiple trams traveling through it.
- A driver can be assigned to drive multiple trams, and a distinct tram can be driven by only one driver.
- A tram undergoes multiple maintenance checks, but a distinct maintenance check is associated with only one tram.
- A tram can be involved in multiple accidents, but a distinct accident can be associated with only one tram.
- A tram can have multiple schedules, but a distinct schedule is always associated with one tram only.
- A passenger can purchase multiple tickets, but a unique ticket is assigned to only one passenger.
- A ticket is always assigned one feedback from the passenger traveling on it, and any unique feedback is associated with only one ticket.
- A ticket has one booking detail, and one distinct booking reference is associated with only one ticket.
- A route can have multiple schedules, but a distinct schedule is associated with only one route.
- A route can have multiple tickets bought by passengers, but a ticket is bought only for one specific route.

## Design Decisions

We have made the following design decisions based on the entities mentioned in the ER diagram:

- **Locality:** To represent different geographical areas or zones, providing clarity to the tram routes and allowing adaptability to changing routes in the future.

- **Route:** To provide critical information about how different localities connect, distance, and transit time, which is essential for passengers and scheduling.

- **Driver:** To keep track of driver assignments, contact details, and license information, allowing flexibility in driver-tram assignments.

- **Tram:** At the core of the system, this entity tracks tram-specific schedules, accident data, maintenance history, and routes.

- **Passenger:** To track passengers using tram services for ticketing, feedback, and communication.

- **Booking Details & Feedback:** To streamline the passenger's journey and ensure accurate feedback and payment tracking.

- **Ticket:** To track passenger journeys, feedback, and monetary transactions.

- **Maintenance & Accident:** To ensure the safety and operational efficiency of trams.

- **Schedule:** To manage tram departure and arrival times.

- **Tracking:** To provide real-time details about tram journeys.

## Enhanced Entity Relationship (EER) Model

![P3 Final ERD](https://github.com/sanalpillai/City-Tram-Conveyance-Management-System/assets/30967322/fb23b519-f305-4cde-acd7-67fc2473391b)

## How to Run

To run the City Tram Conveyance Management System, follow these steps:

1. Clone this repository to your local machine.
2. Set up a database system (e.g., MySQL) and execute the provided SQL scripts to create the database schema.
3. Configure the database connection settings in the Python GUI application files (`mainscreen.py`, `passenger.py`, `route.py`, `tram.py`, `locality.py`).
4. Run the Python GUI application to interact with the database and perform CRUD operations on passenger, route, tram, and locality data.

## Dependencies

The system has the following dependencies:

- Database system (e.g., MySQL, SQL Server Management Studio (SSMS))
- Python for the GUI application

## Contributions

Contributors to this project:

- Sanal Pillai
- Siddharth Pawar
- Sriram Venkatesh
- Ramy Solanki
- Rishabh Patel

## License

This project is licensed under the [MIT License](LICENSE).

