# ansible-namespace
Technically the folders in this namespace are called collections. However I only use them for roles. The use of a namespace makes it possible to have all roles in 1 GitHub repository & and to pull only the roles you really need. And not all of them.

Available roles:
```bash
UPDATE - update & upgrade system
CLOUD_INIT - disable cloud-init
HOSTNAME - change hostname (set 'device_hostname' variable in playbook)
TIMEZONE - change timezone (set 'device_timezone' variable in playbook)
LINTING - install linting tools
```

## Use
Create a `requirements.yml` file in your Ansible project with the roles you want to pull:
```bash
---
collections:
  - name: git+https://github.com/fjfinch/ansible-namespace.git#/<ROLE>
```

Pull the roles on your machine:
```bash
ansible-galaxy collection install -r requirements.yml
```

To use the roles in your Ansible playbook; insert the following lines into your `main.yml` file:
```bash
  roles:
    - GITHUB.<ROLE>.ROLE
```
