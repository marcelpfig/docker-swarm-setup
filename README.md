# The Playbook
This playbook is going to install docker on every remote machine and start a docker swarm cluster.

The master node should be under [master] group in inventory file, while worker nodes should be under [worker] group.

The playbook is able to install docker and setup the cluster on either Ubuntu or RedHat Enterprise Linux (RHEL) as master or worker nodes. To run on Debian/RedHat based systems, adjustments might be required.

One important highlight is this playbook only creates one master node. The worker nodes are going to join this single master. This playbook doesn´t support multiple nodes as master in the same cluster.

## Initial setup
Add your nodes to [master] and [worker] in inventory file.

## Run the playbook
```
ansible-playbook -u user main.yaml
```

## Additional info
Even though this is a simple task, I tried to organize the files using roles and the directory structure recommended at <https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_reuse_roles.html#role-directory-structure>.

The directory full-playbooks contains my initial playbooks (before roles) and they are not being used. They are stored there for studying and consult purposes.

This repository is used for studying and learning purposes. Use at your own risk.