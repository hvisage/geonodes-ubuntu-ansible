### Pre amble ###

The order of execution for geonode and qgis-server:

- ansible-playbook  -u <user> -i inventory/hvvagrant.inv playbooks/first-prep.yml --ask-become-pass -vvvv --ask-pass
- ansible-playbook  -i inventory/hvvagrant.inv playbooks/geonode-install.yml -vvvv


The order of execution for geonode and geosafe:

- ansible-playbook  -u <user> -i inventory/hvvagrant.inv playbooks/first-prep.yml --ask-become-pass -vvvv --ask-pass  --ssh-extra-args="-oStrictHostKeyChecking=no"
- ansible-playbook  -i inventory/hvvagrant.inv playbooks/geosafe.yml -vvvv


### Still to do ###

- the user needs to have his/her pub keys installed/setup for the auto ssh logins the 2nd stage
- The first prep needs the user to be entered on the commandline (-u) etc.
