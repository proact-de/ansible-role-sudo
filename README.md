# Role Name

Installs and configures sudo. By default sets up two groups, which will be granted sudo access: one with password and one without.

## Requirements

None. The neccessary groups are created, if they do not exist.

## Role Variables

* tmxsudo_allow_group: sudo
  * Controls the group of users, who are allowed to use sudo *WITH* password. Default "sudo".
* tmxsudo_nopasswd_group: sudonopw
  * Control the group of users, who are allowed to use sudo *WITHOUT* password. Default "sudonopw".

## Dependencies

None.

## Example Playbook

```yml
- hosts: servers
  roles:
     - { role: proactcloud.sudo, tmxsudo_allow_group: tmxsudo, tmxsudo_nopasswd_group: tmxnopw }
```

## License

internal

## Author Information

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
