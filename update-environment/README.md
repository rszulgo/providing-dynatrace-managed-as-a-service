# Token rotation
This script automatically rotates the Cluster Token Management token stored in the `cluster-management-token.yaml` file. After 
running the script, token is updated in the file. 

## Prerequisites
1. Update `cluster-input.yaml` with your cluster hostname address. Example:
```
clusterURL: "https://mycluster.dynatrace-managed.com"
```

2. Update `cluster-management-token.yaml` with your Cluster Token Management token value. Example:
```
clusterManagementToken: "abcabcabcabascasd"
```

## How to run?
Execute:
```
ansible-playbook hey-rotator.yaml --extra-vars "tokenName=MyNewTokenName"
```
