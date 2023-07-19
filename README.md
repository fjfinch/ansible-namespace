# ansible-namespace
Create `requirements.yml` with:
```bash
collections:
  - name: git+https://github.com/fjfinch/my_namespace.git#/UPDATE
```

In `main.yml`:
```bash
  roles:
    - GITHUB.UPDATE.ROLE
```
