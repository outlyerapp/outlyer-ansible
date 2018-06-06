# Outlyer


This role installs and configures the outlyer agent to send
metrics back to agent.


## Role Variables

* `outlyer_agent_key` - Agent key to use for registration
* `outlyer_agent_debug` - enable debug logging
* `outlyer_agent_solo` - disable central configuration
* `outlyer_agent_docker` - enable the docker checks and discovery
* `outlyer_agent_host_labels` - key value pairings of host labels
* `outlyer_agent_metric_labels` - List of host labels to aply to metrics
* `outlyer_agent_name:` - override agent name 
* `outlyer_manage_service` - Enable/disable the service handler (**true**)


## Usage

In order to automatically add a node to Outlyer, create a file in
your ansible repo named `group_vars/outlyer` using ansible-vault.

Make sure the file has the following content:

```yaml
---
outlyer_agent_key: <insert_outlyer_agent_key_here>
```

```
ansible-playbook -i hosts tasks/main.yml
```

