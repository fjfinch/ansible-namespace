# ansible-namespace
Technically the folders in this namespace are called collections. However I only use them for roles. 

Available roles:
```bash
REQUIREMENTS - pull latest roles
UPDATE - update & upgrade system
DOCKER - install official docker
LINTING - install linting tools
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
