# local k8s

There are plenty of ways to run kubernetes locally. However, nothing beats running kubernetes the hard way. This repo uses `vagrant` and `ansible` to provision a local kubernetes cluster.

## Setup

### Prerequisite
- Vagrant
- Ansible

### Setup

1. cd into `k8s` directory
2. run `vagrant up`, then wait for a while, this takes around 20m
3. ssh into the master `vagrant ssh master` to run `kubectl` commands

### Configuration
- VM_IMAGE = "ubuntu/focal64"
- NODES = 2

### Assumptions

- You should have plenty of RAM, recommended is 2GB per machine.
- This works on `VirtualBox`.
- Too bad `--parallel` does not work on both the providers, otherwise, provisioning may be faster.

### Tips

- Since it takes a while to setup, you may want to take a snapshot after initialization so that you can restore from that. (refer to `vagrant snapshot`)

## Reference

-  Kubernetes Setup Using Ansible and Vagrant [[here](https://kubernetes.io/blog/2019/03/15/kubernetes-setup-using-ansible-and-vagrant/)]
- Using Ansible to Create a Kubernetes Cluster on a Virtual Lab [[here](https://graspingtech.com/create-kubernetes-cluster/)]
