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
#
# how to uninstall gpu-operator
### 1. helm delete -n gpu-operator $(helm list -n gpu-operator | grep gpu-operator | awk '{print $1}')
#
# how to delete kubeflow
### 1. kubectl delete profile --all
### 2. change directory to manifests
### 3. kustomize build example | kubectl delete -f -
