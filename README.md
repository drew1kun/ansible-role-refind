# Ansible role: refind

[![MIT licensed][mit-badge]][mit-link]
[![Galaxy Role][role-badge]][galaxy-link]

Ansible role which installs and configures [rEFInd][refind-link].

Requirements
----

**NOTE:** Role requires Fact Gathering by ansible!

The role Works with the following Systems:

 - MacOS

**NOTE:** The role requires the MacOS SIP (System Integrity Protection) to be turned off

Role Variables
--------------

| Variable | Description | Default |
|----------|-------------|---------|
| `refind_force_install` | If set to `true` will overwrite the current rEFInd installation | `false` |

Dependencies
----

None.

Example Playbook
----

```yaml
- hosts: "{{ target }}"
  gather_facts: yes
  remote_user: user_1
  roles:
    - roles: drew1kun.refind
      refind_force_install: false
```

Run it like:

```
ansible-playbook refind_playbook.yml --extra-vars "target=macbook"
```

License
----

[MIT][mit-link]

Author Information
----

Andrew Shagayev | [e-mail](mailto:drewshg@gmail.com)

[refind-link]: https://www.rodsbooks.com/refind/
[role-badge]: https://img.shields.io/badge/role-drew1kun.refind-green.svg
[galaxy-link]: https://galaxy.ansible.com/drew1kun/refind/
[mit-badge]: https://img.shields.io/badge/license-MIT-blue.svg
[mit-link]: https://raw.githubusercontent.com/drew1kun/ansible-refind/master/LICENSE
