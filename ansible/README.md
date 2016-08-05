### Pre amble ###

The order of "execution:

- ansible-playbook  -u <user> -i inventory/hvvagrant.inv playbooks/first-prep.yml --ask-become-pass -vvvv --ask-pass
- ansible-playbook  -i inventory/hvvagrant.inv playbooks/geonode-install.yml -vvvv

### Still to do ###

- the user needs to have his/her pub keys installed/setup for the auto ssh logins the 2nd stage
- The first prep needs the user to be entered on the commandline (-u) etc.
- 
