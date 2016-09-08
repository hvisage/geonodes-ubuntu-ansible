### Pre amble ###

The order of execution for geonode and qgis-server:

- ```ansible-playbook   -i inventory/example.inv -e "ansible_user=ubuntu" --ssh-common-args=" -oStrictHostKeyChecking=no" --ask-pass  --ask-become  playbooks/first-prep.yml```


The __```ubuntu```__ user above is the "default" user that was created at the
installation of the destination server. The advice is to use a `ubuntu` or `debian` user, as the next  playbook will remove those two users.

- ```ansible-playbook  -i inventory/hvvagrant.inv playbooks/geonode-install.yml -vvvv```


The order of execution for geonode and geosafe:

- ansible-playbook  -u <user> -i inventory/hvvagrant.inv playbooks/first-prep.yml --ask-become-pass -vvvv --ask-pass  --ssh-extra-args="-oStrictHostKeyChecking=no"
- ansible-playbook  -i inventory/hvvagrant.inv playbooks/geosafe.yml -vvvv



### Still to do ###

- the user needs to have his/her pub keys installed/setup for the auto ssh logins the 2nd stage
- The first prep needs the user to be entered on the commandline (-u) etc.
