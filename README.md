# Ansible Community Share

> Ansible configuration management for standing up a Community Share application

**Note**: Target architecture is Ubuntu 16.06.

## Installation

#### Initial Setup

Follow the [Ansible Installation Guide](https://docs.ansible.com/ansible/intro_installation.html) to install the latest version of Ansible locally.

Clone the project locally:

```bash
local $ git clone git@github.com:chrislaskey/ansible-community-share.git
local $ cd ansible-community-share
```

Add a `hosts` file:

```bash
local $ copy hosts.example hosts
local $ vim hosts
```

Transfer the bootstrap script to the remote host:

```bash
local $ scp bootstrap your-host.com:~/
local $ ssh your-host.com
```

Run the bootstrap script on the remote host

```bash
remote $ ./bootstrap
```

Confirm ansible can connect and run on the host:

```bash
local $ ./host-ping
```

#### Running Playbooks

Update the `inventory` file with the correct hostnames:

```bash
local $ copy inventory.example inventory
local $ vim inventory
```
