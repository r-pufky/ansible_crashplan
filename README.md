# Crashplan **Deprecated**
Crashplan installation from public release tarball.

**Deprecated**. This module is no longer maintained.

## Requirements
Pre-existing crashplan.com account. Approximately 1GB of RAM per 1TB for
largest backup set.

Currently [Crashplan 11.x.x stack dumps after authentication](https://old.reddit.com/r/Crashplan/comments/11tfw78/they_borked_it_again_sigh/).
This is a known issue with the current release and is currently being fixed.
Please use the latest 10.x.x version instead, and set `crashplan_auto_upgrades`
to `false` to prevent Crashplan from updating and wedging itself.

## Role Variables
Settings have been throughly documented for usage, including version updates.

[defaults/main.yml](https://github.com/r-pufky/ansible_crashplan/blob/main/defaults/main/main.yml).

### Ports
All ports and protocols have been defined for the role.

Hosts should only define firewall rules for ports they need.

[defaults/ports.yml](https://github.com/r-pufky/ansible_crashplan/blob/main/defaults/main/ports.yml).

## Dependencies
N/A

## Example Playbook
host_vars/crashplan.example.com/vars/crashplan.yml
``` yam
crashplan_memory: 6144
```

site.yml
``` yaml
- name:   'crashplan server'
  hosts:  'crashplan.example.com'
  become: true
  roles:
     - 'r_pufky.crashplan'
```

## Issues
Create a bug and provide as much information as possible.

Associate pull requests with a submitted bug.

## License
[AGPL-3.0 License](https://github.com/r-pufky/ansible_crashplan/blob/main/LICENSE)

## Author Information
https://keybase.io/rpufky
