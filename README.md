# 🌍 ECOHACKERS

Welcome to EcoHackers! This project is a full-stack web application that integrates a Spring Boot backend with an Angular frontend. 🚀 

## 📋 Table of Contents

- [Technologies Used](#technologies-used)
- [Prerequisites](#prerequisites) 
- [Installation](#installation)
- [Running the Application](#running-the-application)
- [Common Issues](#common-issues)
- [Contributing](#contributing)
- [License](#license)


## 💻 Technologies Used

Backend: Spring Boot 🛠️, Java ☕, Maven
Frontend: Angular ⚡, TypeScript
Database: MySQL 🗄️ (configurable for other databases)

## ✅ Prerequisites

Make sure you have the following installed:

Java JDK (version 17 or higher) ☕
Node.js (version 14 or higher) 🟢
Angular CLI (globally installed) ⚡
Maven (version 3.6 or higher) 🛠️
MySQL (or other relational database) 🗄️

## 🛠️ Installation

### 🗂️ Clone the Repository

bash

git clone https://github.com/adptCode/greensteps.git

### Backend Setup (Spring Boot) ⚙️

Navigate to the backend directory:
bash

cd backend

Install dependencies and build the project:
bash

mvn clean install

Database Configuration:
Edit the file src/main/resources/application.properties to configure your MySQL database:

properties

spring.datasource.url=jdbc:mysql://localhost:3306/your_database_name spring.datasource.username=your_username spring.datasource.password=your_password spring.jpa.hibernate.ddl-auto=update

Run the Spring Boot application:
bash

mvn spring-boot:run

The backend server will start at http://localhost:8080. 

### Frontend Setup (Angular) ⚡

Navigate to the frontend directory:
bash

cd frontend

Install dependencies:
bash

npm install

Run the Angular development server:
bash

ng serve

The frontend will be available at http://localhost:4200. 

### 🌐 Connecting Frontend to Backend

Ensure the frontend API requests point to the backend's server URL in src/environments/environment.ts:

typescript

export const environment = { production: false, apiUrl: 'http://localhost:8080/api' };

## 🚀 Running the Application

Start the Backend:

Follow the steps in Backend Setup.

Start the Frontend:

Follow the steps in Frontend Setup.

Open your browser and navigate to http://localhost:4200.

## ❗ Common Issues

Port Conflicts:

If ports 8080 (backend) or 4200 (frontend) are in use, change the ports:
    Spring Boot: Edit application.properties and change server.port=8081.
    Angular: Run ng serve --port 4201.

CORS Issues:

Ensure CORS is configured in your Spring Boot backend by adding appropriate headers or using @CrossOrigin annotations.

## 🤝 Contributing

Feel free to fork this repository, create a feature branch, and submit a pull request. For major changes, please open an issue to discuss the changes you'd like to make. 📜 License

This project is licensed under the MIT License.
