# Linux Ansible Automation

Ansible playbooks for provisioning and configuring Linux environments — including security labs, vulnerable app deployments, and general system setup.

## Purpose

Automate repeatable Linux configuration tasks across different distros and use cases. Built to support both offensive security lab environments (Kali) and general-purpose Linux VMs (Ubuntu, etc.).

## Playbooks

| Playbook | Target | Description |
|---|---|---|
| `playbooks/bootstrap-kali.yml` | `[kali_lab]` | Baseline a Kali Linux VM with tools and config for OSCP / CTF work |
| `playbooks/setup-dvwa.yml` | `[ubuntu_lab]` | Install XAMPP and deploy the OWASP Vulnerable Web Application |

## Usage

1. Copy the inventory template and fill in your hosts:
   ```bash
   cp inventory/hosts.example inventory/hosts
   ```

2. Run a playbook:
   ```bash
   ansible-playbook playbooks/<playbook>.yml --ask-become-pass
   ```

## Requirements

- Ansible installed on your control machine
- SSH key-based auth configured to target hosts (see `ansible.cfg` for key path)
- Target hosts reachable on the network

## Inventory

Host definitions live in `inventory/hosts` (git-ignored — see `inventory/hosts.example` for the format).

## Disclaimer

For educational use and authorized testing only.
