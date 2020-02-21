# Provisioning new environment with a dashboard
This script automatically creates new environment with a specified name of the team `teamName`. After the environment is created, appropriate REST API tokens are generated for further orchestration. To give an example, a sample dashboard is created. 

## Prerequisites
Update `cluster-input.yaml` with your cluster hostname address and `ServiceProviderAPI` token. Example:
```
clusterURL: "https://mycluster.dynatrace-managed.com"
serviceProviderAPIToken: "abcabcabcabascasd"
```

## How to run?
Execute:
```
ansible-playbook hey-envs.yml --extra-vars "teamName=NewDynatraceTeam"
```

As a result of that script 2 new files are created:
- config-token.yaml - that contains a `TokenManagement` token for the newly created environment. It can be used for following environment updates
- environment-id.yaml - that contains environment UUID that is required as a path parameter when calling it's REST API.