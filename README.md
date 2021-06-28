Role Name : kube_worker
=========

Configure Kubernetes Worker node

Requirements
------------
First Configure Kubernetes Master node, using ( kube_master ) role

Role Variables
--------------

packages: 
  - docker 
  - kubelet
  - kubectl
  - kubeadm
  - iproute-tc

services:
  - docker
  - kubelet

Dependencies
------------

This Role is dependent on kube_master which is hosted on Ansibe Galaxy.

Example Playbook
----------------

Playbook for kubernetes_master
    - hosts: tag_Name_of_managed_node
      roles:
         - kubernetes_master

License
-------

BSD

Author Information
------------------

https://www.linkedin.com/in/ajeetrai266