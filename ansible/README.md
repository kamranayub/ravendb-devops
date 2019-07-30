## RavenDB Ansible Playbook

Example RavenDB 4 playbook that:

1. Installs Docker for Linux
2. Configures and ensures a RavenDB container is started

For more information and a walkthrough, see my guide [Automating RavenDB With Ansible](https://kamranicus.com/posts/2019-05-22-ravendb-devops-automation-with-ansible).

## Settings

The example `settings.example.json` shows what a Let's Encrypt configuration might look like, so that the RavenDB server automatically handles renewal of certificates. You may want to remove the `Copy Node A administrator cert` task or disable it in the playbook if you have auto-renewals enabled.