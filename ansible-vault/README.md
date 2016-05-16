## Deploy hashicorp vault + consul HA cluster on Centos6 VMs

#### Steps:

1. git clone https://github.com/andreisid/ansible.git
2. cd ansible-vault
3. Edit hosts file and add your vms for consul cluster and for vault cluster
4. Add values for the following variables in vault.yml playbook:

    vault_consul_advertise_addr: [Address of the Load Balancer in front of vault nodes]
    
    vault_mysql_address: [Address of the mysql server that will server as vault storage backend]
    
4. Add your ssh key to the remote vms with ssh-copy-id
5. Run: ansible-playbook vault.yml -s -K -v -i hosts
