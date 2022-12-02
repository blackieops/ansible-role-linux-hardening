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

Install the role by adding either the Ansible Galaxy package or Git remote to
your `requirements.yml`:

```yaml
# via Galaxy
- src: blackieops.linux_hardening

# or via Git
- src: https://github.com/blackieops/ansible-role-linux-hardening.git
```

Then install it with `ansible-galaxy`:

```
$ ansible-galaxy install -r requirements.yml
```

Finally, you can reference the role in your playbooks:

```yaml
- hosts: all
  roles:
    - { role: blackieops.linux_hardening }
```
