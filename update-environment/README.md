# Updating environment through REST API - creating Management Zones
This script updates existing environment, specified by UUID in `environment-id.yaml` file, by creating a Management Zone of name `mzName`. 

## Prerequisites
1. Update `cluster-input.yaml` with your cluster hostname address. Example:
```
clusterURL: "https://mycluster.dynatrace-managed.com"
```

2. Create or copy from the `../new-environment` directory following files:
- `environment-id.yaml`
- `config-token.yaml` 

3. Example of `environment-id.yaml` file that should contain environment UUID:
```
environmentID: 11333avc-1abc-1212-2323-vvvaaa123123
```
4. Example of `config-token.yaml` file that should contain environment UUID:
```
configToken: abcabcabcabascasd
```
## How to run?
Execute:
```
ansible-playbook hey-mz.yaml --extra-vars "mzName=FrontEndTeam"
```
