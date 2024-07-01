# ansible-namespace
Technically the folders in this namespace are called collections. However I only use them for roles. The use of a namespace makes it possible to have all roles in 1 GitHub repository & and to pull only the roles you really need. And not all of them.

Available roles:
```bash
UPDATE - update & upgrade system
HOSTNAME - change hostname (set the 'device_hostname' variable in your playbook)
TIMEZONE - change timezone (set the 'device_timezone' variable in your playbook)
CLOUD_INIT - disable cloud-init
LINTING - install linting tools
DOCKER - install docker
```

## Use
Create a `requirements.yml` file in your Ansible folder and add this repo URL to it:
```bash
---
collections:
  - name: git+https://github.com/fjfinch/ansible-namespace.git
```

Pull the roles on your machine:
```bash
ansible-galaxy collection install -r requirements.yml
```

To use any role in your Ansible playbook; insert the following lines into your `main.yml` file:
```bash
  roles:
    - GITHUB.<ROLE>.ROLE
```
