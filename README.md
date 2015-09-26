# ansible-common
----------------
An Ansible directory structure for performing common functions for any new server

# What it does
--------------

_See roles/common/tasks/main.yml_

1. Update apt
2. Set Timezone
3. Set NTP
4. Create users
5. Setup and enable swap
6. SSH hardening
7. Setup iptables firewall
8. Install/configure fail2ban
9. Setup apt auto-upgrade for security patches
10. Install list of defined packages

# Usage
-------

### Clone this repo
```
git clone https://github.com/jeremymturner/ansible-common.git
```

### Add hostnames to hosts file (optionally add IP addresses if hostnames do not resolve in DNS)
```
vim hosts/manual
```

### Update timezone, if desired
```
vim group_vars/all
```

### Update list of packages to install, if desired
```
vim group_vars/all
```

### Add user(s) and SSH key(s) (Required, root ssh access will be removed)
```
vim group_vars/all
```

### Run the playbook
```
ansible-playbook main.yml
```
