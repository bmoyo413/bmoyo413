<div align="center">

# Blessings Moyo

`junior linux sysadmin` · `homelabber` · `northern virginia`

[![Site](https://img.shields.io/badge/bmoyo.dev-b2ed91?style=for-the-badge&logo=googlechrome&logoColor=101415)](https://bmoyo.dev)
[![Linux+](https://img.shields.io/badge/CompTIA-Linux%2B-b2ed91?style=for-the-badge&labelColor=1d2526)](https://www.credly.com/badges/ce0b6b3d-195a-48b9-aad5-825786be2b58/public_url)
[![Security+](https://img.shields.io/badge/CompTIA-Security%2B-b2ed91?style=for-the-badge&labelColor=1d2526)](https://www.credly.com/badges/0f0c2be2-a5be-4e9e-8fc5-0abd2aa1af09/public_url)
[![Lab](https://img.shields.io/badge/lab-rebuilding-354244?style=for-the-badge&labelColor=1d2526&logo=proxmox&logoColor=b2ed91)](#-systemctl-status-homelab)

**Open to work** · Linux systems administration, IT support, and infrastructure roles · [jobs@bmoyo.dev](mailto:jobs@bmoyo.dev)

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

| area | tools |
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
