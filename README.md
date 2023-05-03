# Summary
### OS : Ubuntu 22.04
### CRI : Docker latest
### k8s : 1.24.6 deployed by kubespray release-2.20
### CNI : calico
### Kubeflow version : 1.7
### kustomize version : 5.0.0
### storageclass : nfs-provisioner
### etc : gpu-operator
#
# How to use this repository
### 1. run every script as non-root account
### 2. run bootstrap.sh
### 3. (optional) run add_node.sh before adding new worker or master node
### 4. run setup_nfs_provisioner.sh
### 5. run setup_kubeflow.sh
### 6. don't use account_manager.sh yet. It's not tested.
#
# how to uninstall gpu-operator
### 1. helm delete -n gpu-operator $(helm list -n gpu-operator | grep gpu-operator | awk '{print $1}')
#
# how to delete kubeflow
### 1. change directory to manifests
### 2. kustomize build example | kubectl delete -f -
### 3. delete all namespaces related with kubeflow
