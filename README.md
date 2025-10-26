Adapter for Docker Compose deployment on Docker Desktop for repo: https://github.com/alexcayoja-sys/finance

This package adds Dockerfiles and a docker-compose.yml to run the existing Django (Postgres) backend and React frontend using Docker Desktop.
- Postgres runs as 'db' service
- Backend runs with Gunicorn on port 8000
- Frontend is built and served by nginx on port 3000 (host)

How to use:
1. Copy this folder content into the root of the cloned repo (next to backend/ and frontend/)
2. Edit backend/.env with real SECRET_KEY and settings if required
3. From Docker Desktop or terminal run: docker compose up -d --build
4. Access frontend at http://localhost:3000 and backend API at http://localhost:8000

Notes:
- Volumes are configured for Postgres persistence
- Adjust worker counts and production settings as needed
