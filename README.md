# 📦 Ekart Application with Netdata Monitoring using Docker Compose

This project demonstrates how to deploy a custom **Ekart application** container alongside a **Netdata monitoring tool** using **Docker Compose**. The setup enables real-time system and container monitoring via Netdata's web UI.

---


## 📖 About the Project

This deployment includes:
- **Ekart App** — A sample containerized application running on port **8070**
- **Netdata** — A real-time performance and health monitoring dashboard for the host and containers

Both services are managed via **Docker Compose** for easy orchestration.

---

## ⚙️ Tech Stack

- **Docker**
- **Docker Compose**
- **Netdata**
- **Linux (Ubuntu)**

---

## 📁 Folder Structure

```bash
.
├── docker-compose.yml
└── README.md
```

🛠️ Prerequisites:
-------------------
Ensure you have:

1.Docker installed and running

2.Docker Compose installed

3.Internet connection for pulling images


🚀 Installation & Usage
1️⃣ Clone the Repository
```
git clone https://github.com/SuryaSJV/Netdata-Monitoring.git
cd Netdata-Monitoring
```

2️⃣ Run Docker Compose
```
docker compose up -d
```

3️⃣ Verify Running Containers
```
docker ps
```

🌐 Accessing the Applications
Ekart App:
http://localhost:8070

Netdata Dashboard:
http://localhost:19999


📊 Monitoring & Logs
📈 Netdata Dashboard
Open http://localhost:19999 in your browser to view:
```
.Real-time system metrics (CPU, Memory, Disk, Network)

.Docker container statistics

.Active alerts and health checks
```

📂 Viewing Netdata Logs
To access logs inside the container:
```
docker exec -it netdata bash
cd /var/log/netdata
ls
```

To view a log file:
```
tail -f access.log
```

📌 Docker Commands Reference
```
Purpose	                           Command
-------                          ----------
Start containers via Compose  -	docker compose up -d
Stop containers via Compose   -	docker compose down
List running containers       -	docker ps
View logs of a container      -	docker logs <container_name>
Enter container shell	      - docker exec -it <container_name> bash
```
