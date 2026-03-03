# 🛍️ ShoppyGlobe

**ShoppyGlobe** is a full-stack MERN (MongoDB, Express, React, Node.js) e-commerce web application. It provides a seamless shopping experience with features like product browsing, JWT-based authentication, cart management, filtering, checkout, and order handling. The frontend is built using **React**, **Redux Toolkit**, and **core CSS**, while the backend is powered by **Node.js**, **Express**, and **MongoDB Atlas**.

## 💻 Live Demo

[Click here](https://shoppyglobe-frontend.onrender.com/) to view a live demo of **ShoppyGlobe**.

> Note: Both the frontend and backend are deployed on [**Render**](https://www.render.com/), so the backend may take a few seconds to wake up on first request.

## 🚀 Features

### Frontend

- **JWT Authentication** — Secure login and registration with token-based access control.
- **Dynamic Product Pages** — View product details using route parameters.
- **Cart Management** — Add, remove, and update quantity with backend sync.
- **Checkout & Order Summary** — Real-time calculation of totals, taxes, and shipping.
- **Global Search & Filters** — Search by product title, brand, category, or description.
- **Redux Toolkit** — Efficient state management for user, cart, and product data.
- **Lazy Loading** — Optimized performance with `React.lazy` and `Suspense`.

### Backend

- **RESTful API** — Custom-built APIs for products, users, cart, and orders.
- **MongoDB Atlas** — Persistent data storage for users, cart items, and orders.
- **Protected Routes** — Middleware to restrict access based on JWT tokens.
- **CORS Configuration** — Secure communication between frontend and backend.

---

## 🧰 Tech Stack

### Frontend

- **Framework**: React (bundled via [Vite](https://vite.dev/))
- **State Management**: [Redux Toolkit](https://redux-toolkit.js.org/)
- **Routing**: [React Router DOM v7](https://reactrouter.com/) with nested and dynamic routes
- **Styling**: Core CSS
- **UI Enhancements**:
  - [FontAwesome](https://fontawesome.com/) Icon Support
  - Toast Notifications via [`react-hot-toast`](https://react-hot-toast.com/)
- **Performance**:
  - Lazy loading with `React.lazy` & `Suspense`
  - Optimized builds with Vite

### Backend

- **Runtime**: Node.js
- **Server Framework**: [Express.js](https://expressjs.com/)
- **Database**: [MongoDB Atlas](https://www.mongodb.com/products/platform/atlas-database) (via [Mongoose ODM](https://mongoosejs.com/))
- **Authentication**: [JSON Web Tokens (JWT)](https://www.jwt.io/)
- **Security**: Hashed passwords using [bcryptjs](https://www.npmjs.com/package/bcrypt)
- **CORS**: Configured for secure frontend-backend communication
- **Environment Config**: [dotenv](https://www.dotenv.org/)

### Replaced External API

> The project originally used [DummyJSON](https://dummyjson.com/) for product data but now features a **custom-built RESTful API** using data scraped from DummyJSON and stored in **MongoDB Atlas**. This allows for full control over the data layer and CRUD operations across the application.

---

## 📂 Folder Structure

The project follows a **monorepo structure** with separate `frontend/` and `backend/` directories managed together in a single repository. The backend is organized using the **MVC (Model-View-Controller)** architectural pattern to ensure separation of concerns and scalability.

```
.
├── backend/ # Express + MongoDB (API server)
│ ├── config/ # Database connection config (MongoDB Atlas)
│ ├── controllers/ # Logic for handling route requests (auth, products)
│ ├── models/ # Mongoose schemas for User, Order, Cart, and Product
│ ├── routes/ # API endpoint definitions (auth, user, cart, etc.)
│ ├── seedProducts.js # Script to seed initial product data
│ ├── .env # Environment variables (PORT, DB_URI, JWT_SECRET)
│ ├── package.json # Backend dependencies
│ └── server.js # Entry point for the Express server
│
└── frontend/ # React client (Vite + Redux)
├── src/
│ ├── assets/ # Logos, favicon, and static media
│ ├── components/ # UI components (Header, Footer, Search, etc.)
│ ├── pages/ # Route-based views (Home, Cart, Checkout, etc.)
│ ├── utils/ # Redux store & slices, custom hooks
│ ├── App.jsx # App layout and routes
│ └── main.jsx # Entry point with router and Redux provider
├── package.json # Frontend dependencies
└── vite.config.js # Vite build configuration
```

