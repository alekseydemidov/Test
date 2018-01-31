# ostack-deploy
Ansible playbooks for deployment openstack cloud.
It's based on Pike OStack distributive and only for centos 7

This deployment is not fully tested and sometimes it can be failed during changes of OpenStack components.

Implemented compoments:
1. upgrade.yml - upgrade Centos system to latest version, restart system and restoring SELinux context. (separate group in inventory)
2. pre-config.yml - activate required repositories and install common services like NTP, rsyslog etc...
3. controller.yml - install controller service on cotroller node
4. compute.yml - install nova nodes (tags: add-node)
5. network.yml - install neutron nodes (tags: network-node, compute-node)
6. storage.yml - install cinder node (tags: storage-node)
Example: ansible-playbook playbooks/compute.yml

ostack.yml - playbook to install all components (without updating os)
Example: ansible-playbook playbooks/ostack.yml

You can use free any code part or full code if you needed )
Please feel you free to ask me if you have any questions or suggestions
