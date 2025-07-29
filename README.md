# Wisdomize Backend API 🚀

![Node.js](https://img.shields.io/badge/Node.js-18.x-green)
![Express](https://img.shields.io/badge/Express-4.x-lightgrey)
![MySQL](https://img.shields.io/badge/MySQL-8.x-blue)
![JWT](https://img.shields.io/badge/JWT-Auth-orange)

The robust backend API powering the Wisdomize EdTech platform, built with Node.js, Express, and MySQL.

**API Base URL:** [https://wisdomize-backend.onrender.com](https://wisdomize-backend.onrender.com)

## ✨ Features

- **RESTful API** with proper HTTP methods
- **JWT Authentication** with role-based access control
- **MySQL** database integration
- **User roles**: Admin, Instructor, Student
- **Complete course management** system
- **Video content management**
- **Enrollment system**
- **Rating and reviews** functionality
- **CORS management** for frontend integration
- **Input validation** for all endpoints

## 🛠 Tech Stack

**Core:**
- Node.js 18
- Express.js 4
- MySQL 8
- Sequelize ORM

**Security:**
- JSON Web Tokens (JWT)
- Bcrypt password hashing
- CORS middleware
- Environment variables

**API Documentation:**
- Postman Collection

## 📚 API Endpoints

### Authentication
| Method | Endpoint               | Description                |
|--------|------------------------|----------------------------|
| POST   | /api/auth/register     | Register new user          |
| POST   | /api/auth/login        | User login                 |

### Courses
| Method | Endpoint               | Description                |
|--------|------------------------|----------------------------|
| POST   | /api/courses           | Create new course          |
| GET    | /api/courses           | Get all courses            |
| GET    | /api/courses/:id       | Get course by ID           |
| DELETE | /api/courses/:id       | Delete course              |
| GET    | /api/courses/instructor/:email | Get instructor's courses |

### Course Videos
| Method | Endpoint                     | Description                |
|--------|------------------------------|----------------------------|
| POST   | /api/course-videos/add       | Add video to course        |
| PUT    | /api/course-videos/update    | Update video details       |
| DELETE | /api/course-videos/delete    | Remove video               |
| GET    | /api/course-videos/:courseId | Get videos for course      |

### Categories (Admin)
| Method | Endpoint               | Description                |
|--------|------------------------|----------------------------|
| POST   | /api/categories/       | Create new category        |
| GET    | /api/categories        | Get all categories         |
| DELETE | /api/categories/delete | Delete category            |

### Enrollment
| Method | Endpoint               | Description                |
|--------|------------------------|----------------------------|
| POST   | /api/enrollment/       | Enroll in course           |
| GET    | /api/enrollment/:email | Get user's enrollments     |

### User Management
| Method | Endpoint               | Description                |
|--------|------------------------|----------------------------|
| GET    | /api/users/:email      | Get user info              |
| PUT    | /api/users/:email      | Update user profile        |

### Ratings & Reviews
| Method | Endpoint               | Description                |
|--------|------------------------|----------------------------|
| POST   | /api/reviews           | Submit review              |
| GET    | /api/reviews/:courseId | Get course reviews         |
| PUT    | /api/reviews/update    | Update review              |
| DELETE | /api/reviews/delete/:courseId/:email | Delete review |

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- MySQL 8+
- npm 8+

### Installation

1. Clone the repository:
```bash
git clone https://github.com/Nandeesh-nh/wisdomize_backend.git
cd wisdomize_backend
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file:
```env
PORT=5000
DB_HOST=localhost
DB_USER=your_mysql_username
DB_PASSWORD=your_mysql_password
DB_NAME=wisdomize
JWT_SECRET=your_jwt_secret_here
JWT_EXPIRE=30d
```

4. Start development server:
```bash
npm run dev
```

The API will run on [http://localhost:5000](http://localhost:5000)

## 🗄 Database Setup

1. Create MySQL database:
```sql
CREATE DATABASE wisdomize;
```

2. The Sequelize models will automatically create tables on first run.

## 📝 API Documentation

[![Run in Postman](https://run.pstmn.io/button.svg)](https://documenter.getpostman.com/view/your-postman-docs-link)

Full Postman collection available with all request examples.

## 🏗 Deployment

The backend is deployed on Render as a web service:

1. Set build command: `npm install`
2. Set start command: `node src/server.js`
3. Configure MySQL connection in environment variables

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
