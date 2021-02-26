![r1soft-new-2017](https://user-images.githubusercontent.com/78001953/109343354-d8724f00-7832-11eb-8208-bc36b825dac9.jpg)













R1soft R1Soft: Fast, reliable & affordable server backup management.
R1Soft Server Backup Manager (SBM) gives service providers a flexible, server-friendly solution that eliminates the pains of running traditional backups.

http://wiki.r1soft.com/display/ServerBackup/Documentation








This playbook installs R1soft server and R1sost Agent
please follow the steps

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

