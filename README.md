## Testing/Linting Ansible playbooks locally

The testing spectrum from low to high complexity:

1. yamlint
2. `ansible-playbook --syntax-check`
3. ansible-lint
4. molecule test (integration)
5. ansible-playbook --check (against production)
6. Parallel infrastructure

## Local roles

Keep your roles local to the proyect by indicating so in `ansible.cfg`

```ini
[defaults]
nocows = True
roles_path = ./roles
```

```bash
ansible-galaxy  install -r requirements.yml
```


requirements.yml
```yaml
---
  roles:
  - name: elliotweiser.osx-command-line-tools
    version: 2.3.0
  - name: geerlingguy.homebrew
    version: 3.1.0
```

## References
- https://www.ansible.com/theres-a-role-for-that