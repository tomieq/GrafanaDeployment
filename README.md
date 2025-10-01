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

# Grafana uid
Sometimes docker-compose will raise a warning about unknown `UID`.
```
export UID
```

# Grafana digest authentication
Grafana UI is protected with digest authentication. Users are sored in `traefik-config/digestUsers.txt` file. 
The format is:
```
username:realm:encryptedPassword
```
The encryptedPassword can be generated using:
```
brew install apache2-utils
sudo apt-get install apache2-utils
htdigest traefik-config/digestUsers.txt grafana admin
```
Default credentials in the config file is: admin:haslo