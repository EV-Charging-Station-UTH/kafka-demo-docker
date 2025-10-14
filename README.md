# Kafka Demo (Dockerized)

This project demonstrates a simple Kafka ecosystem with Zookeeper, Kafka Broker, Kafka UI, a Producer, a Consumer, and a Frontend for visualization.

All services are containerized using Docker and can be easily started using Docker Compose.

---

## 🚀 How to Run

### 1️⃣ Clone or download this repository
```bash
git clone https://github.com/EV-Charging-Station-UTH/kafka-demo-docker.git
cd kafka-demo-docker
```

### 2️⃣ Ensure you have Docker and Docker Compose installed
Check your installations:
```bash
docker --version
docker compose version
```

If not installed, follow official guides:
- [Install Docker](https://docs.docker.com/get-docker/)
- [Install Docker Compose](https://docs.docker.com/compose/install/)

---

### 3️⃣ Pull the latest images (optional)
If you want to ensure you’re using the latest versions:
```bash
docker compose pull
```

---

### 4️⃣ Start all services
```bash
docker compose up -d
```

This will start:
- 🐘 Zookeeper
- 🔥 Kafka Broker
- 🧭 Kafka UI (on port **8080**)
- 📨 Producer (on port **8082**)
- 📥 Consumer (on port **8083**)
- 🌐 Frontend UI (on port **3000**)

---

### 5️⃣ Verify everything is running
```bash
docker ps
```
You should see all containers running.

---

### 6️⃣ Access the services
| Service | URL | Description |
|----------|------|-------------|
| Kafka UI | [http://localhost:8080](http://localhost:8080) | Inspect Kafka topics, messages, and consumer groups |
| Frontend | [http://localhost:3000](http://localhost:3000) | Web UI to visualize producer and consumer lifecycle |

---

### 7️⃣ Stop all containers
```bash
docker compose down
```

---

### 🧩 Notes
- All images are prebuilt and hosted on Docker Hub under:  
  [`trandinh0506`](https://hub.docker.com/u/trandinh0506)
- The `docker-compose.yml` will automatically connect all services via a shared network (`kafka-demo-net`).
- Data for Kafka and Zookeeper are persisted using named Docker volumes.

---

Enjoy exploring Kafka in action! 🎉
