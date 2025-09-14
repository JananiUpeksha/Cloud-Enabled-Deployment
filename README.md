Cloud Enabled Deployment In Action with AWS
This repository contains four projects that together form a cloud-enabled application. It includes three Spring Boot backend microservices and a React frontend.

🚀 Getting Started
To run this project, you will need Java 21, Maven, and Node.js with npm installed.

1. Backend Services
The backend consists of three separate Spring Boot microservices. Each service can be built and run independently.

course-service: Manages courses using a MySQL database.

student-service: Manages students using a MongoDB database.

media-service: Manages file uploads and retrieval, with local disk storage.

Configuration
Before running, you must configure the database connections in the respective application.properties files for the course-service and student-service.

Building and Running
Navigate to the repository's root directory and run the following Maven command to build all three services:

mvn clean package -DskipTests

After the build is complete, you can run each service from its respective directory:

# Example: Running the student-service
cd student-service
java -jar target/student-service-0.0.1-SNAPSHOT.jar

2. Frontend Application
The frontend is a React application built with TypeScript.

Building and Running
Navigate to the frontend-app directory.

# Install dependencies
npm install

# Start the development server
npm run dev

The application will be accessible at http://localhost:8080 (or another port specified by Vite).

🧩 Project Breakdown
course-service
Description: This Spring Boot microservice is responsible for managing all course-related data. It uses MySQL as its database, relying on Spring Data JPA and Hibernate for data persistence. It provides standard REST API endpoints to perform CRUD (Create, Read, Update, Delete) operations on course entities.

Technology: Spring Boot, Maven, MySQL

Port: 8081

student-service
Description: This is a Spring Boot microservice dedicated to managing student information. It uses a MongoDB database for data storage, leveraging Spring Data MongoDB for its repository and document-handling features. It exposes REST API endpoints for managing student documents.

Technology: Spring Boot, Maven, MongoDB

Port: 8082

media-service
Description: This service handles all media-related tasks, such as file uploads and retrieval. It is a Spring Boot service that, by default, uses the local file system to store media. This can be easily extended to a cloud-based solution like AWS S3 or MinIO.

Technology: Spring Boot, Maven, Local File Storage

Port: 8083

🎥 Video Demonstrations
Deployment to AWS
Add video link for AWS deployment here.

Deployment to GCP
Add video link for GCP deployment here.

📜 License
This project is licensed under the MIT License.

Link to MIT License
