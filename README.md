---

# Cloud Enabled Deployment In Action with AWS/GCP

This repository contains four projects that together form a cloud-enabled application. It includes three Spring Boot backend microservices and a React frontend.

---

## 🚀 Getting Started

To run this project, you will need **Java 21**, **Maven**, and **Node.js with npm** installed.

---

## 1. Backend Services

The backend consists of three separate Spring Boot microservices. Each service can be built and run independently.

* **course-service** – Manages courses using a MySQL database.
* **student-service** – Manages students using a MongoDB database.
* **media-service** – Manages file uploads and retrieval with local disk storage.

### Configuration

Before running, configure the database connections in the respective `application.properties` files for the **course-service** and **student-service**.

### Building and Running

From the repository’s root directory:

```bash
mvn clean package -DskipTests
```

After the build completes, run each service from its respective directory:

```bash
# Example: Running the student-service
cd student-service
java -jar target/student-service-0.0.1-SNAPSHOT.jar
```

---

## 2. Frontend Application

The frontend is a React application built with TypeScript.

### Building and Running

Navigate to the `frontend-app` directory:

```bash
# Install dependencies
npm install

# Start the development server
npm run dev
```

The application will be accessible at **[http://localhost:3000](http://localhost:3000)** (or another port specified by Vite).

---

## 🧩 Project Breakdown

| Service             | Description                                                                                          | Technology                   | Port |
| ------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------- | ---- |
| **course-service**  | Manages all course-related data. Uses MySQL with Spring Data JPA/Hibernate. Provides REST CRUD APIs. | Spring Boot, Maven, MySQL    | 8081 |
| **student-service** | Manages student information. Uses MongoDB with Spring Data MongoDB. Provides REST APIs.              | Spring Boot, Maven, MongoDB  | 8082 |
| **media-service**   | Handles media tasks like file uploads/retrieval. Uses local file storage (extendable to AWS S3).     | Spring Boot, Maven, Local FS | 8083 |

---

## 🎥 Video Demonstrations

* **Deployment to AWS** – Add video link here
* **Deployment to GCP** – Add video link here

---

## 📜 License

This project is licensed under the [MIT License](link-to-MIT-License).

---

Would you like me to also **add instructions for deploying these services to AWS (ECS, EC2, or Elastic Beanstalk)** in the README? (I can create a ready-to-paste section.)
