# Unraid Templates

Community Applications templates for Unraid.

## Available Apps

### SubVault

Self-hosted subscription management application built with Go and HTMX.

- **GitHub:** https://github.com/YakGravity/subvault
- **Docker Image:** `ghcr.io/yakgravity/subvault:latest`

## Installation

### Option 1: Add Template Repository

In Unraid, go to **Docker** → **Template Repositories** and add:

```
https://github.com/YakGravity/unraid-templates
```

### Option 2: Docker Compose

```yaml
services:
  subvault:
    image: ghcr.io/yakgravity/subvault:latest
    ports:
      - "8080:8080"
    volumes:
      - /mnt/user/appdata/subvault:/app/data
    environment:
      - TZ=Europe/Berlin
    restart: unless-stopped
```
