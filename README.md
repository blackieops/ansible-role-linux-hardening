# Security Baseline: Linux Hardening

This is an [Ansible][a] role that sets a OS security baseline for Linux
systems. This does **not** cover any specific software such as SSH or
firewalls, rather is only configuration and permissions for the OS itself.

[a]: https://ansible.com

## Supported Platforms

While these tasks should be generic enough to work most Linux-based operating
systems, we specifically target:

* Debian (Stable)
* Ubuntu Server (LTS)
* Enterprise Linux (RHEL-derived)

## Usage

This role is currently not available on Ansible Galaxy, but you can use it
directly as a submodule:

```
git submodule add https://github.com/blackieops/ansible-linux-hardening roles/linux_hardening
```

Then reference it in your playbook normally:

```yaml
- hosts: all
  roles:
    - { role: linux_hardening }
```
