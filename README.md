# HandSim

<p align="center">
  <kbd>
    <img width="1437" height="745" alt="PreviewImage" src="https://github.com/user-attachments/assets/ec6a58ac-e191-4e90-ad5b-08585ef735e0" />
  </kbd>
</p>

HandSim is a full-stack application for simulating hand interactions with objects in a 3D environment. It uses a frontend built with React, TypeScript, react-three-fiber (Three.js), and Rapier for physics, and a Python backend leveraging OpenCV and MediaPipe for hand landmark detection. The frontend and backend communicate in real time using WebSockets.

## Tech Stack

- **Frontend:** React, TypeScript, Vite, react-three-fiber (Three.js), Rapier (physics)
- **Backend:** Python, OpenCV, MediaPipe
- **Communication:** WebSockets
- **Styling:** CSS

---

## Architecture

```
frontend/
  ├── src/
  │   ├── Components/      # React components for 3D objects and UI
  │   ├── Hooks/           # Custom React hooks for data fetching and state
  │   ├── Experience.tsx   # Main 3D experience logic (react-three-fiber, Rapier)
  │   ├── main.tsx         # App entry point
  │   └── style.css        # Global styles
  └── public/Assets/       # Static assets
backend/
  └── main.py              # Python backend server (OpenCV, MediaPipe, WebSockets)
```

- **Frontend** uses react-three-fiber for 3D rendering and Rapier for physics, receiving hand landmark data via WebSockets.
- **Backend** uses OpenCV and MediaPipe to process video frames and extract hand landmarks, sending data to the frontend in real time.

---

## Usage Instructions

### 1. Install Dependencies

```bash
# Install Node.js dependencies
npm install

# Set up Python environment
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

### 2. Run Backend

```bash
cd backend
python main.py
```

### 3. Run Frontend

```bash
cd frontend
npm run dev
```

### 4. Access the App

Open [http://localhost:5173](http://localhost:5173) in your browser.

---

## Key Files & Folders

- `frontend/src/Components/` — React components for simulation objects
- `frontend/src/Hooks/` — Custom hooks for hand and frame data
- `frontend/src/Experience.tsx` — Main 3D logic (react-three-fiber, Rapier)
- `backend/main.py` — Python backend server (OpenCV, MediaPipe, WebSockets)
- `requirements.txt` — Python dependencies
- `package.json` — Node.js dependencies

---

## Features

- Real-time hand simulation and visualization using MediaPipe landmarks
- Interactive 3D objects (Jenga blocks, barriers, projectiles) for experimentation
- Physics simulation powered by Rapier
- Modular React component structure
- WebSocket-based real-time communication between backend and frontend
