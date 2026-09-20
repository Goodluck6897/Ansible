in centos in all nodes
#yum install epel-release -y;yum install ansible -y
useradd ansibleusr;passwd ansibleusr

on all noes
[root@v2 ~]# cat>>/etc/sudoers
ansibleusr ALL=(ALL) NOPASSWD: ALL

useradd ansibleusr
passwd ansibleusr
visudo
ansibleusr ALL=(ALL) NOPASSWD: ALL
su - ansibleusr
vim /etc/ssh/sshd_config
Set "PasswordAuthentication yes"
service sshd restart

https://github.com/Goodluck6897/ansible-aviz/blob/main/Ansible.md
