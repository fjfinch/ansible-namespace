# ansible-namespace
Collection of collections available for `requirements.yml`:
```bash
---
collections:
  - name: git+https://github.com/fjfinch/my_namespace.git#/UPDATE
  - name: git+https://github.com/fjfinch/my_namespace.git#/LINTING
```

Pull with:
```bash
ansible-galaxy collection install -r requirements.yml
```

Set collections in `main.yml`:
```bash
  roles:
    - GITHUB.UPDATE.ROLE
    - GITHUB.LINTING.ROLE
```

## Linting
```bash
ansible-lint
yamllint <DIRECTORY>
ansible-playbook --syntax-check <PLAYBOOK> # syntax check
```

Contents `.ansible-lint` for ansible-lint:
```bash
skip_list:
  - 'yaml[comments]'
  - 'name[missing]'
  - 'name[casing]'
  - 'fqcn[action-core]'
  - 'no-handler'
```
