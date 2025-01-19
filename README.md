# VM-Creation-In-Foreman-Using-Ansible-Playbook
Automate VM creation in Foreman using Ansible playbook

Here we will create multiple VMs in foreman using ansible by parsing VM metadata information in CSV.
VM Metadata information includes vm name, hostgroup, Subnet, IP, CPU, Memory and Network VLAN ID

Example of CSV Files. Header of this file should not be change.

###### Rendered Output: 
| 	HOSTNAME	 | 	HOSTGROUP	 | 	IP	 | SUBNET	 | 	CPU | 	MEMORY	 | 	VMNET	 |
| 	:-----:	 | 	:-----:	 | 	:-----:	 | 	:-----:	 | 	:-----:	 | 	:-----:	 | :-----:	 |
| 	ansible_client1.lab.io	| 	LARGE_Centos8	| 	192.168.101.111	 | LAB01 |  4  |8192| vm-net-55 |
| 	ansible_client1.lab.io	| 	LARGE_Centos8		| 	192.168.101.112	 | LAB01 |  2  | 8192   | vm-net-55 |
| 	ansible_client1.lab.io	| 	LARGE_Centos8		| 	192.168.101.113	 | LAB01 |   6 | 8192   | vm-net-55 |
| 	ansible_client1.lab.io	| 	LARGE_Centos8		| 	192.168.101.114	 | LAB01 |   4 |  8192  | vm-net-55 |
| 	ansible_client1.lab.io	| 	LARGE_Centos8		| 	192.168.101.115	 | LAB01 |   4 |  8192  | vm-net-55 |
