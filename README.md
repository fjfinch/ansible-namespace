# ansible-namespace
Collection of collections available for `requirements.yml`:
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

Set collections in `main.yml`:
```bash
  roles:
    - GITHUB.UPDATE.ROLE
    - GITHUB.LINTING.ROLE
```
