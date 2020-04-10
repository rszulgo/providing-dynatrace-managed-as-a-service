# providing-dynatrace-managed-as-a-service
Ansible automation to provide Dynatrace Managed as a service

Currently you can find 3 automation examples with Ansible.
- new-environment - automates provisioning of a new environment with a dashboard
- update-environment - automates updating environment by creating a Management Zone
- update-existing-environment - automate updating existing environments by setting Frequent Issue Detection and using EnvironmentManagementToken
- token-rotation - automates `Cluster Token Management` token rotation

## Prerequisites
In order to run above examples it is required to have Ansible installed. Follow the procedure here to get started with Ansible: https://docs.ansible.com/ansible/latest/user_guide/intro_getting_started.html
