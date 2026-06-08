---
title: "What Can I Put in My Homelab? Project Ideas for Every Skill Level"
description: "A roundup of practical services and projects to run in a homelab, from beginner-friendly media servers to advanced self-hosted infrastructure."
pubDate: "Jun 08 2026"
heroImage: "/blog-placeholder-1.jpg"
---

So you've got a spare machine, an old laptop, or a Raspberry Pi gathering dust — what should you actually run on it? Here's a breakdown of homelab projects organized roughly by how much effort they take to set up and maintain.

## Beginner-friendly projects

These are great starting points if you're new to self-hosting. They're well-documented, low-maintenance, and immediately useful.

- **Network-wide ad blocking** — Pi-hole or AdGuard Home intercept DNS requests and block ads/trackers for every device on your network, not just your browser.
- **Media server** — Jellyfin or Plex turn a folder of movies, shows, and music into a Netflix-style streaming experience for your household.
- **File storage and sync** — Nextcloud or Syncthing give you your own private Dropbox/Google Drive without a subscription.
- **Photo backup** — Immich or PhotoPrism automatically back up and organize photos from your phone, with face recognition and search.
- **Password manager** — Vaultwarden (a lightweight Bitwarden-compatible server) keeps your credentials in your own hands.

## Intermediate projects

Once you're comfortable with the basics, these add more moving parts — reverse proxies, databases, or scheduled jobs.

- **Reverse proxy with automatic HTTPS** — Caddy, Traefik, or Nginx Proxy Manager let you run multiple services behind clean subdomains with free TLS certificates.
- **Home automation hub** — Home Assistant ties together smart home devices (lights, sensors, thermostats) into dashboards and automations that don't depend on a vendor's cloud.
- **Personal dashboard** — Homepage, Homarr, or Heimdall give you a single landing page linking to all your self-hosted services.
- **Download automation ("the *arr stack")** — Sonarr, Radarr, and Prowlarr automate fetching and organizing media to feed into Jellyfin/Plex.
- **Bookmark and read-it-later tools** — Linkding or Wallabag replace browser bookmark sprawl with a searchable, self-hosted archive.
- **Git hosting** — Gitea or Forgejo give you a lightweight, self-hosted GitHub alternative for personal projects.

## Advanced projects

These involve more architecture decisions — clustering, monitoring, automation pipelines — and reward you with deeper infrastructure skills.

- **Container orchestration** — Move from `docker compose` to Docker Swarm or a lightweight Kubernetes distro (k3s, MicroK8s) to learn how production infrastructure is actually run.
- **Monitoring and alerting** — Prometheus + Grafana (or the simpler Uptime Kuma) give you dashboards and alerts for every service and host in your lab.
- **Centralized logging** — The Grafana Loki stack or an ELK/EFK setup aggregates logs from all your machines and containers in one searchable place.
- **Infrastructure as code** — Manage your homelab with Ansible, Terraform, or Proxmox + cloud-init so rebuilding a host is a single command instead of a weekend project.
- **VPN and remote access** — WireGuard or Tailscale let you securely reach your homelab from anywhere without opening ports to the internet.
- **Virtualization platform** — Proxmox VE or XCP-ng let a single physical box host dozens of VMs and containers, each isolated and independently manageable.
- **Backup and disaster recovery** — Restic, Borg, or Proxmox Backup Server give you versioned, encrypted backups — and a chance to practice actually restoring them.

## A few tips before you dive in

1. **Start small.** Pick one service, get it running reliably, and only then add the next. A homelab with three solid services beats one with twenty flaky ones.
2. **Use Docker Compose early.** It makes services reproducible, easy to tear down, and easy to document — which matters a lot once you have more than a handful running.
3. **Write down your setup.** Future-you will not remember why you opened that port or what password you used. Even a simple Markdown file per service helps enormously.
4. **Plan your storage before you need it.** Media libraries and backups grow faster than you expect — think about redundancy (RAID, ZFS, or simple periodic backups) from the start.
5. **Segment your network.** Put your homelab on its own VLAN or subnet so a compromised service can't reach the rest of your home network.

Whatever you choose, the real value of a homelab isn't the services themselves — it's the hands-on experience with networking, storage, automation, and security that you simply can't get any other way.
