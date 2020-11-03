# Tower Analytics Data Generator

This repo uses roles from Ansible-CoP's Tower_Configuration collection to configure Tower to have specific resources. 


## Example Usage
Before running the configure_tower.yml, Define all resources in respective files in tower_configs dir. eg: tower_projects.yml, tower_templates.yml.

You can run the playbook directly if you have tower authentication defined in tower_configs/tower_auth.yml

`ansible-playbook playbooks/configure_tower.yml`

You can pass the authentication as variables to the playbook

`ansible-playbook playbooks/configure_tower.yml -e tower_hostname=ansible-tower-web-svc-test-project.example.com -e tower_username=admin -e tower_password=changeme`

You can also pass redhat username and password as variables to the playbook (this is the redhat account to send the Tower data for Automation Analytics)

`ansible-playbook playbooks/configure_tower.yml -e redhat_username=username -e redhat_password=password`

## See Also:
* [Tower Configuration collection](https://github.com/redhat-cop/tower_configuration) to find instructions about installing the collection or authentication.
* [Ansible Using collections](https://docs.ansible.com/ansible/latest/user_guide/collections_using.html) for more details.


