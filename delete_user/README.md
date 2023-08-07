# Delete a User

## Purpose

Ansible playbook to delete a user account from a target machine.

## Example Usage

Note that `-i` flag matches the variable `target_ip`.

```bash
ANSIBLE_HOST_KEY_CHECKING=false ansible-playbook -u $ANSIBLE_USER --private-key=$PATH_TO_PRIV_KEY -i 10.10.10.10, -e 'target_ip=10.10.10.10' -e "target_user=$TARGET_USER" delete_user.yml
```

