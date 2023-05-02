# Summary
### OS : Ubuntu 22.04
### CRI : Docker latest 
### k8s version : 1.24.6 deployed by kubespray release-2.20
### CNI : calico
### Kubeflow version : 1.7
### kustomize version : 5.0.0
### storageclass : nfs-provisioner
### etc : gpu-operator, dashboard
#
# How to use this repository
### 1. fix ips of every node
### 2. change hostnames of every node(optional)
### 4. sudo setup_master.sh in master node
### 5. sudo setup_worker.sh as root in worker nodes
### 6. After executing setup_mster.sh, k8s_join_worker.sh will be created at $HOME in master node. copy it to worker nodes
### 7. Run k8s_join_worker.sh in every worker node
### 8. run setup_gpu_operator.sh in master node if worker nodes have gpus
### 9. run setup_nfs_provisioner.sh in master node. write the nfs_ip and nfs_path precisely
### 10. run setup_kubeflow_v1.5.sh(or kubeflow_V1.2) in master node. write master_ip precisely.
### 11. After above all, you can access kubeflow through "HTTPS"!!!
