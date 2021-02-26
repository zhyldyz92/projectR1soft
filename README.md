![r1soft-new-2017](https://user-images.githubusercontent.com/78001953/109343354-d8724f00-7832-11eb-8208-bc36b825dac9.jpg)













R1soft R1Soft: Fast, reliable & affordable server backup management.
R1Soft Server Backup Manager (SBM) gives service providers a flexible, server-friendly solution that eliminates the pains of running traditional backups.
R1soft utilizes Continusly Data Protection to work in harmony with our system at the block level. Trasforming the entire backup process into a in short time. R1soft like a traditional backups, it starts by taking a full snapshot of your data. 
After the initial replica is a created, our server backup manager continusly monitors changes to your data and savees only those bits of information that have changes.


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

Installing Prerequsites

- name: Install Prerequisites
    yum:
      name:
      - epel-release
      - vim
      - wget
      - unzip

Because of we were working on Centos7, Centos 7 has some bugs, to fix the bugs follow next steps

HOW TO FIX CENTOS 7 R1SOFT-AGENT
- name: install pip
 yum:
   name: python-pip
   state: present
- name: install zeep (dependency for r1soft modules)
 pip:
   name: zeep
 yum:
   name:
   - serverbackup-enterprise-agent 
   - kernel-devel
   - kernel-headers
   - distro-sync
- name: Restart server
 command: /sbin/shutdown -r +1
 async: 0
 poll: 0
 ignore_errors: true
