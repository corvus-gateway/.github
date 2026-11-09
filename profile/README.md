<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/corvus-gateway/corvus/main/assets/brand/corvus-logo-dark.svg">
  <img src="https://raw.githubusercontent.com/corvus-gateway/corvus/main/assets/brand/corvus-logo.svg" alt="Corvus" width="360">
</picture>

### Active Web Protection Gateway

A self-hosted reverse proxy that also protects the services behind it.

[Documentation](https://corvusgateway.org/) · [Install](https://corvusgateway.org/getting-started/install/) · [Releases](https://github.com/corvus-gateway/corvus/releases) · [Discussions](https://github.com/corvus-gateway/corvus/discussions)

</div>

**[Corvus](https://github.com/corvus-gateway/corvus)** is as easy to run as Nginx Proxy Manager
(domains, forwarding and free SSL in a few clicks) and also watches, protects and controls the
traffic that passes through it:

- **Proxy & TLS:** proxy hosts, redirections, TCP/UDP streams, Let's Encrypt with HTTP-01 and DNS-01
- **Protection:** exploit blocking, security rules, request body inspection, automatic bans, rate limits, challenges
- **Access queue:** a waiting room that keeps your service up when traffic spikes
- **Monitoring:** live traffic, request logs, security events and alerts
- **Easy move:** import an existing Nginx Proxy Manager setup

One container, amd64 and arm64, Apache-2.0. Everything runs on your own server.

```yaml
services:
  corvus:
    image: 'ghcr.io/corvus-gateway/gateway:latest'
    restart: unless-stopped
    ports: ['80:80', '443:443', '9443:9443']
    volumes: ['./data:/data']
```

#### Get involved

Questions and ideas go to [Discussions](https://github.com/corvus-gateway/corvus/discussions).
Looking for a place to start? See the [good first issues](https://github.com/corvus-gateway/corvus/labels/good%20first%20issue)
and [CONTRIBUTING.md](https://github.com/corvus-gateway/corvus/blob/main/CONTRIBUTING.md).
Security reports: [SECURITY.md](https://github.com/corvus-gateway/corvus/blob/main/SECURITY.md).
