🛺 Cab Booking System (Uber‑Style App)
A full-stack MERN (MongoDB, Express, React, Node.js) cab booking application inspired by the Sheryians Coding School tutorial. Enables users to request rides, drivers to accept bookings, and real-time tracking of trips.

🚀 Features
User Authentication: Sign up / log in as a rider or driver.

Ride Requests: Users can book rides by entering pickup/drop locations.

Driver Dashboard: Drivers view incoming requests and accept.

Real-Time Tracking: Live ride status and maps (Google Maps integration).

Admin Controls: Monitor users, rides, and drivers.

Chat Integration: In-ride messaging between riders and drivers.

Notifications: Users get informed when rides are accepted, started, finished.

🧱 Tech Stack
Frontend: React, Redux (or Context API), Google Maps API, Socket.io

Backend: Node.js, Express.js, Socket.io

Database: MongoDB (with Mongoose)

Realtime Communication: WebSockets via Socket.io

Maps & Geolocation: Google Maps Platform

📂 Repository Structure
perl
Copy
Edit
cab-booking-system/
├── Backend/
│   ├── controllers/      # Route handler logic
│   ├── db/               # Database connection setup
│   ├── middlewares/      # Auth and validation middleware
│   ├── models/           # Mongoose schemas (User, Ride, etc.)
│   ├── routes/           # API route definitions
│   ├── services/         # Business logic and socket handlers
│   ├── app.js            # Express app initialization
│   └── server.js         # Server + Socket.io setup
├── frontend/             # React application
│   ├── src/
│   │   ├── components/   # UI components (Map, User forms, etc.)
│   │   ├── pages/        # Screens (Home, Dashboard, Booking)
│   │   ├── store/        # Redux slices or context
│   │   └── utils/        # API calls, helper functions
│   └── package.json
├── README.md
└── .gitignore
🔧 Prerequisites
Node.js (v14+)

MongoDB (local or Atlas)

Google Maps API key

npm or yarn

⚙️ Installation & Development
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/yourusername/cab-booking-system.git
cd cab-booking-system
2. Backend Setup
bash
Copy
Edit
cd Backend
npm install
cp .env.example .env
# Edit .env with MONGODB_URI, JWT_SECRET, GOOGLE_MAPS_KEY, etc.
npm run dev
3. Frontend Setup
bash
Copy
Edit
cd frontend
npm install
cp .env.example .env
# Edit .env with REACT_APP_API_URL, REACT_APP_GOOGLE_MAPS_KEY, etc.
npm start
App runs at:

Backend → http://localhost:5000

Frontend → http://localhost:3000

📋 API Routes
Route	Method	Protected	Description
/api/auth/register	POST	No	Register user (rider/driver)
/api/auth/login	POST	No	User login
/api/users/me	GET	Yes	Get current user info
/api/rides/request	POST	Yes	Rider requests a ride
/api/rides/:id/accept	PUT	Yes	Driver accepts a ride request
/api/rides/:id/complete	PUT	Yes	Mark ride as completed
/api/rides	GET	Yes	List rides (user-specific)

✨ Real-Time Features with Socket.io
Event broadcasting when:

New ride is requested (rideRequested)

Driver accepts ride (rideAccepted)

Ride completed (rideCompleted)

Real-time location updates via WebSocket during trip

📦 Deployment
Deploy backend on Heroku / AWS / DigitalOcean

Build frontend (npm run build) and serve it (e.g., in Express or via Netlify/Vercel)

Set environment variables in production (MONGODB_URI, API keys)

✅ Contributing
Fork the repository

Create a feature branch (git checkout -b feature-name)

Make changes & commit (git commit -m "Describe change")

Open a pull request


📝 License
MIT

