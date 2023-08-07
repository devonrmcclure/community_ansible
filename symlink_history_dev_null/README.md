# Symlink Histories to /dev/null

## Purpose

Ansible playbook to symlink history files to `/dev/null` for a `target_user` on a `target_ip`.

## Example Usage

Note that:

- `-i` flag matches the variable `target_ip`.
- the `target_user` and `target_file` are listed in [`history_dev_null.yml`](history_dev_null.yml)

```bash
ANSIBLE_HOST_KEY_CHECKING=false ansible-playbook -u $ANSIBLE_USER --private-key=$PATH_TO_PRIV_KEY  -i 10.10.10.10, -e 'target_ip=10.10.10.10' history_dev_null.yml
```

