# Rental & Services Management System

A full-stack platform to list, browse, book, and manage rentals (e.g., apartments, vehicles) and on-demand services (e.g., plumbing, pest control). Customers can discover and reserve; owners/admins can manage inventory, pricing, calendars, and bookings.

> Tech: **React** · **Node.js/Express** · **MongoDB/Mongoose** · **JWT Auth** · **Docker / Docker Compose**

---

## Features
- **Listings & Search** — Filter by type, price, dates, and availability.
- **Bookings & Payments** — Create, manage, and cancel bookings; payment-gateway ready.
- **Accounts & Auth** — JWT-based sign up/in; roles for **customer** and **owner/admin**.
- **Reviews & Ratings** — Build trust via feedback loops.
- **Admin Dashboard** — Inventory, pricing, calendar blocks, approvals.
- **Scalable** — Stateless services, environment-driven config, Dockerized.

---

## Architecture
- **Frontend (`/frontend`)**: React SPA; talks to API via `VITE_API_BASE`.
- **API (`/api`)**: Node.js/Express; REST endpoints for auth, listings, bookings.
- **Admin Backend (`/backend`)** *(optional/separate)*: Owner/admin operations.
- **Database**: MongoDB (with optional `mongo-express` for inspection).
- **Container Orchestration**: `docker-compose.yml` for local dev.

---


## Prerequisites
- **Node.js 18+** and **npm**
- **Docker** & **Docker Compose** (recommended for local dev)
- (Optional) Payment keys (e.g., Stripe/PayPal)


A full-stack platform that connects customers with rental property owners and service providers. It simplifies **bookings, payments, and communication**, while enabling owners to manage inventory, pricing, and customer feedback.

---

## 🚩 Problem

Renting homes, vehicles, or booking services often involves:
- Unresponsive owners or unclear availability
- Manual, outdated booking methods
- Scattered communication and delayed payments
- Difficulty in tracking customer feedback

The rental and services industry is **fragmented despite its $2 trillion global market size**, leading to poor customer experiences and inefficiency:contentReference[oaicite:2]{index=2}.

---

## 🛠️ Technologies Used

### Frontend
- **React.js**: SPA with reusable UI components, Virtual DOM, and fast rendering:contentReference[oaicite:5]{index=5}

### Backend
- **Node.js**: REST APIs, real-time support, scalable server-side runtime  
- **Mongoose & JWT**: MongoDB ORM and authentication/authorization:contentReference[oaicite:6]{index=6}

### Database
- **MongoDB**: Separate collections for users, listings, bookings; supports flexible schemas, fast lookups, and aggregation:contentReference[oaicite:7]{index=7}

---

## 🏗️ Architecture

### Overview
- **Three-tier architecture**:  
  `Frontend (React) ↔ Backend (Node.js/Express) ↔ Database (MongoDB)`:contentReference[oaicite:8]{index=8}
- **Services**:  
  - `api/` — public booking & payment endpoints  
  - `backend/` — admin dashboard & management APIs  
  - `frontend/` — React SPA for customers:contentReference[oaicite:9]{index=9}
- **Deployment**: Docker Compose orchestrates all containers (`api`, `backend`, `frontend`, `mongo`, `mongo-express`):contentReference[oaicite:10]{index=10}


