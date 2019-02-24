# ansible-role-packer

[![Build Status](https://travis-ci.org/BadFever/ansible-roler-packer.svg?branch=master)](https://travis-ci.org/BadFever/ansible-roler-packer)

Installs [Packer](https://www.packer.io).

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

The Packer version to install.

```YAML
packer_version: "1.3.4"
```

The system architecture (e.g. `386` or `amd64`) to use.

```YAML
packer_arch: "amd64"
```

The packer binary location.

```YAML
packer_bin_path: /usr/local/bin
```

## Dependencies

None.

## Example Playbook

    - hosts: all
      roles:
        - ansible-role-packer

## License

MIT
