# 🎓 Student Management System

Modern full-stack web application for managing students and courses with an intuitive dashboard.

## ✨ Features

- **Dashboard** - Real-time stats and student overview
- **Student Management** - CRUD operations with live search
- **Course Management** - Create and manage courses
- **Responsive Design** - Works on all devices
- **Health Monitoring** - Built-in system health checks

## 🚀 Quick Start

### Prerequisites
- Node.js (v14+)
- MongoDB
- npm

### Installation

1. **Clone & Install**
   ```bash
   git clone <repo-url>
   cd student-management-system
   npm install
   ```

2. **Environment Setup**
   Create `.env` file:
   ```env
   MONGODB_URI=mongodb://localhost:27017/student-management-app
   PORT=3000
   ```

3. **Start MongoDB**
   ```bash
   # Windows
   mongod
   
   # macOS
   brew services start mongodb-community
   
   # Linux
   sudo systemctl start mongod
   ```

4. **Run the Server**
   ```bash
   node server.js
   ```

5. **Access App**
   Open: `http://localhost:3000`

## 🛠 Tech Stack

**Frontend:** HTML5, CSS3, Vanilla JavaScript, Font Awesome  
**Backend:** Node.js, Express.js, MongoDB, Mongoose  
**Tools:** Winston (logging), Morgan (HTTP logs), CORS

## 📡 Key API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/students` | Get all students |
| POST | `/api/students` | Create student |
| GET | `/api/courses` | Get all courses |
| POST | `/api/courses` | Create course |
| GET | `/api/dashboard/stats` | Dashboard data |
| GET | `/health` | Health check |

## 📋 Usage

1. **Add Courses First** - Navigate to Courses → Add Course
2. **Add Students** - Go to Students → Add Student (requires active courses)
3. **Search** - Use the search bar to find students
4. **Dashboard** - View statistics and recent activity

## 🔧 Troubleshooting

**Connection Refused Error?**
- Start the backend server: `node server.js`
- Ensure MongoDB is running
- Check `http://localhost:3000/health`

**Can't Delete Course?**
- Remove enrolled students first
- Courses with students can't be deleted

## 📊 Project Structure

```
├── public/index.html    # Frontend
├── server.js           # Backend
├── package.json        # Dependencies
├── .env               # Config
└── README.md          # This file
```

## 🧪 Development

```bash
# Dev mode with auto-restart
npm install -g nodemon
nodemon server.js
```

---

**Need Help?** Check the health endpoint at `/health` or review server logs for debugging.
