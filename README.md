#  StudyNotion - Full Stack EdTech Platform

**StudyNotion** is a fully functional **EdTech platform** that enables users to **create**, **consume**, and **rate educational content**.  
It’s built using the **MERN Stack** — **MongoDB**, **Express.js**, **React.js**, and **Node.js**.

---

##  Project Description

**StudyNotion** aims to:

-  Provide a **seamless and interactive learning experience** for students, making education more engaging and accessible.
-  Offer a **platform for instructors** to showcase their expertise and connect with learners across the globe.

The platform features complete functionality across front-end, back-end, and database layers — from course creation and enrollment to payment and media management.

---

##  System Architecture

The platform follows a **client-server architecture**, consisting of:

- **Front-end (React.js)** – The user-facing interface for students and instructors.  
- **Back-end (Node.js + Express.js)** – Handles API requests, authentication, and business logic.  
- **Database (MongoDB)** – Stores users, courses, and media-related data.


##  Front-end

The front end is built with **React.js**, using **Redux** for state management and **Tailwind CSS** for responsive UI design.  
It communicates with the backend via **RESTful API calls**.

###  For Students
- **Homepage:** Overview and navigation links.  
- **Course List:** Displays all courses with details and ratings.  
- **Wishlist:** Saved courses for later.  
- **Cart & Checkout:** Secure course purchase flow with payment integration.  
- **Course Content:** Displays videos and materials for enrolled courses.  
- **User Profile:** View and edit personal information.

###  For Instructors
- **Dashboard:** Overview of created courses, feedback, and ratings.  
- **Insights:** Detailed analytics (views, clicks, enrollments).  
- **Course Management:** Create, update, or delete courses and manage pricing/content.  
- **Profile Management:** Edit instructor details and media.

###  For Admin *(Future Scope)*
- **Dashboard:** Overview of platform metrics (users, instructors, revenue).  
- **Instructor Management:** Manage instructors and their courses.  
- **User & Course Management:** Administrative tools for platform moderation.  

>  **Tech Used:** React.js, Redux, Tailwind CSS, SwiperJS, React Icons

---

##  Back-end

The backend follows a **monolithic architecture**, built with **Node.js** and **Express.js**, and connected to **MongoDB** via **Mongoose**.

###  Key Features

- **User Authentication & Authorization**  
  - Secure signup/login using **JWT** and **Bcrypt** for password hashing.  
  - Includes **OTP verification** and **Forgot Password** functionality.  

-  **Course Management**  
  - CRUD operations for courses.  
  - Students can rate and review courses.  

-  **Payment Integration**  
  - Integrated **Razorpay** for secure payments and enrollment.  

-  **Cloud-based Media Management**  
  - Uses **Cloudinary** for storing and delivering images, videos, and documents.  

- **Markdown Content Support**  
  - Course content stored and rendered using **Markdown** for flexibility.

---

### 🧩 Frameworks, Libraries & Tools

| Category | Technology |
|-----------|-------------|
| Backend Framework | **Node.js**, **Express.js** |
| Database | **MongoDB**, **Mongoose** |
| Authentication | **JWT**, **Bcrypt** |
| Media Storage | **Cloudinary** |
| Payment Gateway | **Razorpay** |
| Mail Service | **NodeMailer** |

---



##  API Design

The backend API is designed using **RESTful principles**.  
It exchanges data in **JSON** format and uses standard HTTP methods (`GET`, `POST`, `PUT`, `DELETE`).

###  Sample API Endpoints

| Method | Endpoint | Description |
|--------|-----------|-------------|
| **POST** | `/api/auth/signup` | Create a new user (student/instructor) |
| **POST** | `/api/auth/login` | Authenticate user & generate JWT |
| **POST** | `/api/auth/verify-otp` | Verify OTP sent to registered email |
| **POST** | `/api/auth/forgot-password` | Send password reset link |
| **GET** | `/api/courses` | Get list of all available courses |
| **GET** | `/api/courses/:id` | Get course details by ID |
| **POST** | `/api/courses` | Create a new course (instructor only) |
| **PUT** | `/api/courses/:id` | Update a course |
| **DELETE** | `/api/courses/:id` | Delete a course |
| **POST** | `/api/courses/:id/rate` | Rate a course |
