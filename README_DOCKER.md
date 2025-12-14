**Docker Quick Start**

This project includes Docker setup for the Backend (Node/Express), Frontend (Expo web) and MongoDB.

Prerequisites:
- Docker & Docker Compose installed

Build and start everything:

```bash
# from repo root
docker-compose up --build -d
```

Verify services:

```bash
# Backend
curl -i http://localhost:3001/
curl -i http://localhost:3001/api

# Frontend (Expo web)
# open http://localhost:19006 in your browser
```

Stop and remove:

```bash
docker-compose down
```

Notes:
- Backend environment uses `MONGO_URI=mongodb://mongo:27017/discountmate` when run via Compose.
- Backend logs are available under `./Backend/logs` on your host (mounted volume).
- The frontend is configured to run Expo in web mode; if you prefer to run it locally with native simulators, run it outside Docker.
