# ansible-namespace
Technically the folders in this namespace are called collections. However I only use them for roles. The use of a namespace makes it possible to have all roles in 1 Github repository & and to only pull the roles you really need. (and not all).

Create a `requirements.yml` file in your Ansible project with the following (pull the roles you want):
```bash
---
collections:
  - name: git+https://github.com/fjfinch/my_namespace.git#/UPDATE
  - name: git+https://github.com/fjfinch/my_namespace.git#/LINTING
```

Pull the roles on your machine with:
```bash
ansible-galaxy collection install -r requirements.yml
```

To use the roles in your Ansible playbook; insert the following into your `main.yml` file:
```bash
  roles:
    - GITHUB.UPDATE.ROLE
    - GITHUB.LINTING.ROLE
```
