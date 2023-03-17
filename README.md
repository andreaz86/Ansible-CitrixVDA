# Ansible-UpgradeCitrixVDA

This Ansible playbook can be used to upgrade Citrix VDA on persistent Windows Virtual Machine (Golden Image too).
The playbook supports different version of VDA based on the operating systems, for example if the target is Windows Server 2012R2 then it suppose to use VDA 1912 instead of 2203 (based on the OS Major Version variable).


# Requirements
To use the playbook you need a Ansible machine with TCP 5985 opened on VDA machines. 
The Playbook use WinRM, be sure you configured the right GPOs in order to use this protocol. Make sure you also have installed pywinrm from pip on the ansible machine.


# Usage
- Personalize inventory.ini
    - List of VDA Machines under [vda] label.
    - Personalize arguments list if required (VDA 1912 and 2203 has different argument sets).
    - Change CloudConnector/Delivery Controllers FQDN in the cc_names variable.
- Download VDA and place on the same folder where the plabook resides.
    - Take care of file names, needs to be alligned with plabook tasks called "Copy VDA #"
- run ansible-playbook -i inventory.ini playbook.yml