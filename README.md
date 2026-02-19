# Node.js & PostgreSQL Backend Project

📌 Overview
This repository contains the backend of a Movie Ticket Booking System developed using Node.js, Express.js, and PostgreSQL.
The project focuses on building a scalable, high-performance backend system that manages movies, theatres, shows, users, and seat bookings while efficiently handling concurrent booking requests.
The backend exposes secure RESTful APIs used by the frontend application to perform authentication, movie listing, show management, and real-time seat booking.

## 🎯 Objectives
-Build a scalable movie ticket booking backend using Node.js
-Design a relational database schema for movies, theatres, shows, users, and bookings
-Implement secure RESTful APIs with full CRUD functionality
-Handle concurrent seat booking requests safely
-Prevent double-booking and maintain data consistency
-Optimize performance for high user traffic

## 🛠️ Tech Stack
-Backend: Node.js, Express.js
-Database: PostgreSQL
-Authentication: JWT (JSON Web Token)
-Concurrency Handling: Event-driven architecture, asynchronous I/O
-Database Client: pg (PostgreSQL client with connection pooling)
-Environment Management: dotenv
-API Type: RESTful APIs

## ⚙️ Features
✅ User Registration & Login (JWT Authentication)
✅ Movie listing API
✅ Theatre & show management
✅ Seat selection & booking system
✅ Booking history for users
✅ Secure payment-ready backend structure
✅ PostgreSQL relational schema design
✅ Proper validation & structured error handling
✅ Modular and scalable folder architecture

**Core modules**
-Users – Registration, Login, Authentication
-Movies – Add/View/Delete movies
-Theatres – Manage theatre details
-Shows – Show timings & seat availability
-Bookings – Seat booking & transaction handling

**🔄 Concurrency & Performance Handling**
Since seat booking systems are highly concurrent systems, the backend implements:
⚡ Node.js non-blocking I/O to process multiple requests simultaneously
🔁 PostgreSQL connection pooling for efficient DB usage
🔒 Database transactions to prevent double seat booking
🧠 Row-level locking (SELECT ... FOR UPDATE) to avoid race conditions
🚀 Optimized queries for faster response time under heavy load
This ensures:
-No two users can book the same seat at the same time
-Data consistency during simultaneous booking attempts
-Reliable performance during peak traffic

**🗄️ Database Design (PostgreSQL)**

-Main Tables:
users
movies
theatres
shows
seats
bookings

-Relationships:
One Movie → Many Shows
One Theatre → Many Shows
One Show → Many Seats
One User → Many Bookings
