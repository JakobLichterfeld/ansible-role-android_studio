# Ansible Role: Android Studio

Install Android Studio via download.

- Install required libraries for 64-bit machines
- Download and verify (sha256) the specified Android Studio
- Install to `/opt`

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

| Name           | Default Value   | Description                        |
| -------------- | --------------- | -----------------------------------|
| `download_dir_on_remote_host` | "/home/{{ ansible_user }}/Downloads/automatically_by_ansible_playbook" | Download Base Directory on Remote Host |
| `android_studio.version` | "2022.3.1.19" | Android Studio Version you want to install |
| `android_studio.checksum` | "sha256:250625dcab183e0c68ebf12ef8a522af7369527d76f1efc704f93c05b02ffa9e" | Checksum of the version to be downloaded |

## Dependencies

None.

## Example Playbook

```yaml
---
- hosts: all
  gather_facts: yes
  become: true

  roles:
    - role: jakoblichterfeld.android_studio

```

## License

MIT

## Author Information

This role was created in 2023 by [Jakob Lichterfeld](https://github.com/JakobLichterfeld).
