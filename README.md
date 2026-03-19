Kali Linux Baseline Automation (OSCP / CTF)

This repository contains Ansible playbooks used to baseline and configure a Kali Linux environment for OSCP preparation, CTFs, and offensive security labs.

Purpose

Quickly rebuild a consistent Kali setup without manual configuration. Designed to be repeatable, fast, and aligned with offensive security workflows.

What It Does

Updates and upgrades the system

Installs common offensive security tools (nmap, gobuster, metasploit, hydra, impacket, etc.)

Sets up Python and scripting environment

Configures user environment (aliases, directories, workflow structure)

Optionally applies basic system hardening

Usage

Clone the repository

Update the inventory file (if needed)

Run the playbook:

ansible-playbook -i inventory/hosts.ini playbooks/bootstrap-kali.yml --ask-become-pass

Requirements

Kali Linux

Ansible

Goal

Spin up a fresh Kali VM and fully configure it in minutes with a consistent toolset and environment.

Disclaimer

For educational use and authorized testing only.
