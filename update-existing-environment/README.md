# Updating environment through REST API - Frequent Issues Detection settings
This script updates existing environments as specified by UUID in `environments.yml` file, by setting FID values

## Prerequisites
1. Update `cluster-input.yaml` with your cluster hostname address. Example:
```
clusterURL: "https://mycluster.dynatrace-managed.com"
```

2. Create `environments.yaml` file that contains Ansible list of environment UUIDs:

Example:
```
environments: ["11333avc-1abc-1212-2323-vvvaaa123123","22444avc-1abc-1212-2323-vvvaaa123123"]
```

3. Create EnvironmentManagementToken in DebugUI (since 192) or in CMC (since 194)

## How to run?
Execute:
```
ansible-playbook hey-envs.yaml --extra-vars "token=tokenValue"
```