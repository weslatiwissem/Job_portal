# 💼 Portail d'Emploi en Ligne

> A full-stack web-based job portal connecting job seekers with recruiters through an intuitive, responsive interface.

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)
![Thymeleaf](https://img.shields.io/badge/Thymeleaf-005F0F?style=for-the-badge&logo=thymeleaf&logoColor=white)

---

## 👥 Authors

| Name |
|------|
| Oueslati Ouissem |
| Sarra Ben Bettaieb |
| Maram Raboudi |

---

## 📖 Overview

This project is a web-based job portal that simplifies the hiring process by connecting **job seekers** and **recruiters** on a single platform. It provides role-based dashboards, job listing management, CV upload, and application tracking — all within a clean, responsive interface.

---

## ✨ Features

### 🔐 Common (All Users)
- User registration, login, and logout
- Profile management

### 👤 Job Seekers
- Browse and search job listings by title and location
- Apply to job offers
- Upload and manage CV
- View application history

### 🏢 Recruiters
- Create, edit, and delete job postings
- View received applications
- Browse candidate profiles

### 🛠️ Administrators
- Manage user accounts
- Validate job listings
- Remove inappropriate content
- Access usage statistics and reports

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| Backend | Java, Spring Boot, Spring MVC, Spring Security |
| Frontend | HTML, CSS, JavaScript, Bootstrap, Thymeleaf |
| Database | MySQL, JPA / Hibernate |
| Auth | BCrypt password encoding, role-based access control |
| File Upload | MultipartFile (profile photo & CV upload) |

---

## 🏗️ Architecture

The application follows a classic **MVC (Model-View-Controller)** architecture:

```
src/
├── config/          # Security config, authentication handlers
├── controllers/     # MVC controllers (dashboard, jobs, profiles)
├── entity/          # JPA entities (Users, JobPostActivity, Profiles...)
├── repository/      # Spring Data JPA repositories
├── services/        # Business logic layer
└── util/            # Utility classes (file upload, etc.)
```

---

## 🔒 Security

- Spring Security with form-based login
- Custom `AuthenticationSuccessHandler` that redirects users by role (`Job Seeker` → `/dashboard/`, `Recruiter` → `/dashboard/`)
- BCrypt password hashing
- CSRF disabled (API-friendly setup)
- Public routes: `/`, `/global-search/**`, `/register/**`, static assets

---

## 🚀 Getting Started

### Prerequisites

- Java 17+
- Maven
- MySQL

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/job-portal.git
   cd job-portal
   ```

2. **Configure the database**

   Edit `src/main/resources/application.properties`:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/job_portal
   spring.datasource.username=your_username
   spring.datasource.password=your_password
   spring.jpa.hibernate.ddl-auto=update
   ```

3. **Run the application**
   ```bash
   mvn spring-boot:run
   ```

4. **Access the app**

   Open your browser at `http://localhost:8080`

---

## 📅 Development Timeline

| Week | Dates | Phase |
|------|-------|-------|
| Week 1 | Apr 21 – Apr 27, 2025 | Requirements analysis & architecture design |
| Week 2 | Apr 28 – May 4, 2025 | Base UI development |
| Week 3 | May 5 – May 11, 2025 | Frontend/backend integration & database |
| Week 4 | May 12 – May 18, 2025 | Testing, bug fixes & performance tuning |
| Week 5 | May 19 – May 25, 2025 | Final deployment & documentation |

---

## 📄 License

This project was developed as part of an academic assignment. All rights reserved by the authors.
