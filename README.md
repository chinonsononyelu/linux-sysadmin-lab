# Linux Systems Administration & Automation Lab

A hands-on, multi-node Linux lab built on UTM simulating enterprise server
operations across RHEL and Ubuntu environments. This lab covers user and group
management, SSH hardening, sudo policy enforcement, firewall configuration, systemd
service management, centralized logging, infrastructure monitoring, container
management, configuration management automation, and real-world troubleshooting.
It served as the primary preparation environment for the Red Hat Certified System
Administrator (RHCSA) exam, passed in February 2026.

---

## Lab Environment

| Component    | Node 1 — RHEL                                                                  | Node 2 — Ubuntu                                                                 |
|--------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| OS           | RHEL 9.8                                                                       | Ubuntu 26.04 LTS                                                                |
| Hostname     | rhel-node                                                                      | ubuntu-node                                                                     |
| Virtualization | UTM 4.7.4                                                      | UTM 4.7.4                                                         |
| Host OS      | Mac OS                                                                      | Mac OS                                                                      |
| Resources    | 2 vCPUs, 4 GB RAM, 40 GB                                                       | 2 vCPUs, 4 GB RAM, 40 GB                                                        |
| Primary Role | RHCSA practice, firewalld, systemd, SELinux, user mgmt, centralized log server | Bash automation, monitoring stack, Docker, Ansible control node, log forwarding |

---

## Network Architecture

Both VMs use an Host-Only for node-to-node communication with
static IPs. A separate NAT adapter provides internet access for package downloads.

| Adapter  | Type             | Purpose                        |
|----------|------------------|--------------------------------|
| enp0s2   | Host-Only        | Lab communication (192.168.70.x)|
| enp0s1   | Shared/NAT       | Internet access for downloads  |



---
