#WordPress & WireGuard


## Getting Started

### 1. Configure the Environment
Copy the example environment file and fill in your secure database credentials and trusted IP information.
```bash
cp .env.example .env
nano .env
```

### 2. Start the Stack
Bring up all the containers in detached mode:
```bash
docker compose up -d
```


### 3. Connect to the VPN
To access the website, you must be connected to the VPN. The client configuration file and a convenient QR code are automatically generated for you at:
```text
./wireguard/peer1/peer1.conf
./wireguard/peer1/peer1.png
```
Import this configuration into your local WireGuard app (desktop or mobile) and connect. Once connected to the VPN, you can immediately access the WordPress site through your browser.

## 🛠 Useful Commands
- View logs for all services: `docker compose logs -f`
- Restart Nginx to apply new configs: `docker compose restart nginx`
- Stop all services: `docker compose down`

