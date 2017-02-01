# Ansible Community Share

> Ansible configuration management for standing up a Community Share application

**Note**: Target architecture is Ubuntu 16.06.

## Installation

#### Initial Setup

Follow the [Ansible Installation Guide](https://docs.ansible.com/ansible/intro_installation.html) to install the latest version of Ansible locally.

Clone the project locally:

```bash
$ git clone git@github.com:chrislaskey/ansible-community-share.git
$ cd ansible-community-share
```

Add a host inventory file:

```bash
$ copy hosts/production.example hosts
$ vim production
```

Transfer the bootstrap script to the remote host:

```bash
$ scp bin/bootstrap your-host.com:~/
$ ssh your-host.com
```

Run the bootstrap script on the **remote** host

```bash
$ ./bootstrap
```

Confirm ansible can connect and run on the host:

```bash
$ bin/ping
```

#### Running Playbooks

Update the host inventory file with the correct hostnames:

```bash
$ copy hosts/production.example hosts/production
$ vim hosts/production
```
