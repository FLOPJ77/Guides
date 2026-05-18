
# KVM basic guide

List all VMs
```
virsh list --all
```

<br>
	
Show basic info (CPU, RAM, State) of a specific VM
```
virsh dominfo <vm-name>
```

<br>

List VMs configured to start automatically on boot
```
virsh list --autostart
```

<br>

Start a VM
```
virsh start <vm-name>
```

<br>

Shutdown(The gentle shutdown) Reboot(The gentle reboot) Destroy(The hardest shutdown) Reset(The hardest reboot)
```
virsh shutdown <vm-name>
virsh reboot <vm-name>
virsh destroy <vm-name>
virsh reset <vm-name>
```

<br>

Suspend / Resume (Pause the VM in RAM)
```
virsh suspend <vm-name>
virsh resume <vm-name>
```

<br>

List all virtual disks attached to the VM
```
virsh domblklist <vm-name>
```

<br>

List all network interfaces (and MAC addresses)
```
virsh domiflist <vm-name>
```

<br>

View CPU and Core allocation
```
virsh vcpuinfo <vm-name>
```

<br>

Edit the VM configuration (XML) this opens your default editor (usually vi).
```
virsh edit <vm-name>
```

<br>

Dump the VM configuration to a file (Backup)
```
virsh dumpxml <vm-name> > vm_backup.xml
```

<br>

Console VM, --force can help when VM is stuck
```
virsh console <vm-name>
virsh console <vm-name> --force
```

<br>

Increase RAM the VM can use
```bash
virsh setmaxmem <vm-name> 4G --config
virsh setmem <vm-name> 4G --config
```

<br>

Is possible to increase RAM while VM is running using --live but remember to add --config too if you want it keeps changes after restart. Note that the RAM cant exceed the "Max Memory" defined in the XML:
```
virsh setmem <vm-name> 4G --live --config
```

<br>

Check current CPU usage/affinity
```
virsh vcpuinfo <vm-name>	
```

<br>

Change CPU count immediately (Live)
```
virsh setvcpus <vm-name> 4 --live
```

<br>

Set CPU count for next boot
```
virsh setvcpus <vm-name> 4 --config
```

<br>

Set the maximum limit to 8 CPUs
```
virsh setvcpus <vm-name> 8 --maximum --config
```








