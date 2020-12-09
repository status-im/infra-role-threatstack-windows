# Description

This role configures the [ThreatStack](https://threatstack.com) Windows client software which enables monitoring activity going on on hosts and docker containers for suspicious activity.

# Requirements

It does assume you have access to the `cloud/ThreatStack/deploy-key` through [password-store](https://www.passwordstore.org/) from [infra-pass](https://github.com/status-im/infra-pass).

# Usage

Simply insteall the [`infra-role-threatstack-windows`](https://github.com/status-im/infra-role-threatstack-windows) role via `ansible-galaxy`:

```yaml
- name: threatstack-windows
  src: git@github.com:status-im/infra-role-threatstack-windows.git
  scm: git

```
And use it in an Ansible playbook:
```yaml
- name: Configure Threatstack
  hosts: some-hosts
  roles:
    - threatstack-windows
```

# Details

Instructions used: https://threatstack.zendesk.com/hc/en-us/articles/360028693491
