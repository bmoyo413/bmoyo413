<div align="center">

# Blessings Moyo

`junior linux sysadmin` · `homelabber` · `northern virginia`

[![Site](https://img.shields.io/badge/bmoyo.dev-1a1b26?style=for-the-badge&logo=googlechrome&logoColor=7aa2f7)](https://bmoyo.dev)
[![Linux+](https://img.shields.io/badge/CompTIA-Linux%2B-1a1b26?style=for-the-badge&labelColor=c8102e)](https://www.comptia.org/certifications/linux)
[![Security+](https://img.shields.io/badge/CompTIA-Security%2B-1a1b26?style=for-the-badge&labelColor=c8102e)](https://www.comptia.org/certifications/security)
[![Lab](https://img.shields.io/badge/lab-rebuilding-1a1b26?style=for-the-badge&logo=proxmox&logoColor=e0af68)](#-systemctl-status-homelab)

</div>

```console
$ whoami
Blessings Moyo. I keep Linux servers patched, monitored, and boring.

$ cat ~/experience
RHEL across 10+ client production environments as a contract jr. sysadmin:
Ansible, patching, user and sudo policy for 20+ users, Nagios and Grafana.
Today: IT and operations support, SaaS admin, phone support for field techs.
```

---

## `$ systemctl status homelab`

```console
● homelab.target - two Proxmox VE nodes on ZFS
     Active: degraded (rebuild in progress)

     node 1  active (running)   media VM, Jellyfin, Pi-hole + Unbound, RustDesk server
     node 2  inactive (dead)    offline, first in line to be rebuilt from code
```

I am rebuilding the lab from bare metal, this time from one repo that builds it instead of describing it. That repo goes public once the first node runs from it, and this page will link to it then.

---

## `$ git show v1`

The first build was a two-node Proxmox cluster running Docker Compose stacks: Caddy with Let's Encrypt over Cloudflare DNS-01, Authentik SSO over OIDC, Gitea, Vaultwarden, Prometheus, Grafana, Loki, and Alloy, with Alertmanager paging my phone through ntfy. DNS ran on Pi-hole + Unbound on both nodes, and media ran an arr stack over WireGuard plus Jellyfin.

It lives on, archived, at **[bmoyo413/homelab](https://github.com/bmoyo413/homelab)**.

---

## `$ ls ~/toolbox`

| | |
|---|---|
| **servers** | RHEL, Rocky, CentOS, Ubuntu, Debian, Proxmox VE |
| **automation** | Ansible, Bash, Git, cron |
| **containers** | Docker, Docker Compose |
| **observability** | Prometheus, Grafana, Loki, Alloy, Alertmanager, Nagios, ntfy |
| **networking** | DNS (Pi-hole + Unbound), Caddy, WireGuard, NFS, TLS, Let's Encrypt |
| **access** | SSH keys, sudo and RBAC, firewalld, hardening, Authentik SSO (OIDC) |
| **storage** | ZFS (mirror and RAIDZ1), LVM |
| **ci / iac** | GitHub Actions, Terraform (Proxmox, Tailscale), Sigstore/Cosign |
| **ticketing** | osTicket, Jira |

<div align="center"><sub><code>$ exit 0</code></sub></div>
