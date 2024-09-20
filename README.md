##How to run the assignment
### 1. Prerequisites
Before you start, ensure you have the following installed on your system:
- **Docker**: [Install Docker](https://docs.docker.com/get-docker/)
- **Docker Compose**: [Install Docker Compose](https://docs.docker.com/compose/install/)
- **Git**: [Install Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

---

### 2. Clone the Repository
First, clone the repository containing the assignment files:
```bash
git clone https://github.com/aakashkhanna/hs-assignment.git
cd hs-assignment
```

---

### 3. Build and Run the Services
Once the `docker-compose.yml` file and `nginx.conf` are ready, run the following command to start all services:

```bash
docker-compose up --build
```

This command will:
- Build the Docker images for each API.
- Start the PostgreSQL service.
- Start each API and the reverse proxy (NGINX).

---

### 4. Verify the Services
Once the services are up and running, you can test each API using the following URLs in your browser or via a tool like Postman or `curl`:

- **Users API**: `http://localhost:3000`
- **Orders API**: `http://localhost:4000`
- **Products API**: `http://localhost:5000`

Each API should respond to its respective routes as defined in the code provided.

---

### 5. Stopping the Containers
To stop all running services, press `CTRL + C` in the terminal where `docker-compose` is running or run:

```bash
docker-compose down
```

This will stop and remove the running containers.

---


### Troubleshooting and Notes
- **Port conflicts**: Ensure no other services are running on ports 3000, 4000, 5000, or 5432.
```