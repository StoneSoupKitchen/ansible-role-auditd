[![CI](https://github.com/StoneSoupKitchen/ansible-role-auditd/actions/workflows/ci.yml/badge.svg)](https://github.com/StoneSoupKitchen/ansible-role-auditd/actions/workflows/ci.yml)

# Ansible role: auditd

An Ansible role for configuring auditd.

## Requirements

Supported operating systems:
* Debian 10 (Buster)
* Debian 11 (Bullseye)

## Role Variables

The following table lists all variables that can be overridden
and their default values.

| Name                     | Default Value | Description                      |
| ------------------------ | ------------- | -------------------------------- |
| `auditd_package` | auditd | Name of the auditd package. Use `name=ver` format to pin. |
| `auditd_package_state` | present | Installation state for the auditd package. |
| `auditd_plugins_package` | audispd-plugins | Name of the auditd plugins package. Use `name=ver` format to pin. |
| `auditd_plugins_package_state` | present | Installation state for the auditd plugins package. |

## Examples

```yaml
- hosts: all
  roles:
    - stonesoupkitchen.auditd
```

## Development

A Makefile is included for easier development with `pipenv`.
After cloning this repository,
use the following commands to set up an environment.

    pipenv install --dev

To lint your changes with ansible-lint:

    make lint

To run tests with molecule:

    make test

## License

See [LICENSE](./LICENSE).

