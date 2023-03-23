# Ansible-CitrixVDA
Series of Ansible playbook to be used for:
- Installing Citrix VDA on Windows [link](https://github.com/andreaz86/Ansible-CitrixVDA/tree/main/Install%20VDA/Windows%20VDA)|
- installing Citrix VDA on Linux (Ubuntu) [link](https://github.com/andreaz86/Ansible-CitrixVDA/tree/main/Install%20VDA/Linux%20VDA)
- Upgrading VDA Agent on Windows persistent VM (or master image too) [link](https://github.com/andreaz86/Ansible-CitrixVDA/tree/main/Upgrade%20VDA/Windows%20VDA)


# Requirements
To use the playbook you need a Ansible host with port TCP 5985 opened on Windows VDA and port TCP 22 on Linux ones.
For Windows, be sure you configured the right GPOs in order to use this protocol.
For testing purpose you can also use the script from ansible github: [https://github.com/ansible/ansible/blob/devel/examples/scripts/ConfigureRemotingForAnsible.ps1](https://github.com/ansible/ansible/blob/devel/examples/scripts/ConfigureRemotingForAnsible.ps1).

Make sure you also have installed pywinrm from pip on the ansible machine (pip3 install pywinrm).
Install the following modules:
- ansible-galaxy collection install community.windows
- ansible-galaxy collection install chocolatey.chocolatey
- ansible-galaxy collection install community.general 



