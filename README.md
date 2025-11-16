

# DevOps2 – Spring Boot + Docker + Nginx Deployment

This project demonstrates a production-ready deployment of a Spring Boot web application using **Docker**, **Nginx**, and **Maven**, following DevOps best practices for containerization and lightweight service orchestration.

It includes a reverse proxy setup, SQL initialization script, and a modular deployment structure designed for portability and scalability.

---

## Features

* **Spring Boot backend** (Java)
* **Dockerized application** for reproducible builds
* **Nginx reverse proxy** (port 80 → app on 8080)
* **SQL initialization** via `sql.txt`
* **Maven build lifecycle** for clean packaging
* **Lightweight, cloud-ready deployment architecture**

---

## Tech Stack

| Layer                 | Technology                    |
| --------------------- | ----------------------------- |
| **Backend**           | Java, Spring Boot             |
| **Build System**      | Maven                         |
| **Containerization**  | Docker                        |
| **Reverse Proxy**     | Nginx                         |
| **Database Setup**    | SQL initialization script     |
| **Deployment Target** | Linux server / cloud instance |

---

## ⚙️ How to Run

### 1️⃣ Build the application

```bash
mvn clean package
```

### 2️⃣ Build Docker image

```bash
docker build -t devops2-app .
```

### 3️⃣ Run application container

```bash
docker run -p 8080:8080 devops2-app
```

### 4️⃣ Run Nginx reverse proxy

```bash
docker run -p 80:80 \
  -v $(pwd)/nginx.conf:/etc/nginx/nginx.conf:ro \
  nginx
```

Application is now reachable at:

```
http://localhost
```

---

## Purpose

This project showcases:

* DevOps fundamentals
* Containerization best practices
* Reverse proxy configuration
* Backend deployment workflow
* Cloud-ready and portable application architecture

Ideal for demonstrating DevOps engineering and backend deployment skills.


