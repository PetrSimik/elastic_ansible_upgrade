# elastic_ansible_upgrade
upgrade PROD
#check nodes
```
ansible -i hosts_production -m ping elastic_production_nodes -u my_user
```

#upgrade specific single node for production
```
ansible-playbook -i hosts_production upgrade_elastic_nodes.yml -u my_user --limit "ela01node"
```

#upgrade all prod nodes designed to run one by one and wait until health of cluster is green before process to other step
```
ansible-playbook -i hosts_production upgrade_elastic_nodes.yml -u my_user
```
