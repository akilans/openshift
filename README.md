# Openshift

# Openshift Resources
- User
- DeploymentConfig
- Build
- ImageStream
- Route
- Project
- ReplicationController
- BuildConfig
- ImageStreamTag
- Template
- Pod
- ConfigMap
- Secret
- Service
- AutoScaler(HPA)

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
The server is accessible via web console at:
https://console-openshift-console.apps-crc.testing

Log in as administrator:
Username: kubeadmin
Password: hUYMe-XdUto-Eh5D4-RLE9Z

Log in as user:
  Username: developer
  Password: developer

Use the 'oc' command line interface:
$ eval $(crc oc-env)
$ oc login -u developer https://api.crc.testing:6443

### OC commands

```bash
oc whoami # loggedin user name
oc logout
oc login
oc get projects
oc project #current project
oc new-project my_project_1 #create new project
oc project new_project # switches to the project
oc get users
oc get deployments|pods|services
# add admin role to akilan user
oc adm policy add-cluster-role-to-user cluster-admin akilan
oc rsh $POD_NAME #login to shell
oc delete pod $POD_NAME # delete pod
oc get pods
```

### Ways to deploy to openshift

- k8s yaml manifest files
- git repo - Openshift clones the repo, build docker image and runs
-
