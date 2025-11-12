🤝 Multi-Vendor Management Portal

A Multi-Vendor Management Portal application built with Spring Boot designed to streamline the procurement process. This system facilitates the creation of a vendor base, manages the quotation process, and enables the Company to select the most competitive bid.

✨ Features and Workflow

This application implements a precise procurement workflow managed across three core user roles:

Admin Functionality (Vendor Creation):

Admins are responsible for managing the vendor ecosystem within the portal.

They can create new vendor accounts, including contact details and necessary credentials for login.

Company Functionality (Quotation/RFQ Creation & Acceptance):

The Company user can log in and create a new Request for Quotation (RFQ) for a required product or service.

Upon creation of the quotation, all relevant vendors are automatically notified via email with the details of the RFQ.

The Company user can accept the vendor who quoted the lowest price from the submitted bids.

Vendor Functionality (Price Submission):

Vendors receive the RFQ notification and login to the portal.

They can view the open quotation requests and submit their competitive price/bid against the RFQ item.

Technical Features: Built on Spring Boot for robust backend logic and a clean, responsive front-end framework.

🚀 Getting Started

Follow these steps to set up and run the project on your local machine. You will be using Spring Tool Suite (STS) for development.

📋 Prerequisites

Ensure the following software is installed on your system:

Java Development Kit (JDK) 17+

Apache Maven (for dependency management and building)

MySQL Database (e.g., MySQL Workbench or a similar client)

Key Project Dependencies (Added via STS Initializer):
The project is built using the following core Spring Boot dependencies, which are typically included when creating the project in Spring Tool Suite (STS) or using the Spring Initializr:

Spring Data JPA: Used for interacting with the MySQL database via ORM (Object-Relational Mapping).

Spring Web (MVC): Enables the creation of the web application, handling requests, and defining RESTful endpoints.

MySQL Driver (Connector/J): The JDBC driver necessary to connect the Spring application to the MySQL database.

Spring Boot DevTools: Provides development-time features like automatic application restarts upon code changes.

⚙️ Installation and Setup

1. Database Setup

The first step is to create the necessary database and prepare the schema using MySQL.

Open your MySQL Workbench or command-line client.

Create the required database as specified for this project:

CREATE DATABASE online_vendor;








2. Configuration Update

You need to update the database credentials in the Spring Boot configuration file.

Navigate to the configuration file:

src/main/resources/application.properties








Find the following lines related to MySQL connection and update them to match your local setup. Ensure the database name matches online_vendor.

# Database Configuration Properties
spring.datasource.url=jdbc:mysql://localhost:3306/online_vendor
spring.datasource.username=root
spring.datasource.password=YOUR_MYSQL_PASSWORD_HERE








3. Build and Run

With the database configured, you can now build and launch the application using Spring Tool Suite (STS).

Open Spring Tool Suite (STS):

Import the project as an existing Maven project.

Run the Application:

Right-click the project in the Project Explorer.

Select Run As -> Spring Boot App.

The application will now start, typically accessible at http://localhost:8080 unless configured otherwise.
