# Openshift

### Installation

- create a redhat account - https://access.redhat.com/
- download openshift local - https://console.redhat.com/openshift/create/local
- CRC is a tool that manages a local OpenShift 4.x cluster optimized for testing and development purposes
- extract the tar file and plac crc file inside /usr/loacl/bin folder
- download oc cli tool to interact with openshift - https://console.redhat.com/openshift/downloads

```bash
crc setup
crc start
```

### OC commands

```bash
oc login
oc get projects
oc get users
oc get deployments|pods|services
# add admin role to akilan user
oc adm policy add-cluster-role-to-user cluster-admin akilan
```

### Ways to deploy to openshift

- k8s yaml manifest files
- git repo - Openshift clones the repo, build docker image and runs
-
