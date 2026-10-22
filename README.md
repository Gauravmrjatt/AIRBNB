# Airbnb Clone

A rental booking app: an Express and MongoDB API with JWT auth and Cloudinary uploads, and a React single page front end on top.

## What it does

- Register, log in, log out. JWT rides in an httpOnly cookie
- Create, browse and manage listings
- Create and manage bookings
- User profiles with avatar upload
- Uploads pass through Multer, then land in Cloudinary
- `isAuth` middleware guards the private routes

About 2,200 lines across 43 files, 3 Mongoose models.

## Stack

**Backend** Express, MongoDB via Mongoose, JWT, bcryptjs, Cloudinary, Multer, cookie-parser
**Frontend** React, Vite, React Router, Axios, React Toastify

## Layout

```
backend/
  config/         db.js, cloudinary.js, token.js
  controllers/    auth, booking, listing, user
  middleware/     isAuth, multer
  models/
  index.js
frontend/         React SPA
```

## Run it

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

| Command | What it does |
|---|---|
| `npm run dev` | Vite dev server |
| `npm run build` | Production build |
| `npm run preview` | Preview the build |
| `npm run lint` | ESLint |

## Environment

| Variable | Purpose |
|---|---|
| `MONGODB_URL` | Mongo connection string |
| `JWT_SECRET` | Token signing |
| `CLOUDINARY_CLOUD_NAME` | Cloudinary cloud |
| `CLOUDINARY_API_KEY` | Cloudinary key |
| `CLOUDINARY_API_SECRET` | Cloudinary secret |
