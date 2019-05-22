## RavenDB Ansible Playbook

Example RavenDB 4 playbook that:

1. Installs Docker for Linux
2. Configures and ensures a RavenDB container is started

### Requirements

I am using [Vultr](https://vultr.com) to host my VMs. I had to perform the steps outlined in this guide before I could execute my playbook:

- [Initial secure server configuration for Ubuntu 18.04](https://www.vultr.com/docs/initial-secure-server-configuration-of-ubuntu-18-04)

### Become / sudo

You will need to either run the playbook as a `root` user on the remote host via SSH (not recommended)
or you will need to provide another sudo-permissioned user and provide the password:

    ansible-playbook -i inventory -K ravendb.yml

I also use `become_method=su` because `sudo` (the default) wasn't working in Vultr.