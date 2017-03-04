# Ansible Community Share

> Ansible configuration management for standing up a Community Share application

## About

Community Share uses:

- Amazon EC2 for compute
- Amazon S3 for file storage
- Facebook for user authentication
- Ansible for server configuration and code deployment

See the [Community Share repository](https://github.com/chrislaskey/community-share) for more details about the application itself.

Community Share runs on top of:

- Ubuntu 16.04
- Unicorn
- Nginx
- PostgreSQL

## Installation

**Note**: Target architecture is Ubuntu 16.04.

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

To configure the server run the playbook:

```bash
$ bin/install
```

To deploy application code changes also use:

```bash
$ bin/install
```
