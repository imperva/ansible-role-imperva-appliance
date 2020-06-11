## Overview
This project will upgrade an Imperva MX or Gateway.

## Setup
1. Install python 3.6+
2. Configure python virtualenv (if you don't have a PATH_TO_VIRTUALENV and/or you don't have strong feelings on what it should be, you can add a pythonlocal directory in your home dir and path to it - it just keeps you from adding all the python modules to the general machine installation).  (if you have problems with Vagrant finding it later after you logged off, you may need to rerun "source $PATH_TO_VIRTUALENV/bin/activate")
```
python3 -m venv $PATH_TO_VIRTUALENV
source $PATH_TO_VIRTUALENV/bin/activate
```
3. Install python modules
```
pip install -r ./extension/setup/python_requirements.txt
```
4. Install ansible external deps
```
ansible-galaxy collection install -r requirements.yml
```
5. You will need to have an ansible user created on the Imperva appliance that has access to a standard shell.  Your Imperva appliance will need to be unsealed to do this.  You will need to do this once on each Imperva appliance, but then you will be able to keep using that user.  Log in using admin, then type
```
admin
```
to exit the restricted shell.  Then you can 
```
useradd ansible
passwd ansible
```


## Deployment

From the project directory, you can test by running:

ansible-playbook -i inventories/default/hosts -u ansible --extra-vars "ansible_sudo_pass=Webco123 ansible_password=Webco123 ansible_become_method=su ansible_become_pass=Webco123" -vvv site.yml

Edit the inventories/default/hosts file to include the IP or name of your MX for testing.
