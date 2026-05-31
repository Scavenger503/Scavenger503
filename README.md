# Hey, I'm Scavenger 👋

Infrastructure engineer, self-hosting enthusiast, and perpetual homelab builder. I design and operate production-grade infrastructure, build security automation pipelines, and document everything I break and fix along the way.

---

## 🖥️ What I Run

A multi-node homelab running 80+ self-hosted services across dedicated physical machines, a Synology NAS with vDSM, and a Raspberry Pi — all managed as a unified environment.

| Machine | Role |
|---|---|
| Lenovo M710q | Primary Docker host — Ghost, N8N, Linkwarden, and more |
| Lenovo M715q (DevOps) | Security & DevOps — Wazuh SIEM, agent monitoring |
| Lenovo M715q (K3s) | Dedicated K3s cluster node — Kubernetes workloads |
| Synology DS923+ | NAS — backups, storage, vDSM |
| vDSM (on DS923+) | Monitoring stack — Uptime Kuma, Ntopng, VoidWatch Bot |
| Raspberry Pi | DNS & DHCP — AdGuard Home (dual instance) |
| Proxmox Node | Virtualization testing |
| Fedora 43 KDE | Daily driver |

All external access via Cloudflare Tunnels — zero open inbound ports.

---

## 🚀 Featured Projects

| Project | Description | Status |
|---|---|---|
| [HomeLab](https://github.com/Scavenger503/HomeLab) | Production infrastructure across Docker, Kubernetes, and Proxmox | ✅ Active |
| [K3s Cluster](https://github.com/Scavenger503/HomeLab/tree/main/K3s) | GitOps-managed Kubernetes cluster with Prometheus/Grafana monitoring | ✅ Live |
| [Wazuh AI Security Pipeline](https://github.com/Scavenger503/HomeLab/tree/main/Phase-2) | Automated SIEM alerting — Wazuh → N8N → Luna AI → Telegram | ✅ Live |
| [NTOPNG-Alerts](https://github.com/Scavenger503/NTOPNG-Alerts) | Network threat detection — Ntopng → N8N → Luna AI → Telegram | ✅ Live |
| 🛡️ [Guardian](https://github.com/Scavenger503/Guardian) | ✅ Live | A lightweight Docker container update watcher written in Go. Built as a self-hosted replacement for the now-archived Watchtower. Monitors labeled containers, compares SHA digests, and automatically pulls and restarts updated images — with Telegram notifications at every step.

- Published on [Docker Hub](https://hub.docker.com/r/scavenger503/guardian) and GHCR
- CI/CD via GitHub Actions
- Non-root container, label opt-in, digest-based comparison

`Go` `Docker` `GitHub Actions` `Self-hosted` `Open Source`

---

## ☸️ K3s Kubernetes Cluster

A production K3s cluster running on dedicated hardware, fully managed via GitOps using ArgoCD. All workloads are defined as Kubernetes manifests stored in GitHub — changes auto-sync to the cluster.

**Live public access:**
- 🏠 [k3s-homepage.scavenger.pro](https://k3s-homepage.scavenger.pro) — Cluster dashboard
- 📊 [k3s-grafana.scavenger.pro](https://k3s-grafana.scavenger.pro) — Prometheus/Grafana monitoring (anonymous viewer)
- 🔀 [ArgoCD](https://github.com/Scavenger503/HomeLab/blob/main/K3s/K3s%20argocd.md) — GitOps pipeline (documented on GitHub)

**Stack:**
```
GitHub (source of truth)
    │
    ▼
ArgoCD (GitOps controller)
    ├── Homepage
    ├── Prometheus + Grafana
    └── Traefik ingress

Cloudflare Tunnel → Traefik → Kubernetes pods
```

**Documentation:** [K3s Setup Guides](https://github.com/Scavenger503/HomeLab/tree/main/K3s)

---

## 🤖 Luna AI — Security Intelligence Layer

Luna is my AI-powered security analyst running inside N8N. She receives raw alerts from Wazuh (SIEM) and Ntopng (network traffic monitor), analyzes them in real time, and delivers plain-English SOC-style triage reports directly to Telegram — including threat assessment, context, and recommended actions.

**Pipeline:**
```
Wazuh SIEM ──────┐
                  ├──▶ N8N Webhook ──▶ Luna (Claude API) ──▶ Telegram
Ntopng Alerts ───┘
```

**What Luna does:**
- Receives security alerts from two independent monitoring sources
- Enriches each alert with AI-powered triage analysis
- Delivers structured SOC-style reports including severity, confidence, and recommended actions
- Operates 24/7 autonomously — catching real production events overnight without intervention
- Escalates critical alerts via push notification — bypasses Do Not Disturb for urgent threats

---

## 🛡️ Security Stack

- **Wazuh SIEM** — log aggregation, threat detection, file integrity monitoring across all nodes
- **Ntopng** — real-time network flow analysis with active threat intelligence feeds (Abuse.ch, Emerging Threats, IPsum)
- **VoidWatch Bot** — Telegram bot for Ntopng network alerts
- **Luna AI** — Claude-powered alert triage and SOC analysis
- **AdGuard Home** — DNS-level filtering across the entire network (dual instance for redundancy)
- **Cloudflare WAF** — edge protection for all public-facing services
- **Uptime Kuma** — service availability monitoring with instant alerting

---

## 🎯 Currently Working On

- ☸️ K3s cluster — adding Falco runtime security monitoring
- 🛡️ Guardian — custom container image update manager (Watchtower replacement)
- 📜 Terraform Associate (004) certification
- ☁️ AWS Cloud Practitioner certification
- 🔒 CompTIA Security+
- 📦 Immich migration to vDSM for self-hosted photo management

---

## 📜 Certifications in Progress

- HashiCorp Terraform Associate
- Certified Kubernetes Administrator (CKA)
- AWS Cloud Practitioner
- CompTIA Security+
- GitHub Actions

---

## 🌐 Links

- 🌍 World of Hackers — [worldofhackers.io](https://worldofhackers.io)
- 🎵 Zyntherix Music — [zyntherixmusic.com](https://zyntherixmusic.com)
- 🎙️ DarkHours FM — [darkhoursfm.com](https://darkhoursfm.com)
- 🔗 Scavvy Link Shortener — [go.scavenger.pro](https://go.scavenger.pro)
- 💬 The Quote Codex — [wisdom.scavenger.pro](https://wisdom.scavenger.pro)
- 📖 Scavenger Stories — [stories.scavenger.pro](https://stories.scavenger.pro)
- 👤 About Me — [about.scavenger.pro](https://about.scavenger.pro)

---

## 🧰 Tech Stack

`Docker` `Kubernetes (K3s)` `Portainer` `ArgoCD` `Helm` `Prometheus` `Grafana` `Cloudflare` `Wazuh` `N8N` `Ntopng` `AdGuard Home` `Synology DSM` `Proxmox` `Ghost CMS` `Fedora Linux` `Bash` `YAML` `Git` `Terraform` `Traefik`

---

*Building in public. Breaking things on purpose. Documenting everything.*
