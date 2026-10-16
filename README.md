
# DevOps Winter Arc — Day 02
## Dockerfile Deep Dive

### Objective
Build and run a configurable Node.js API using Docker.

### Files
- `Dockerfile` — Builds the Node.js API image.
- `server.js` — Implements the API and health endpoint.
- `package.json` — Defines application metadata.
- `.dockerignore` — Excludes unnecessary files.
- `Dockerfile.greeter` — Demonstrates CMD and ENTRYPOINT.

### Build
```bash
sudo docker build --progress=plain -t demo-api:v1 --build-arg APP_VERSION=1.0 .
```

### Run
```bash
sudo docker run -d --name api -p 3000:3000 demo-api:v1
```

### Test
```bash
curl http://localhost:3000/
curl http://localhost:3000/health
```

### Key Learnings
- Dockerfile instructions and image layers
- Build arguments versus environment variables
- Docker build caching
- CMD versus ENTRYPOINT
- Container ports and API health checks

