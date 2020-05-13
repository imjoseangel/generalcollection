# skel role

Creates Skel for Ansible roles. Use the following `ansible-galaxy' command:

```bash
ansible-galaxy init --init-path=roles/ --role-skeleton=roles/skel/ mynewrole
```

## Requirements

ansible >= 2.9.x

## Variables

None

## Dependencies

No direct dependencies.

## Example Playbook

eg:

```yaml
---
- name: Ansible
  hosts: localhost
  connection: local
  gather_facts: false


  collections:
    - imjoseangel.general

  vars:

    variable1: value

  tasks:

    - name: Collection Module Test
      collection_test:
        name: Hello World
        new: False

    - name: Include role
      include_role:
        name: dummycollection
      vars:
        dummy:
          name: test
        action_dummy: deploy
```

## License

MIT

## Author Information

imjoseangel
