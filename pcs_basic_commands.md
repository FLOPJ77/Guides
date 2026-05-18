# PCS Commands
This guide covers the clusters management using Pacemaker and Corosync (PCS).

### List:

- pcs status --full
- pcs status resources
- pcs constraint show
- pcs cluster standby [NODE_NAME]
- pcs cluster unstandby [NODE_NAME]
- pcs resource move [RESOURCE_NAME] [TARGET_NODE]
- pcs resource clear [RESOURCE_NAME]
- pcs resource cleanup [RESOURCE_NAME]
- pcs cluster start
- pcs cluster stop
- pcs cluster start --all






<br>


Show the cluster status
```
pcs status --full
```

<br>

View only the state of configured resources (VMs, IPs, etc.)
```
pcs status resources
```

<br>

List all location and colocation rules (why a VM is on a specific node)
```
pcs constraint show
```

<br>

Move all resources off the node
```
pcs cluster standby [NODE_NAME]
```

<br>

Bring the node back into the cluster after maintenance
```
pcs cluster unstandby [NODE_NAME]
```

<br>

Manually move a resource to a specific node
```
pcs resource move [RESOURCE_NAME] [TARGET_NODE]
```

<br>

IMPORTANT: Remove the move constraint:
If you don't run this, the resource can NEVER move back automatically even if the current node fails.
```
pcs resource clear [RESOURCE_NAME]
```

<br>

Reset the failure count and status for a resource
```
pcs resource cleanup [RESOURCE_NAME]
```

<br>

Start the cluster services on the local node
```
pcs cluster start
```

<br>

Stop the cluster services on the local node
```
pcs cluster stop
```

<br>

Start cluster on all nodes in the configuration
```
pcs cluster start --all
```
