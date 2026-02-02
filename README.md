# Kafka-startup-with-kafka-ui
kafka startup file for easier kafka setup along with kafka-UI


# Usage

### To start go to file directory and run below command

Starts Kafka in KRaft mode (no Zookeeper)
```bash
docker compose up
```

### Verify containers are running
```bash
docker compose ps
```

### To access kafka-ui 

```bash
http://localhost:8080
```

### Test Kafka connectivity

#### From your host (outside Docker)
```
localhost:9092
```

#### From another Docker container
```
kafka:19092
```

### Stop / remove containers
```
docker compose down
```

## Things to note

- Do NOT use localhost:9092 from another container
- Use kafka:19092
- Ports
- 9092 → host access
- 19092 → internal Docker access
- 9093 → controller (internal only)
- First startup may take ~10–20 seconds
- Kafka UI may show “connecting” briefly
