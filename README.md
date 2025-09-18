# Grafana logs preview

### Start service
```
docker-compose up
docker-compose up -d --force-recreate
```
### Stop service
```
docker-compose down
```

### Initial login
```
login: admin
pass: admin
```

### Ports
- Grafana listens on port 3000
- Loki listens on port 3100
- Traefik wraps them on port 7070