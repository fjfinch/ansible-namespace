# ansible-namespace
Create a `requirements.yml` file in your Ansible project with the collections you want. Available collections:
```bash
---
collections:
  - name: git+https://github.com/fjfinch/my_namespace.git#/UPDATE
  - name: git+https://github.com/fjfinch/my_namespace.git#/LINTING
```

Pull the collections with on your machine:
```bash
ansible-galaxy collection install -r requirements.yml
```

Use the collections in your projects `main.yml` file:
```bash
  roles:
    - GITHUB.UPDATE.ROLE
    - GITHUB.LINTING.ROLE
```
