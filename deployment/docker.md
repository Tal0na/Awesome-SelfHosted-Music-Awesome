# 🎧 Quick Music Server (Docker)

Minimal guide to deploy **Navidrome** or **Jellyfin** using Docker.

---

## 📁 Setup

```bash
mkdir -p music-server/{data,music} && cd music-server
```

---

## 🐳 Navidrome

```yaml
# docker-compose.yml
services:
  navidrome:
    image: deluan/navidrome:latest
    container_name: navidrome
    ports:
      - "4533:4533"
    restart: unless-stopped
    environment:
      ND_SCANINTERVAL: 1h
      ND_LOGLEVEL: info
      ND_BASEURL: ""
    volumes:
      - ./data:/data
      - ./music:/music:ro
```

🌐 Access: `http://localhost:4533`

---

## 🐳 Jellyfin

```yaml
# docker-compose.yml
services:
  jellyfin:
    image: jellyfin/jellyfin:latest
    container_name: jellyfin
    ports:
      - "8096:8096"
    restart: unless-stopped
    volumes:
      - ./data:/config
      - ./music:/music:ro
```

🌐 Access: `http://localhost:8096`

---

## 🛠️ Commands

```bash
docker compose up -d          # Start
docker compose down           # Stop
docker compose logs -f        # Logs
docker compose pull && docker compose up -d  # Update
```

---

## ⚙️ Navidrome Variables

| Variable            | Description        | Example         |
| ------------------- | ------------------ | --------------- |
| `ND_SCANINTERVAL`   | Scan frequency     | `1h`, `30m`     |
| `ND_BASEURL`        | Reverse proxy path | `/music`        |
| `ND_LOGLEVEL`       | Log level          | `info`, `debug` |
| `ND_SESSIONTIMEOUT` | Session expiry     | `24h`           |

---

## 💡 Tips

- Use `:ro` on the music volume to prevent accidental file modifications
- Set `ND_BASEURL` if running behind a reverse proxy
- On first login, create your admin account
- Point the music volume to your existing library path, e.g. `/home/user/Music:/music:ro`
