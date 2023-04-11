# OCP git configurations for RHACM policies using kustomize and the policy generator plugin

This repo contains three different directory structure for:

- Policy for installing operators
- Policy for configuring operators
- Policy for configuring clusters

The OCP environments are:

- management-hub
- development
- testing
- staging
- production

## Directory structure

### clusters-configurations
Put here all the clusters configurations like:

- Ingress controller
- Proxy
- OAuth
- Api


### operators-configurations
Put here all the operator's configurations like:

- group-sync
- logging

### operators-install
Put here all the operator's you want to install like:

- group-sync-operator
- logging-operator
- metallb-operator
- external-secret-operator


All the common clusters configurations go in the "base" subdirectory

All the ad-hoc configurations go in the "clusters-personalizations" subdirectory


For creating the policy in the RHACM hub cluster, create three RHACM applications using this path:

- /configurations/clusters-configurations/clusters-personalizations/
- /configurations/operators-install/clusters-personalizations/
- /configurations/operators-configurations/clusters-personalizations/


For info about the policy-generator plugin:

https://github.com/stolostron/policy-generator-plugin
















