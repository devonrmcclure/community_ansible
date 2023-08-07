# GitHub Secrets

## Purpose

Ansible playbook to add secrets/SSH keys to a specific GitHub repo settings.

## Example Usage

Note that `-i` flag matches the variable `target_ip`.

Also note that the `,` after the IP is not a typo.

User must be logged into the gh CLI for this to work.

To change the names of the secrets and amount, the `secrets.yml` file would need to be edited. The relevant lines are the loop on line 44, using the passed in -e variables, and line 52, defining the name of the secrets as they will show on GitHub.

The path to the `gh_secret.js` file will need to be updated inside of `secrets.yml` on line 40 as well.

```bash
ANSIBLE_HOST_KEY_CHECKING=false ansible-playbook -u $ANSIBLE_USER --private-key=$PATH_TO_PRIV_KEY -i 10.10.10.10, -e 'target_ip=10.10.10.10' gh_secrets.yml
```
