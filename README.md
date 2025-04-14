# nginx-rtmp-docker

A lightweight, Dockerized NGINX RTMP server for live video streaming. Easily stream from OBS or any RTMP compatible client.

## 🚀 Quick Start

1. **Clone the repo**

```bash
git clone https://github.com/RaguSalsa/nginx-rtmp-docker.git
cd nginx-rtmp-docker
```

2. **Start the server**

```bash
docker compose up -d
```

3. **Stream to it using OBS**

- **Service:** Custom
- **Server:** `rtmp://<your-ip/domain>:1935/${STREAM_APP}`
- **Stream Key:** `<your-key>`

> Example Output Stream Server:  
> `rtmp://www.example.com:1935/live/abc123`

## 📊 View Stream Stats

View a live XML feed of streaming stats at:

```
http://<your-ip/domain>/stat
```

## ⚙️ Configuration

You can change the STREAM_APP variable in `docker-compose.yml`:

```yaml
environment:
  - STREAM_APP=live
```
