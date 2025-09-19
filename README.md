# Ansible Homelab

Ansible automation for homelab infrastructure management.

## Structure

```
ansible/
├── playbooks/          # Ansible playbooks
├── inventories/        # Inventory configurations
│   └── homelab/       # Homelab-specific inventory
├── roles/             # Custom roles
├── collections/       # External collections requirements
├── files/            # Static files for deployment
└── ansible.cfg       # Ansible configuration
```

## Usage

Run playbooks from the project root:

```bash
ansible-playbook playbooks/baseline.yml
ansible-playbook playbooks/package_upgrade.yml
```

## Inventory

Host definitions and variables are in `inventories/homelab/`:
- `hosts.ini` - Host definitions
- `group_vars/` - Group-specific variables  
- `host_vars/` - Host-specific variables

## Roles

Custom roles for system and user management:
- `system-*` - System-level configurations
- `user-*` - User management tasks