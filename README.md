# 💘 Dating Recommendation Engine

This is a Spring Boot-based backend application that powers a **dating recommendation engine**, which suggests the most compatible users based on gender, age, and interests. The system is designed to be extensible and robust, using Java and MySQL for backend and data persistence.

## 🚀 Features

* Match recommendations based on:

  * ✅ Opposite gender preference
  * ✅ Closest age
  * ✅ Common interests
* Clean, modular, and extensible architecture
* Uses **Spring Boot** for backend REST services
* **MySQL** as the database
* Includes unit tests for logic validation
* Easily extendable to include new matching rules or frontend components

---

## 🏗️ Tech Stack

* Java 17+
* Spring Boot
* Spring Data JPA (Hibernate)
* MySQL
* JUnit / Mockito (for unit testing)

---

## 🧠 Matching Logic

The matchmaking engine evaluates potential matches using the following rules, in order of priority:

1. **Gender Rule** – Opposite gender preferred
2. **Age Rule** – Closer age preferred
3. **Interest Rule** – More common interests preferred

---

## 🛠️ How to Run the Application

### ✅ Prerequisites

* Java 17 or higher
* Maven
* MySQL Server

### 📦 Setup Steps

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/dating-app.git
   cd dating-app
   ```

2. **Create a MySQL database:**

   ```sql
   CREATE DATABASE dating_app;
   ```

3. **Configure `application.properties`:**

   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/dating_app
   spring.datasource.username=your_mysql_username
   spring.datasource.password=your_mysql_password
   spring.jpa.hibernate.ddl-auto=update
   ```

4. **Build and run the application:**

   ```bash
   mvn spring-boot:run
   ```

5. **Access the API:**

   * Base URL: `http://localhost:8080`
   * Example endpoint to get top matches:

     ```
     GET /api/users/{userId}/matches?topN=2
     ```

---

## 📂 Project Structure

```
src/
├── main/
│   ├── java/
│   │   └── com.example.datingapp/
│   │       ├── controller/
│   │       ├── service/
│   │       ├── model/
│   │       ├── repository/
│   │       └── DatingAppApplication.java
│   └── resources/
│       ├── application.properties
│       └── data.sql
└── test/
    └── java/
        └── com.example.datingapp/
```

---

## 🧪 Running Tests

Run unit tests with:

```bash
mvn test
```

---

## 🌱 Future Enhancements

* Add web frontend (HTML/CSS/JS or React)
* Add messaging or chat feature
* Integrate caching with Redis
* Use Kafka for matchmaking notifications

---
