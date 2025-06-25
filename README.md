# 🐳 Nginx Reverse Proxy with Golang & Python Services (Docker Compose)

This project demonstrates a Dockerized microservices setup with an Nginx reverse proxy. It includes:
- A Golang-based API service
- A Python Flask-based API service
- Nginx as a reverse proxy to route requests

All components run in isolated Docker containers and communicate using Docker’s bridge network.



---

## ⚙️ Technologies Used

- Golang (Service 1)
- Python + Flask (Service 2)
- Nginx (Reverse Proxy)
- Docker & Docker Compose
- Health checks
- Bridge networking

---

## 📦 Architecture Overview

```text
          +-----------------------------+
          |        Client (Browser)     |
          +-------------+---------------+
                        |
                http://localhost:8080
                        |
                +-------v--------+
                |     Nginx      |
                | (Reverse Proxy)|
                +---+------+-----+
                    |      |
     /service1 ---> |      | <--- /service2
                +--v--+  +--v--+
                | Go  |  |Python|
                | App |  | App  |
                +-----+  +------+
