# 🗺️ YourPlaces - Full-Stack Location Sharing App

YourPlaces is a full-stack **MERN (MongoDB, Express.js, React, Node.js)** application that enables users to discover, create, and share interesting locations on an interactive map. Users can sign up, log in, upload custom photos, add descriptions, and pinpoint exact map coordinates using integrated geocoding.

---

## ✨ Features

- 🔐 **User Authentication** – Secure signup and login using **JWT** and **bcryptjs** password hashing.
- 🗺️ **Interactive Google Maps** – View place locations on an embedded Google Map.
- 📍 **Location Geocoding** – Converts plain-text addresses into latitude and longitude using the Google Geocoding API.
- 🖼️ **Image Uploads** – Upload profile pictures and place images using Multer.
- ✏️ **CRUD Operations** – Create, Read, Update, and Delete places.
- 🛡️ **Protected Routes** – Only the creator of a place can edit or delete it.
- 📱 **Responsive UI** – Built with React and Tailwind CSS for desktop and mobile devices.

---

## 🛠️ Tech Stack

### Frontend

- React.js (Hooks, Custom Hooks, Context API)
- React Router DOM
- Tailwind CSS / Custom CSS
- Google Maps JavaScript API

### Backend

- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT (Authentication)
- Multer (File Uploads)
- Axios (Google Geocoding API)

---

## 📁 Project Structure

```text
YourPlaces/
├── backend/
│   ├── controllers/      # Route logic
│   ├── middleware/       # Authentication & uploads
│   ├── models/           # Mongoose models
│   ├── routes/           # API routes
│   ├── util/             # Helper functions
│   ├── uploads/          # Uploaded images
│   ├── app.js
│   └── .env
│
└── frontend/
    ├── public/
    └── src/
        ├── components/
        ├── context/
        ├── hooks/
        ├── pages/
        └── App.js
```

---

## 🚀 Getting Started

### Prerequisites

- Node.js (v14+)
- MongoDB (Local or Atlas)
- Google Cloud API Key (Maps JavaScript API + Geocoding API)

---

### 1. Clone the Repository

```bash
git clone https://github.com/pcdhamejani/yourplaces.git
cd yourplaces
```

---

### 2. Backend Setup

```bash
cd backend
npm install
```

Create a `.env` file:

```env
MONGO_URI=your_cluster_or_local_url
JWT_KEY=your_super_secret_jwt_key
GOOGLE_API_KEY=your_google_maps_api_key
```

Start the backend server:

```bash
npm start
```

Backend runs on:

```
http://localhost:5000
```

---

### 3. Frontend Setup

```bash
cd frontend
npm install
```

Create a `.env` file:

```env
REACT_APP_GOOGLE_API_KEY=your_google_maps_api_key
```

Add the Google Maps script to `public/index.html`:

```html
<script src="https://maps.googleapis.com/maps/api/js?key=%REACT_APP_GOOGLE_API_KEY%"></script>
```

Start the frontend:

```bash
npm start
```

Frontend runs on:

```
http://localhost:3000
```

---

## 🔒 API Endpoints

### Users (`/api/users`)

| Method | Endpoint | Description | Auth |
|--------|----------|-------------|------|
| GET | `/` | Get all users | ❌ |
| POST | `/signup` | Register a new user | ❌ |
| POST | `/login` | Login and receive JWT | ❌ |

### Places (`/api/places`)

| Method | Endpoint | Description | Auth |
|--------|----------|-------------|------|
| GET | `/:pid` | Get place by ID | ❌ |
| GET | `/user/:uid` | Get all places by user | ❌ |
| POST | `/` | Create a place | ✅ |
| PATCH | `/:pid` | Update a place | ✅ |
| DELETE | `/:pid` | Delete a place | ✅ |

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome.
