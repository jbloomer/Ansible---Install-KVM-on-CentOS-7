# Install KVM on CentOS 7

## Introduction

> This is an Ansible Playbook used to install KVM on remote servers. This was built specifically for CentOS 7 Linux but could easily be adapted for other Linux Distributions

## Installation

1. Clone this repository
2. Update `inventory` to use your IP address (or DNS) or your machine
3. Verify the correct configuration in `ansible.cfg` exist for your setup
4. execute `ansible-playbook main.yml`

## Sample Output

```
PLAY [Install KVM] ****************************************************************************************************************************************************

TASK [Gathering Facts] ************************************************************************************************************************************************
ok: [192.168.1.2]

TASK [checkVirtualization : Check for CPU Virtualization] *************************************************************************************************************
changed: [192.168.1.2]

TASK [installKVM : Installing KVM Packages] ***************************************************************************************************************************
changed: [192.168.1.2] => (item=qemu-kvm)
changed: [192.168.1.2] => (item=libvirt)
changed: [192.168.1.2] => (item=libvirt-python)
changed: [192.168.1.2] => (item=libguestfs-tools)
changed: [192.168.1.2] => (item=virt-install)

TASK [installKVM : Enable and Start libvirtd] *************************************************************************************************************************
changed: [192.168.1.2]

TASK [installKVM : Verify KVM module is loaded] ***********************************************************************************************************************
changed: [192.168.1.2]

PLAY RECAP ************************************************************************************************************************************************************
192.168.1.2                  : ok=1    changed=8    unreachable=0    failed=0
```
