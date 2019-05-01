# Sample Content for Using Ansible with Cloud Automation Services 

## Contents 

* web.yml - Simple Playbook for deploying Nginx 
* blueprint.yaml - Blueprint with an Ansible Object

### Overview

Ansible integration in Cloud Automation Services leverages an Ansible Control Machine to act as a central point for executing the playbooks. Both provisioning and de-provisioning playbooks are supported.

From an authentication to ansible hosts, we support a number of  methods:

* Generated Key
* Public Key
* Username and Password


### Your Ansible Control Machine

**Only Ansible 2.6+ is supported currently.** Ensure you have upgraded your Ansible installation using ``` pip --upgrade ansible ```. If you do not have pip installed, you'll need to install it...

Ubuntu: ``` apt install python-pip -y ```
CentOs: ``` yum install python-pip -y ```

Once that is created, you will need to provide a user with sufficient credentials to connect to the Ansible control machine via the integration over SSH.

#### A Note on Ansible Requirements

Ensure you have Python installed on the endpoint machines; Python is required for Ansible to function.