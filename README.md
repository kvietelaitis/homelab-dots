# Home Server
 
Self-hosted services running on Docker with Caddy reverse proxy.
 
## Services
 
- **Audiobookshelf** - Audiobook & podcast server
- **Calibre** - E-book management
- **Immich** - Photo & video backup
- **Jellyfin** - Media streaming
- **Retrom** - Game library manager
- **Samba** - Network file sharing
- **Syncthing** - File synchronization
- **Vaultwarden** - Password manager
## Structure
 
```
├── caddy/          # Reverse proxy configuration
├── docker/         # Service compose files
└── scripts/        # Management scripts
```
 
## Scripts
 
- `docker-up` - Start all services
- `docker-shutdown` - Stop all services
- `docker-upgrade` - Update containers
- `backup-srv` - Backup server data with restic
## Usage
 
```bash
# Start services
./scripts/docker-up
 
# Stop services
./scripts/docker-shutdown
 
# Update all containers
./scripts/docker-upgrade
 
# Backup
./scripts/backup-srv
```
 
## Access
 
Some services are accessible via Caddy reverse proxy, while others are only available with a tailscale connection. Configure domains in `caddy/Caddyfile`.
 
