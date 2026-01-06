# Ulauncher-user-config-Role

[![Almalinux9-CI](https://github.com/philnewm/ansible-ulauncher-user-config/actions/workflows/almalinux9-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-ulauncher-user-config/actions/workflows/almalinux9-ci-caller.yml) [![Rocky9-CI](https://github.com/philnewm/ansible-ulauncher-user-config/actions/workflows/rocky9-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-ulauncher-user-config/actions/workflows/rocky9-ci-caller.yml) [![CentOSStream9-CI](https://github.com/philnewm/ansible-ulauncher-user-config/actions/workflows/centosstream9-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-ulauncher-user-config/actions/workflows/centosstream9-ci-caller.yml) [![Fedora43-CI](https://github.com/philnewm/ansible-ulauncher-user-config/actions/workflows/fedora43-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-ulauncher-user-config/actions/workflows/fedora43-ci-caller.yml)<br>
[![Ubuntu2404-CI](https://github.com/philnewm/ansible-ulauncher-user-config/actions/workflows/ubuntu2404-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-ulauncher-user-config/actions/workflows/ubuntu2404-ci-caller.yml) [![Debian13-CI](https://github.com/philnewm/ansible-ulauncher-user-config/actions/workflows/debian13-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-ulauncher-user-config/actions/workflows/debian13-ci-caller.yml)

Role description

This role applies a bunch of custom settings as well as a [forked theme](https://github.com/philnewm/ulauncher_theme).<br>
It will also work for XOrg and Wayland since this requires a few [adjustments](https://github.com/Ulauncher/Ulauncher/wiki/Hotkey-In-Wayland) when it comes to the configured hotkey.

This role includes a molecule testing setup as a submodule at `molecule/`

## Structure

```code
📦 ansible-ulauncher-user-config
 ┣ 📂 defaults
 ┃ ┗ 📜 main.yml
 ┣ 📂 meta
 ┃ ┗ 📜 main.yml
 ┣ 📂 molecule
 ┃ ┗ 📂 default
 ┃   ┗ 📜, 📜, 📜, scenario_files
 ┣ 📂tasks
 ┃ ┣ 📜absent.yml
 ┃ ┣ 📜main.yml
 ┃ ┣ 📜present.yml
 ┃ ┣ 📜tests.yml
 ┃ ┣ 📜themes.yml
 ┃ ┗ 📜wayland.yml
 ┗ 🗒️ README.md

```

Describe and explain role structure.

## Requirements

Elaborate external dependencies and how to use them.

## Role Variables

* defaults/main.yml
  * first_var
  * sec_var
  * third_var
* vars/main.yml
  * first_var
  * sec_var
  * third_var

## Dependencies

List role ansible-galaxy dependencies - if any.

## Example Playbook

Add an example playbook

```yaml
---

tasks:
  - name: Include ansible-ulauncher-user-config present
    ansible.builtin.include_role:
      name: ansible-ulauncher-user-config
    vars:
      state: present

...
```

## License

Add license - if any.

## Notes

Includes special git configuration for submodule files that are most likely to get local overrides
`.git/info/attributes`

```code
molecule/default/cleanup.yml merge=ours
molecule/default/converge.yml merge=ours
molecule/default/verify.yml merge=ours
```

## Changes to role template

* Add github action that flags empty directories on release creation
