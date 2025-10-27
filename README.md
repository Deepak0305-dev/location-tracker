# 📍 Location Tracker

**Live demo:** [https://location-tracker-1-e8hg.onrender.com/](https://location-tracker-1-e8hg.onrender.com/)

A real-time location tracking web application that allows users to share and view live GPS locations on a map.  
Useful for delivery tracking, event management, or personal location sharing — with smooth, responsive maps and WebSocket updates.

---

## 🚀 Features

- Real-time location updates using WebSockets (Socket.IO or native WebSocket)
- Interactive map visualization (Leaflet / Mapbox / Google Maps)
- Track multiple users or devices simultaneously
- Optional location history and route tracking
- Responsive, mobile-friendly UI
- Hosted on **Render** (full-stack deployment)

---

## 🧱 Tech Stack

| Layer | Technology |
|--------|-------------|
| **Frontend** | React (or vanilla HTML/JS) |
| **Mapping** | Leaflet / Mapbox GL JS / Google Maps |
| **Backend** | Node.js + Express |
| **Real-time** | Socket.IO |
| **Database** | MongoDB / PostgreSQL (optional) |
| **Hosting** | Render.com |

---

location-tracker/
├── backend/
│ ├── package.json
│ ├── src/
│ │ ├── index.js
│ │ ├── routes/
│ │ └── sockets/
│ └── .env.example
├── frontend/
│ ├── package.json
│ ├── src/
│ │ ├── App.jsx
│ │ ├── components/
│ │ └── pages/
│ └── public/
├── docker-compose.yml (optional)
├── README.md
└── LICENSE

----


---

## ⚙️ Setup — Run Locally

### 1️. Clone the Repository
```bash
git clone https://github.com/<your-username>/location-tracker.git
cd location-tracker

2. cd backend
   cp .env.example .env
   # Add your environment variables (see below)
   npm install
   npm run dev       # or: node src/index.js
   # Server runs on PORT (default 5000)

3. Frontend Setup
   cd ../frontend
   npm install
   npm start
   # Visit http://localhost:3000

------
**Backend**
PORT=5000
NODE_ENV=development
MONGO_URI=mongodb+srv://<user>:<pass>@cluster.mongodb.net/location-tracker
JWT_SECRET=your_secret_key_here
SOCKET_PATH=/socket
ALLOW_ORIGIN=http://localhost:3000

**Frontend**
VITE_API_URL=http://localhost:5000
VITE_SOCKET_URL=http://localhost:5000
VITE_MAPBOX_TOKEN=pk.your_mapbox_token_here
-----

** Future Enhancements **

• Add route playback feature (view path history)

• Enable sharing via invite link or QR code

• Push notifications for movement alerts

• Add dark/light map themes

• Integrate with GPS modules for IoT devices

-----

