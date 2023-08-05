# ansible-namespace
Technically the folders in this namespace are called collections. However I only use them for roles. The use of a namespace makes it possible to have all roles in 1 Github repository & and to only pull the roles you really need. (and not all).

Available roles:
```bash
UPDATE
LINTING
```

Create a `requirements.yml` file in your Ansible project with the roles you want to pull:
```bash
---
collections:
  - name: community.general
  - name: git+https://github.com/fjfinch/ansible-namespace.git#/<ROLE>
```

Pull the roles on your machine with:
```bash
ansible-galaxy collection install -r requirements.yml
```

To use the roles in your Ansible playbook; insert the following into your `main.yml` file:
```bash
  roles:
    - GITHUB.<ROLE>.ROLE
```
