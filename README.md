# Ansible-CitrixVDA
Series of Ansible playbook to be used for:
- Installing Citrix VDA on Windows [(link)]()
- installing Citrix VDA on Linux (Ubuntu) [link](https://github.com/andreaz86/Ansible-CitrixVDA/tree/main/Install/Linux%20VDA)
- Upgrading VDA Agent on Windows persistent VM (or master image too)


# Requirements
To use the playbook you need a Ansible machine with TCP 5985 opened on VDA machines. 
The Playbook use WinRM, be sure you configured the right GPOs in order to use this protocol. 
Make sure you also have installed pywinrm from pip on the ansible machine (pip3 install pywinrm).


