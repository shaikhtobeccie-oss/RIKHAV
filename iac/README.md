# Network IaC with Ansible

Infrastructure-as-Code project for managing network device configuration using Ansible.

## Goal

Use Ansible to automate the configuration management of network devices (switches, routers, firewalls, etc.) instead of manual CLI changes — enabling consistent, repeatable, and version-controlled network configs.

## Status

🚧 **Day 1** — Project initiated. Setting up repo structure and planning the Ansible-based workflow.

## Planned Project Structure

```
iac/
├── inventories/        # Host inventories (per environment: dev, staging, prod)
│   └── dev/
│       ├── hosts.yml
│       └── group_vars/
├── playbooks/          # Ansible playbooks
├── roles/              # Reusable Ansible roles
├── group_vars/         # Variables shared across groups of devices
├── host_vars/          # Variables specific to individual devices
├── ansible.cfg         # Ansible configuration
└── README.md
```

## Prerequisites

- Ansible installed on the control node (`pip install ansible`)
- SSH/network access to target devices
- Appropriate Ansible network collections (e.g. `ansible-galaxy collection install cisco.ios`, `arista.eos`, `junipernetworks.junos`, etc. — to be decided based on target device vendor)

## Roadmap

- [ ] Day 1: Initialize repo, write README, plan structure
- [ ] Define inventory for target network devices
- [ ] Install required Ansible network collections
- [ ] Write first playbook (e.g. gather facts / backup running config)
- [ ] Implement config push/validation workflow
- [ ] Add CI checks (lint, syntax-check, dry-run)

## Notes

This README will be updated as the project progresses — each day's work and decisions will be logged here or in a `docs/` folder as the project grows.
