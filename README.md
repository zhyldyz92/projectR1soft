R1soft R1Soft: Fast, reliable & affordable server backup management.
R1Soft Server Backup Manager (SBM) gives service providers a flexible, server-friendly solution that eliminates the pains of running traditional backups.

http://wiki.r1soft.com/display/ServerBackup/Documentation










Installing R1soft agent on CentOS7 
This ansible playbook will install R1soft agent. Please follow the steps

Step 1 Create master machine where u will install Ansible
Step 2 Whith master machine's public key create 2 machines for R1soft server and R1soft Agent

Step 3 Add hosts ip addresses to the /etc/ansible/hosts

[r1softserver]
youripaddress
[r1softagent]
youripaddress

Step 4 Run the playbook

