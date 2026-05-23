# SmartPlanner Frontend

A Vue 3 frontend for SmartPlanner, built with Vite and served via Nginx in production.

---

## Prerequisites

- [Node.js 20+](https://nodejs.org/)
- [Docker Desktop](https://www.docker.com/products/docker-desktop/)

---

## Environment Setup

Copy the example env file

```bash
cp .env.example .env
```

## 1. Run Frontend Locally

```bash
# Install dependencies
npm install

# Start the dev server (hot-reload at http://localhost:5173)
npm run dev
```
---

## 2. Run with Docker Compose (dev)

> The dev compose file joins an **external** Docker network called `smartplanner` that the backend creates. Start the backend stack first, or create the network manually:
> ```bash
> docker network create smartplanner
> ```

```bash
docker compose -f docker-compose.dev.yml up --build -d
```

The app will be available at **http://localhost**.

---

## 3. Stop the Container

```bash
docker compose -f docker-compose.dev.yml stop
```

---

## 4. Delete the Container

```bash
docker compose -f docker-compose.dev.yml down
```

To also remove the built image:

```bash
docker compose -f docker-compose.dev.yml down --rmi local
```
