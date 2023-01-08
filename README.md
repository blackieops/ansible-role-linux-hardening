# Security Baseline: Linux Hardening

[![Molecule Tests](https://github.com/blackieops/ansible-role-linux-hardening/actions/workflows/test.yml/badge.svg)](https://github.com/blackieops/ansible-role-linux-hardening/actions/workflows/test.yml)

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

## Configuration

The defaults should provide a solid baseline for the majority of systems,
however if you have specific needs you can configure some of the specifics.

Check [the vars set in `defaults`][def] for an accounting and example of which
tasks you can configure.

[def]: ./defaults/main.yml
