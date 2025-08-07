# Real-Time Location Tracker

A real-time location tracking web application built with JavaScript, using Node.js, Express, Socket.io, and EJS. It allows clients to share live location data and see each other's positions dynamically on a map.

---

##  Features

-  Real-time location updates via WebSocket (Socket.io)  
-  Interactive map display with real-time markers using Leaflet.js  
-  Multi-client support of live geolocation sharing  
-  Lightweight server using Node.js and Express.js

---

##  Tech Stack

- **Backend:** Node.js, Express.js  
- **Real-Time Communication:** Socket.io  
- **Frontend:** EJS templating, Leaflet.js for map visualization  
- **Dependencies & Node Modules:** Installed via `npm`

---

##  Project Structure

LocationRealtime/
├── public/
│ ├── css/ # Stylesheets
│ └── js/ # Client-side JavaScript
├── views/
│ └── index.ejs # EJS template for frontend UI
├── app.js # Main server application
├── package.json # Project metadata and dependencies
├── package-lock.json # Exact package versions
└── README.md # This file


---

##  Getting Started

### Prerequisites

- Node.js (LTS or newer)  
- npm (comes with Node.js)


How It Works
Server Setup

app.js initializes an Express server and sets up Socket.io for bidirectional communication.

Client Connection

When a client connects via browser, they serve an HTML page rendered from index.ejs.

Location Broadcasting

Client-side JavaScript captures geolocation data using the browser's API and sends it to the server through Socket.io.

Server broadcasts every client’s coordinates to all connected browsers.

Map Rendering

Leaflet.js renders an interactive map in each client window.

As coordinates arrive, client-side scripts update or render markers for each user in real-time.



Implement marker labels or popups with user info or timestamps

Introduce map clustering to handle many simultaneous users

Add UI elements for toggling markers visibility or map themes

Store location history (e.g. in a database) for playback or analytics
