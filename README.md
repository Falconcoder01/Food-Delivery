# 🚚 Food Delivery App – Dockerized MERN Stack application with Nginx 


A fully Dockerized MERN (MongoDB, Express.js, React.js, Node.js) food delivery web application featuring Nginx as a reverse proxy and load-balancer for streamlined performance, scalability, and production-ready deployment.

> Forked and enhanced from [@Mshandev/Food-Delivery](https://github.com/Mshandev/Food-Delivery)  
> Modernized with Docker, Docker Compose, and Nginx for seamless containerized deployment.

---

## 🔥 Features

- 🍔 Full-stack Food Delivery Application
- 📦 Dockerized Backend, Frontend, and MongoDB
- 🌐 Nginx Reverse Proxy for Load Balancing and Performance
- 🧾 Authentication, Cart, and Order Management
- 🧠 Built with MERN Stack
- 💻 Easily Deployable on Any Docker-Ready Host

---

## 🚀 Tech Stack

| Layer     | Technology                  |
|-----------|-----------------------------|
| Frontend  | React.js, Redux, Tailwind   |
| admin     | React.js, Redux, Tailwind   |
| Backend   | Node.js, Express.js         |
| Database  | MongoDB                     |
| Proxy     | Nginx (multi-container setup) |
| Containerization | Docker, Docker Compose |

---

## 🐳 Getting Started with Docker

### Prerequisites

- Docker v2 & Docker Compose v2 installed
- Git installed

## 📂 Structure:

    Frontend: http://localhost
    admin-panel: http://localhost/admin
    Backend API: http://localhost/api (proxied via Nginx)
    MongoDB: Internal container (mongo:latest)



## Setup Environment Variables In Backend

    JWT_SECRET=YOUR_SECRET_TEXT
    SALT=YOUR_SALT_VALUE
    MONGO_URL=YOUR_DATABASE_URL
    STRIPE_SECRET_KEY=YOUR_KEY


## Clone and Run

```bash
git clone https://github.com/Falconcoder01/Food-Delivery.git
cd Food-Delivery
docker compose up -d --build
```
## 📬 Contact
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/utkarshm1/)
Email: utkarshmishra5485@gmail.com


