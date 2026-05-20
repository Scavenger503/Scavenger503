# Hey, I'm Scavenger 👋

Infrastructure engineer, self-hosting enthusiast, and perpetual homelab builder. I design and operate production-grade infrastructure, build security automation pipelines, and document everything I break and fix along the way.

---

## 🖥️ What I Run

A multi-node homelab running 80+ self-hosted services across dedicated physical machines, a Synology NAS with vDSM, and a Raspberry Pi — all managed as a unified environment.

| Machine | Role |
|---|---|
| Lenovo M710q | Primary Docker host — Ghost, N8N, Linkwarden, Mattermost, and more |
| Lenovo M715q | Security & DevOps — Wazuh SIEM, agent monitoring |
| Synology DS923+ | NAS — backups, storage, Jellyfin |
| vDSM (on DS923+) | Monitoring stack — Uptime Kuma, Ntopng, VoidWatch Bot |
| Raspberry Pi | DNS & DHCP — AdGuard Home |
| Proxmox Node | Virtualization testing |
| Fedora 43 KDE | Daily driver |

All external access via Cloudflare Tunnels — zero open inbound ports.

---

## 🚀 Featured Projects

| Project | Description | Status |
|---|---|---|
| [HomeLab](https://github.com/Scavenger503/HomeLab) | Production Docker stacks powering a multi-node self-hosted homelab | ✅ Active |
| [wazuh-n8n-security-pipeline](https://github.com/Scavenger503/HomeLab/tree/main/Phase-2) | Automated SIEM alerting — Wazuh → N8N → Claude AI → Telegram | ✅ Live |
| [ntopng-n8n-security-pipeline](https://github.com/Scavenger503/HomeLab/tree/main/NTOPNG-Alerts) | Network threat detection — Ntopng → N8N → Luna AI → Telegram | ✅ Live |

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
- Escalates critical alerts (score ≥ 50 or blacklisted IPs) via Ntfy push notification — bypasses Do Not Disturb for urgent threats

---

## 🛡️ Security Stack

- **Wazuh SIEM** — log aggregation, threat detection, file integrity monitoring across all nodes
- **Ntopng** — real-time network flow analysis with active threat intelligence feeds (Abuse.ch, Emerging Threats, IPsum)
- **VoidWatch Bot** — Telegram bot for Ntopng network alerts
- **Luna AI** — Claude-powered alert triage and SOC analysis
- **AdGuard Home** — DNS-level filtering across the entire network
- **Cloudflare WAF** — edge protection for all public-facing services
- **Uptime Kuma** — service availability monitoring with instant alerting

---

## 🎯 Currently Working On

- ☸️ K3s cluster deployment for hands-on Kubernetes practice
- 📜 Terraform Associate (004) certification
- ☁️ AWS Cloud Practitioner certification
- 🔒 Expanding Luna AI capabilities across additional alert sources
- 📦 Immich migration to vDSM for self-hosted family photo management

---

## 📜 Certifications in Progress

- HashiCorp Terraform Associate
- Certified Kubernetes Administrator (CKA)
- GitHub Actions
- AWS Cloud Practitioner

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

`Docker` `Portainer` `Cloudflare` `Wazuh` `N8N` `Ntopng` `AdGuard Home` `Synology DSM` `Proxmox` `Ghost CMS` `Fedora Linux` `Bash` `YAML` `Git` `Terraform` `Kubernetes`

---

*Building in public. Breaking things on purpose.*
