# Ansible Role: CloudPanel on Ubuntu 24.04

This Ansible role installs **CloudPanel (Community Edition v2)** on an Ubuntu 24.04 server. It also optionally creates an admin user using the `clpctl` command-line tool.

---

## Supported Platforms

- ✅ Ubuntu 24.04 (Noble Numbat)

> ℹ️ Requires internet access and root privileges (`become: true`).

---

## Role Variables

```yaml
cloudpanel_admin_user: "admin"
cloudpanel_admin_email: "admin@example.com"
cloudpanel_admin_first_name: "John"
cloudpanel_admin_last_name: "Doe"
cloudpanel_admin_pass: "SuperSecretPassword123"
cloudpanel_admin_tz: "Europe/Berlin"
```


## Example Playbook
```yaml
- name: Install CloudPanel on Ubuntu 24.04
  hosts: cloudpanel
  become: true

  roles:
    - role: cloudpanel

  vars:
    cloudpanel_admin_user: "admin"
    cloudpanel_admin_email: "admin@example.com"
    cloudpanel_admin_first_name: "John"
    cloudpanel_admin_last_name: "Doe"
    cloudpanel_admin_pass: "SuperSecretPassword123"
    cloudpanel_admin_tz: "Europe/Berlin"
```