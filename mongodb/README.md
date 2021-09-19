# local MongoDB ReplicaSet

## Setup

### Prerequisite
- Vagrant
- Ansible
- PipENV

### Initialize
1. run `pipenv --three`
2. install ansible `pip install ansible`
3. install mongodb plugin `ansible-galaxy collection install community.mongodb`

### Setup

1. run `vagrant up`, then wait for a while, this takes around 20m
2. run `ansible-playbook -i hosts deploy.yaml`

### Configuration
- VM_IMAGE = "centos/8"
- NODES = 2

### Assumptions

- You should have plenty of RAM, recommended is 2GB per machine.
- This works on `VirtualBox`.
- Too bad `--parallel` does not work on both the providers, otherwise, provisioning may be faster.

### Tips

- Since it takes a while to setup, you may want to take a snapshot after initialization so that you can restore from that. (refer to `vagrant snapshot`)
