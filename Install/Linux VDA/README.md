# Install Citrix VDA on Ubuntu using Ansible
this playbook can be used to install Citrix VDA agent on ubuntu VM.


## Configure
just replace the default value on varibles in the inventory.ini:
- **ansible_user:** username used for connection.
- **ansible_password:** password for the user (not recommended).
- **ansible_ssh_private_key_file:** ssh key file for user authentication (recommended).
- **ansible_become_user:** privilege esclation account username (sudoers)
- **ansible_become_password:** privilege esclation account password 
- **linuxvda_url:** url for downloading the linux VDA (in the playbook there is also a commented task if you prefer to push from ansible)
- **dc_internal_ip:** Domain Controller IP
- **dc_fqdn:** Domain Controller FQDN (not needed if domain_joined="false")
-**netbios_name:** NETBIOS name of the domain (not needed if domain_joined="false")
- **domain_name:** domain name (not needed if domain_joined="false")
- **ad_join_username:** username to be used for AD Join (not needed if domain_joined="false")
- **ad_join_password:** password to be used for AD Join (not needed if domain_joined="false")
- **rendezvousv2:** if need to push rendezvous V2 reg key (true/false)
- **rendezvousv2_proxy:** specify the proxy to be used for rendezvous C2(leave false if not)
- **domain_joined:** specify if you want VM to be used for Non Domain Join

## Requirements
Read the [main project page](https://github.com/andreaz86/Ansible-CitrixVDA/) for ansible requirements