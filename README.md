
# Ansible role to install Nginx (Debian, CentOS)
This is a Ansible role to install Nginx
## Prerequisites
Installed and configured Ansible 
Add *hosts* file into same directory and usew role with -i hosts
```
Example: 
 > cat hosts
  [web-debian]
  ip1
  ip2

  [web-centos]
  ip3

  [web:children]
  web-debian
  web-centos
```
## Usage
* Install Nginx to inventory hosts
```
 > git clone https://github.com/r00tvvm/nginx-role.git && cd nginx-role
 > ansible-playbook -i hosts site.yml
```

* Remove Nginx from inventory hosts
```
 > ansible-playbook -i hosts site.yml -t remove
```
