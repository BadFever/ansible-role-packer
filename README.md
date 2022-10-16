# ansible-role-packer

Installs [Packer](https://www.packer.io).

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

The Packer version to install.

```YAML
packer_version: "1.8.3-1"
```

The system architecture (e.g. `386` or `amd64`) to use.

```YAML
packer_arch: "amd64"
```

## Dependencies

None.

## Example Playbook

```yml
- hosts: all
  roles:
    - ansible-role-packer
```

## License

MIT
