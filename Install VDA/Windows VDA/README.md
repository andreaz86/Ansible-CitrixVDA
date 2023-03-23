# Install Citrix VDA on Windows using Ansible
this playbook can be used to install Citrix VDA agent on Windows VM.


## Configure
just replace the default value on varibles in the inventory.ini:
- **ansible_user:** username used for connection.
- **ansible_password:** password for the user (not recommended).
- **ansible_port:** WinRm ports used (5986 recommended), 5985 for without certificate encryption.
- **vda_url:** url used to download the VDA
- **optimizer_url:** url used to download citrix optimizer
- **rendezvousv2:** if need to push rendezvous V2 reg key (true/false)
- **rendezvousv2_proxy:** specify the proxy to be used for rendezvous C2(leave false if not)
- **vda_arguments:** specify arguments passed to the VDA installation

## Requirements
Read the [main project page](https://github.com/andreaz86/Ansible-CitrixVDA/) for ansible requirements.
