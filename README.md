[![Actions Status - Master](https://github.com/juju4/ansible-adduser/workflows/AnsibleCI/badge.svg)](https://github.com/juju4/ansible-adduser/actions?query=branch%3Amaster)
[![Actions Status - Devel](https://github.com/juju4/ansible-adduser/workflows/AnsibleCI/badge.svg?branch=devel)](https://github.com/juju4/ansible-adduser/actions?query=branch%3Adevel)

# kvrocks ansible role

Setup kvrocks server
* https://github.com/KvrocksLabs/kvrocks/

## Requirements & Dependencies

### Ansible
It was tested on the following versions:
 * 2.11

### Operating systems

Tested on Ubuntu 14.04, 16.04, 18.04, Centos 6, 7 and OpenBSD 5.8.

## Example Playbook

Just include this role in your list.
For example

```
- host: myhost
  roles:
    - juju4.kvrocks
```

## Variables

TBD

## Continuous integration

```
$ pip install molecule docker
$ molecule test
$ MOLECULE_DISTRO=ubuntu:20.04 molecule test --destroy=never
```


## Troubleshooting & Known issues

* Kvrocks releases are only for x86_64 architecture. No arm at Dec 2021.

* Be aware that rpm package installs file in /www/kvrocks and does not include any systemd unit file.

* Molecule docker uses [Docker official build of CentOS](https://hub.docker.com/_/centos) but with Centos8 End-Of-Life, repositories are not valid anymore. Moved to alternate distributions.
[Failed to download metadata for repo ‘AppStream’ CentOS, Feb 2022](https://techglimpse.com/failed-metadata-repo-appstream-centos-8/)
[CentOS 8 is dead: choosing a replacement Docker image, Jan 2022](https://pythonspeed.com/articles/centos-8-is-dead/)

## License

BSD 2-clause
