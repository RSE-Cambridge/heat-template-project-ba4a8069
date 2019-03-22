# heat-template-project-ba4a8069
Heat template to deploy empty instances on the hphi-jtoa2-project-ba4a8069 project

## Requirements

| Node | Flavor | Comments |
--- | --- | --- 
| controller01 c1.hphi.3xlarge | SG internal between workers and controller |
| 8x 8 core 64 GB 128GB volume ||
| (old) 4x c1.hphi.6xlarge 300 GB volume | |

## Opentack CLI intructions 

* Deploy the platform stack
```bash
# Source your openstack.rc file 
openstack stack create -t heat-template-stack.yml saas-project

# Show status
openstack stack show saas-project
```

* Update stack
```bash
# Set new parameters
openstack stack update --parameter image=Packer-tetris-debian-1528990535 -t heat-template-stack.yml saas-project
openstack stack show saas-project
```

* Delete the stack
```bash 
openstack stack delete sa0s-project
```



