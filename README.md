# ansible-namespace
Contents of `requirements.yml`:
```bash
---
collections:
  - name: git+https://github.com/fjfinch/my_namespace.git#/UPDATE
  - name: git+https://github.com/fjfinch/my_namespace.git#/LINTING
```
Execute with:
```bash
ansible-galaxy collection install -r requirements.yml
```

Contents of `main.yml`:
```bash
  roles:
    - GITHUB.UPDATE.ROLE
```
