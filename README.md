# Practical 6: Connecting React Frontend to Express Backend (Full-Stack Integration)

**Course**: Advanced Web Development Frameworks (ITUE301)  
**Student**: Bhavya Durgani &bull; **Roll No**: D25CS112  
**Department**: CSE - CSPIT, CHARUSAT  

---

## 📌 Overview
This project (`prac6`) demonstrates complete **full-stack integration** by connecting a **React (Vite)** Single Page Application with an **Express.js / MongoDB** REST API. It showcases Cross-Origin Resource Sharing (CORS) configuration, asynchronous HTTP client requests via `fetch`, responsive task management state handling, and seamless end-to-end CRUD persistence.

### Architecture Overview:
- **Backend (`/backend`)**:
  - Express.js running on `http://localhost:5000`.
  - CORS middleware enabled (`cors()`) to allow requests from the React origin.
  - MongoDB connection (`mongodb://127.0.0.1:27017/taskdb`).
  - REST endpoints: `GET /tasks`, `POST /tasks`, `PUT /tasks/:id`, `DELETE /tasks/:id`.
- **Frontend (`/task-manager-frontend`)**:
  - React (Vite) running on `http://localhost:5173`.
  - Task creation form with title and description inputs.
  - Live task listing with status indicators (Pending / Completed).
  - Inline status toggle and task deletion actions.
  - Real-time feedback banners (loading spinners, success alerts, and error banners).

---

## 🚀 Steps to Run

Practical 6 contains both a backend server and a frontend client. Follow these steps to run both concurrently:

### 1. Ensure MongoDB is Running
Make sure MongoDB is active on your machine:
```bash
mongod
```

### 2. Start the Backend Server (Terminal 1)
Open a new terminal window:
```bash
cd prac6/backend
npm install
npm start
```
* Backend starts at: `http://localhost:5000`
* Console confirms:
  ```text
  MongoDB connected successfully
  Server running at http://localhost:5000
  ```

### 3. Start the React Frontend (Terminal 2)
Open a second terminal window:
```bash
cd prac6/task-manager-frontend
npm install
npm run dev
```
* Frontend starts at: `http://localhost:5173`
* Open `http://localhost:5173` in your web browser.

---

## 📸 Screenshots to Include in Lab File / Report

Capture and paste the following screenshots into your practical document:

1. **Screenshot 1 - Dual Terminal Startup (Backend + Frontend)**:
   - *Capture*: Two terminal windows side-by-side:
     - Left: Backend running `npm start` on port 5000 with `MongoDB connected successfully`.
     - Right: Frontend running `npm run dev` with Vite ready on `http://localhost:5173`.
2. **Screenshot 2 - Task Manager UI Initial Load**:
   - *Capture*: Browser window at `http://localhost:5173` showing the clean Task Manager interface, the input form ("Add New Task"), and initial list of tasks retrieved from MongoDB.
3. **Screenshot 3 - Adding a New Task via Frontend**:
   - *Capture*: Filling in the task form (e.g. Title: "Prepare AWDF Practical 6 Report", Description: "Document full-stack integration") and clicking "Add Task", showing the newly added task appearing dynamically in the list.
4. **Screenshot 4 - Toggling Task Completion Status**:
   - *Capture*: Clicking the checkbox or "Mark as Completed" button on a task, showing the status update from "Pending" to "Completed" with green badge or strikethrough styling.
5. **Screenshot 5 - Deleting a Task from Frontend**:
   - *Capture*: Clicking the "Delete" button on a task, showing the task card removed from the UI and confirmation alert displayed.
6. **Screenshot 6 - Browser DevTools Network Tab (CORS & HTTP 200)**:
   - *Capture*: DevTools **Network** tab showing the `POST /tasks` or `GET /tasks` request with status `200 OK` or `201 Created`, response headers displaying `Access-Control-Allow-Origin: *`, and JSON payload proving successful client-server communication.
7. **Screenshot 7 - MongoDB Compass Verification**:
   - *Capture*: MongoDB Compass GUI showing the `taskdb.tasks` collection displaying the identical tasks created through the React frontend, proving full-stack persistence.
