# Automate-VM-Creation-In-Foreman-Using-Ansible-Playbook
Automate VM creation in Foreman using Ansible playbook

Here we will create multiple VMs in foreman using ansible by parsing VM metadata information in CSV format.
VM Metadata information includes vm name, hostgroup, Subnet, IP, CPU, Memory and Network VLAN ID

Example of CSV Files. Header of this file should not be change.

###### Rendered Output: 
| 	HOSTNAME	 | 	HOSTGROUP	 | 	IP	 | SUBNET	 | 	CPU | 	MEMORY_IN_BYTES	 | 	VMNET	 |
| 	:-----:	 | 	:-----:	 | 	:-----:	 | 	:-----:	 | 	:-----:	 | 	:-----:	 | :-----:	 |
| 	ansible_client1.lab.io	| 	LARGE_Centos8	| 	192.168.101.111	 | LAB01 |  4  | 4294967296 | vm-net-55 |
| 	ansible_client1.lab.io	| 	LARGE_Centos8		| 	192.168.101.112	 | LAB01 |  2  | 4294967296   | vm-net-55 |
| 	ansible_client1.lab.io	| 	LARGE_Centos8		| 	192.168.101.113	 | LAB01 |   6 | 8589934592   | vm-net-55 |
| 	ansible_client1.lab.io	| 	LARGE_Centos8		| 	192.168.101.114	 | LAB01 |   4 |  4294967296  | vm-net-55 |
| 	ansible_client1.lab.io	| 	LARGE_Centos8		| 	192.168.101.115	 | LAB01 |   4 |  8589934592  | vm-net-55 |

# 1. To Create Multiple VMs from csv file
   
     $ ansible-playbook foreman_vm_create.yaml -t Create_VM

# 2. To delete Multiple VMs from csv file

    $ ansible-playbook foreman_vm_create.yaml -t Delete_VM
    
# 3. To reboot/reset Multiple VMs from csv file

    $ ansible-playbook foreman_vm_reset.yaml

# 4. To list ansible tags in playbook

    $ ansible-playbook foreman_vm_create.yaml --list-tags

# 5. Demo playbook running

    $ ansible-playbook foreman_vm_create.yaml  -t Create_VM
  
    Enter the path of CSV file of VMs. Exa: /home/dushyantk/vm.csv: 

# ==================================================================================================
