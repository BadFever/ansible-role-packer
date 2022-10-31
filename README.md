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

The packer repository url.

```YAML
packer_repo_url: https://apt.releases.hashicorp.com
```

The packer apt release channel.

```YAML
packer_apt_release_channel: main
```

The system architecture (e.g. `386` or `amd64`) to use.

```YAML
packer_apt_arch: "{{ 'arm64' if ansible_architecture == 'aarch64' else 'amd64' }}"
```

The packer apt repository.

```YAML
packer_apt_repository: "deb [arch={{ packer_apt_arch }}] {{ packer_repo_url }} {{ ansible_distribution_release }} {{ packer_apt_release_channel }}"
```

The packer apt gpg key.

```YAML
packer_apt_gpg_key:  https://apt.releases.hashicorp.com/gpg
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
