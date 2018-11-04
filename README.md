Ansible - Dockerised Wordpress and Netdata
=========

Ansible playbook to install docker, docker-compose, dockerised-wordpress and netdata.

dockerised-wordpress is installed using docker-compose to install nginx, mariadb and wordpress by using the respective docker images.

Requirements
------------

Ansible 2.2 or higher.  
Tested on target servers using Ubuntu 16.04 LTS only.

Setup
--------------

#### Target hosts inventory
- insert the target host ip address in the host file located at `/hosts`
- change the `[target_ip]` to the host target ip address

#### System, Wordpress, Mysql and Netdata variables
- the variables are stored in `/defaults/main.yml`

#### Nginx config
-  nginx config file is stored at `roles/containerised-wordpress/templates/wordpress.conf`

####  

Executing Playbook
----------------

Run the following command to execute the ansible playbook
`ansible-playbook playbook.yml -i hosts -u [system_user]   `

