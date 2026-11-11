# Team Task Manager

A full-stack MERN application designed to simplify team collaboration, project organization, and task tracking. The application provides role-based access control, allowing administrators to manage projects and tasks while team members can view and update their assigned work.

## Live Demo

- **Frontend:** https://team-task-manager-client-olive.vercel.app
- **Backend API:** https://team-task-manager-server-azgz.onrender.com

## Features

### Authentication & Security
- User registration and login
- JWT-based authentication
- Secure password hashing using bcrypt
- Protected routes
- Role-based access control (RBAC)

### Project Management
- Create, view, edit, and delete projects
- Add team members to projects
- View project members
- Manage project activities

### Task Management
- Create and assign tasks to team members
- Edit and delete tasks
- Update task status
- Filter tasks based on status
- Identify overdue tasks

### Role-Based Access Control

**Admin**
- Create, edit, and delete projects
- Add team members
- Create, assign, edit, and delete tasks
- View dashboard analytics
- Manage project activities

**Member**
- View assigned tasks
- Update task status
- Track assigned work and progress

### Dashboard
- Total tasks
- Completed tasks
- Pending tasks
- In-progress tasks
- Overdue tasks

## Tech Stack

| Category | Technologies |
|---|---|
| Frontend | React.js, Vite |
| Styling | Tailwind CSS |
| Backend | Node.js, Express.js |
| Database | MongoDB Atlas, Mongoose |
| Authentication | JWT, bcryptjs |
| API Communication | Axios, REST APIs |
| Routing | React Router |
| Deployment | Vercel, Render |

## Project Structure

```text
team-task-manager/
│
├── client/
│   ├── public/
│   └── src/
│       ├── components/
│       ├── context/
│       ├── pages/
│       ├── services/
│       ├── App.jsx
│       └── main.jsx
│
├── server/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   └── server.js
│
├── .gitignore
└── README.md
```

## Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/chandana191300/team-task-manager.git
cd team-task-manager
```

### 2. Backend Setup

```bash
cd server
npm install
```

Create a `.env` file inside the server folder:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
```

Start the backend:

```bash
npm run dev
```

The backend runs at:

`http://localhost:5000`

### 3. Frontend Setup

Open another terminal:

```bash
cd client
npm install
```

Create a `.env` file inside the client folder:

```env
VITE_API_URL=http://localhost:5000/api
```

Start the frontend:

```bash
npm run dev
```

Open the local URL displayed by Vite in your browser.

## API Endpoints

### Authentication

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/auth/signup` | Register a user |
| POST | `/api/auth/login` | Login |

### Projects

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/projects` | Get projects |
| POST | `/api/projects` | Create project |
| PUT | `/api/projects/:projectId` | Update project |
| DELETE | `/api/projects/:projectId` | Delete project |
| PUT | `/api/projects/:projectId/add-member` | Add member |

### Tasks

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/tasks` | Get tasks |
| POST | `/api/tasks` | Create task |
| PUT | `/api/tasks/:taskId` | Update task |
| DELETE | `/api/tasks/:taskId` | Delete task |
| PUT | `/api/tasks/:taskId/status` | Update task status |
| GET | `/api/tasks/dashboard/stats` | Get dashboard statistics |

## Environment Variables

Keep all environment variables and database credentials private. Never commit `.env` files to GitHub.

## Future Enhancements

- Real-time notifications
- Kanban board
- Team chat functionality
- File attachments
- Activity tracking

## Repository

GitHub: https://github.com/chandana191300/team-task-manager