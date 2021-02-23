# Pelorus: Deployment core stack
Role that deploy core stack of Pelorus.

## Download sources

```bash
# Clone Sources
git clone https://github.com/fmenesesg/pelorus-install.git

# Go to pelorus-install
cd pelorus-install
```

## Pre Req



## Demo Application



## Apply Service Mesh configurations


### Ansible Directory Structure

```bash
[francisco@fmeneses pelorus-install]$ tree .


```

* group_vars/all: Global playbook variables

* roles/pelorus-deploy/files: Will contain tls.crt and tls.key files

* roles/pelorus-deploy/meta/main.yml: Metadata file (author,company, etc)

* roles/pelorus-deploy/tasks/main.yml: File that has all the tasks.

* roles/pelorus-deploy/templates/*: Template files used by the task file

* site.yml: Main playbook file


## Variables setup

"All" file contains all the variables used by the playbook

```yaml

```

## Playbook execution

To execute the playbook use the following command

```bash
ansible-playbook site.yml -K
```
