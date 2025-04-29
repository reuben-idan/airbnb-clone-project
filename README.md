# Airbnb Clone Project

## 📘 Project Overview

The Airbnb Clone Project is a full-stack web application inspired by Airbnb. It aims to replicate a booking platform where users can list, browse, and book accommodations. This project is designed to strengthen your backend development skills, database modeling, API design, application security, and deployment automation using CI/CD pipelines.

### 🎯 Project Goals

- Simulate a real-world team development workflow.
- Understand scalable backend system design.
- Implement security-first APIs.
- Practice version control and continuous delivery.

---

## 👥 Team Roles

### Backend Developer
Responsible for building server-side logic, implementing REST/GraphQL APIs, integrating databases, and handling core application functionality.

### Database Administrator (DBA)
Designs and maintains the relational database structure, optimizes queries, and ensures data consistency and security.

### DevOps Engineer
Handles containerization, builds CI/CD pipelines, manages deployments, and ensures uptime, scalability, and rollback support.

### Technical Writer
Documents system architecture, APIs, database schemas, and features for both internal teams and external users.

### Project Manager
Coordinates the team, defines deliverables and deadlines, and ensures smooth collaboration and task execution.

---

## 🧰 Technology Stack

| Technology     | Purpose                                                                          |
|----------------|----------------------------------------------------------------------------------|
| **Django**     | Web framework used to develop APIs and manage backend logic                      |
| **MySQL**      | Relational database for storing user, property, booking, and payment data        |
| **GraphQL**    | API layer for efficient data fetching and manipulation                           |
| **Docker**     | Containerizes the app for consistent dev, test, and production environments      |
| **GitHub Actions** | Automates testing, builds, and deployment pipelines                         |
| **Markdown**   | Used for writing structured documentation (README, team roles, etc.)             |

---

## 🗃️ Database Design

### Key Entities and Sample Fields

1. **Users**
   - id
   - name
   - email
   - password_hash
   - role (guest/host)

2. **Properties**
   - id
   - owner_id (FK to Users)
   - title
   - location
   - price_per_night

3. **Bookings**
   - id
   - property_id (FK to Properties)
   - user_id (FK to Users)
   - start_date
   - end_date

4. **Reviews**
   - id
   - user_id (FK to Users)
   - property_id (FK to Properties)
   - rating
   - comment

5. **Payments**
   - id
   - booking_id (FK to Bookings)
   - amount
   - status
   - payment_method

### Relationships

- A user can own multiple properties.
- A property can have multiple bookings and reviews.
- A booking is linked to a user and a property.
- A payment is associated with a specific booking.

---

## ✨ Feature Breakdown

### User Management
Handles user registration, authentication, profile updates, and user roles (host or guest).

### Property Management
Allows hosts to list properties with images, pricing, and availability, and to update or delete listings.

### Booking System
Enables guests to search, filter, and book properties with date availability and pricing validation.

### Review System
Guests can leave feedback and ratings after their stay, helping build trust and quality.

### Payment Integration
Processes secure transactions for bookings and tracks payment status.

### Admin Dashboard
Provides management views for monitoring users, listings, and financial metrics.

---

## 🔐 API Security

### Key Measures

- **Authentication**: Use of JWT to verify identity.
- **Authorization**: Role-based permissions to restrict access (e.g., only hosts can add properties).
- **Rate Limiting**: Prevents abuse by limiting API calls per user/IP.
- **Input Validation & Sanitization**: Prevents injection and malformed request attacks.
- **HTTPS Enforcement**: Ensures data is encrypted in transit.

### Why Security Matters

- **Protecting User Data**: Prevent data leaks and unauthorized access to personal information.
- **Securing Payments**: Ensures financial transactions are encrypted and tamper-proof.
- **System Stability**: Avoids API abuse that could lead to crashes or denial-of-service.

---

## ⚙️ CI/CD Pipeline

### What is CI/CD?
CI/CD stands for Continuous Integration and Continuous Deployment. It automates the software release process from code push to deployment.

### Why It’s Important
- Reduces human error in deployment.
- Ensures rapid feedback and quick delivery.
- Enables agile practices and faster product updates.

### Tools Used
- **GitHub Actions**: Directly integrated with the GitHub repository, allowing for the creation of automated workflows for building, testing, and deploying the application.
- **Docker**: Used to containerize the application, ensuring consistent environments across the CI/CD pipeline.

---



