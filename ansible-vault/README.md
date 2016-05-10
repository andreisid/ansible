## Deploy hashicorp vault + consul HA cluster on Centos6 VMs

#### Steps:

1. git clone https://github.com/andreisid/ansible.git
2. cd ansible-vault
3. Edit hosts file and add your vms
4. Add your ssh key to the remote vms with ssh-copy-id
5. Run: ansible-playbook vault.yml -s -K -v -i hosts
