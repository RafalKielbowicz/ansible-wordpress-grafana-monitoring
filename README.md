# Ansible-Wordpress-Grafana-Monitoring

- **Ansible**
 is open source software that automates software provisioning, configuration management, and application deployment.
- **Grafana**
 the analytics platform for all your metrics. Grafana allows you to query, visualize, alert on and  understand your metrics no matter where they are stored.

## Structure
![graphana](https://user-images.githubusercontent.com/30602779/49342800-e939b780-f65f-11e8-9a00-cd31f96f18e8.PNG)
## Configuration
- In **hosts.ini** add **public** ip of web_nodes, db_nodes and stats_node
```ini
[web_nodes]
#web_nodes_ip ansible_user=ec2-user
[db_nodes]
#db_nodes_ip ansible_user=ec2-user

[metrics_source]
#web_nodes_ip ansible_user=ec2-user
[metrics_store]
#db_nodes_ip ansible_user=ec2-user
[metrics_graph]
#stats_node_ip ansible_user=ec2-user
```

- In **webnode.yml** 
> in vars: **wp_db_ip** and **metric_store_ip** - add **private ip of db_nodes**
>> you can change database and user names by changing var: **project_name**


