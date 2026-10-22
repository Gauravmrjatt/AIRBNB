# Airbnb Clone

A full-stack rental booking application — an Express/MongoDB API with JWT auth and Cloudinary image uploads, plus a React (Vite) single-page frontend.

## Stack

**Backend** — Express · MongoDB (Mongoose) · JWT · bcryptjs · Cloudinary · Multer · cookie-parser
**Frontend** — React · Vite · React Router · Axios · React Toastify

## Features

- **Auth** — register, login, logout; JWT stored in an httpOnly cookie
- **Listings** — create, browse and manage rental listings
- **Bookings** — create and manage reservations
- **Users** — profiles with avatar upload
- **Image pipeline** — Multer for multipart uploads, Cloudinary for storage and delivery
- **Route protection** — `isAuth` middleware guards private endpoints

## Structure

```
backend/
  config/         db.js · cloudinary.js · token.js
  controllers/    auth · booking · listing · user
  middleware/     isAuth · multer
  models/
  index.js        entry point
frontend/         React SPA (Vite)
```

## Getting started

### Backend

```bash
cd backend
npm install
```

Create `.env` (do not commit it):

```env
MONGODB_URL=mongodb://localhost:27017/airbnb
JWT_SECRET=<your-secret>
CLOUDINARY_CLOUD_NAME=<cloud-name>
CLOUDINARY_API_KEY=<api-key>
CLOUDINARY_API_SECRET=<api-secret>
```

```bash
npm run dev        # nodemon index.js
```

### Frontend

```bash
cd frontend
npm install
npm run dev
```

| Command | Description |
|---|---|
| `npm run dev` | Vite dev server |
| `npm run build` | Production build |
| `npm run preview` | Preview the build |
| `npm run lint` | ESLint |

## Environment variables

| Variable | Purpose |
|---|---|
| `MONGODB_URL` | MongoDB connection string |
| `JWT_SECRET` | Token signing secret |
| `CLOUDINARY_CLOUD_NAME` | Cloudinary cloud |
| `CLOUDINARY_API_KEY` | Cloudinary API key |
| `CLOUDINARY_API_SECRET` | Cloudinary API secret |
