**What I changed**
- Added Docker support for Backend and Frontend (Dockerfiles).
- Added `docker-compose.yml` to run `mongo`, `backend`, and `frontend` services.
- Added `README_DOCKER.md` and updated `Backend/README.md` with Docker instructions.
- Updated `.gitignore` to exclude backend logs and uploads.

**How to test**
1. Ensure Docker and Docker Compose are installed.
2. Run `docker-compose up --build -d` from repo root.
3. Verify `GET /` and `GET /api` at `http://localhost:3001`.
4. Verify `POST /api/v1/users/signup` returns a validation error for empty payload.

**Notes**
- Mongo runs as an internal service; if you already have a local Mongo listening on 27017, the compose file will not bind that port to avoid conflicts.
