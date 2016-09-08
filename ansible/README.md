### Pre amble ###

The order of execution for geonode and qgis-server:

- ansible-playbook  -u <user> -i inventory/hvvagrant.inv playbooks/first-prep.yml --ask-become-pass -vvvv --ask-pass
- ansible-playbook  -i inventory/hvvagrant.inv playbooks/geonode-install.yml -vvvv


The order of execution for geonode and geosafe:

- ansible-playbook  -u <user> -i inventory/hvvagrant.inv playbooks/first-prep.yml --ask-become-pass -vvvv --ask-pass  --ssh-extra-args="-oStrictHostKeyChecking=no"
- ansible-playbook  -i inventory/hvvagrant.inv playbooks/geosafe.yml -vvvv


The __<user>__ above is the "default" user that was created at the
installation of the destination server. The advice is to use a `ubuntu` or `debian` user, as the rest of the playbooks will remove those two users.


### Still to do ###

- the user needs to have his/her pub keys installed/setup for the auto ssh logins the 2nd stage
- The first prep needs the user to be entered on the commandline (-u) etc.
