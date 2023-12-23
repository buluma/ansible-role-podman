# [Ansible role podman](#podman)

Install and configure Podman on your system.

|GitHub|Version|Issues|Pull Requests|
|------|-------|------|-------------|
|[![github](https://github.com/buluma/ansible-role-podman/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-podman/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-podman.svg)](https://github.com/buluma/ansible-role-podman/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-podman.svg)](https://github.com/buluma/ansible-role-podman/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-podman.svg)](https://github.com/buluma/ansible-role-podman/pulls/)|

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/buluma/ansible-role-podman/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: converge
  hosts: all
  become: yes
  gather_facts: yes

  roles:
    - role: buluma.podman
```

The machine needs to be prepared. In CI this is done using [`molecule/default/prepare.yml`](https://github.com/buluma/ansible-role-podman/blob/master/molecule/default/prepare.yml):

```yaml
---
- name: prepare
  hosts: all
  become: yes
  gather_facts: no

  roles:
    - role: buluma.bootstrap
```

Also see a [full explanation and example](https://buluma.github.io/how-to-use-these-roles.html) on how to use these roles.

## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/buluma/ansible-role-podman/blob/master/defaults/main.yml):

```yaml
---
# defaults file for podman

# You can modify the `storage.conf` file using this list.
# podman_storage:
#   - option: driver
#     value: overlay
#     section: storage
podman_storage: []

# You can start docker as a specific user other than "root".
# podman_user: my_user
podman_user: ""
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-podman/blob/master/requirements.txt).

## [State of used roles](#state-of-used-roles)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | Version |
|-------------|--------|--------|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Build Status GitHub](https://github.com/buluma/ansible-role-bootstrap/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-bootstrap.svg)](https://github.com/shadowwalker/ansible-role-bootstrap)|

## [Dependencies](#dependencies)

Most roles require some kind of preparation, this is done in `molecule/default/prepare.yml`. This role has a "hard" dependency on the following roles:

- {'role': 'buluma.bootstrap'}

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-podman/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|[Alpine](https://hub.docker.com/repository/docker/buluma/alpine/general)|all|
|[Debian](https://hub.docker.com/repository/docker/buluma/debian/general)|bullseye|
|[EL](https://hub.docker.com/repository/docker/buluma/enterpriselinux/general)|all|
|[Fedora](https://hub.docker.com/repository/docker/buluma/fedora/general)|all|
|[opensuse](https://hub.docker.com/repository/docker/buluma/opensuse/general)|all|
|[Ubuntu](https://hub.docker.com/repository/docker/buluma/ubuntu/general)|jammy|
|[Kali](https://hub.docker.com/repository/docker/buluma/kali/general)|all|

The minimum version of Ansible required is 2.12, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-podman/issues)

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-podman/blob/master/CHANGELOG.md)

## [License](#license)

[Apache-2.0](https://github.com/buluma/ansible-role-podman/blob/master/LICENSE).

## [Author Information](#author-information)

[buluma](https://buluma.github.io/)


### [Special Thanks](#special-thanks)

Template inspired by [Robert de Bock](https://github.com/robertdebock)
