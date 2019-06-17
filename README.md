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

Copyright 2019 Proact Deutschland GmbH

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

<http://www.apache.org/licenses/LICENSE-2.0>

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

## Author Information

Patrick Dreker <patrick.dreker@proact.de>
