# project-1
Deployment to tomcat
  1. Install tomcat
  2. Create the below user with manager-script permission in tomcat-users.xml file
     <user username="deployer" password="deployer" roles="manager-script"/>
  3. Create credentials with above username and password in Jenkins and mention the url of webserver(tomcat)
  Plugin : Deply to container


# project-2
Deployment to webserver using Ansible configuration
  1. Install Ansible with ansadmin user (Any user)
  2. Do the below 3-4 steps in both Ansible server and Ansible Node
  3. Open visudo and give root privilages to the above user
  4. Open vi /etc/ssh/sshd_config and enable 'PasswordAuthentication yes' and do 'service ssh restart'
  5. Create ssh key with 'ssh-keygen' and do 'ssh-copy-id nodeipaddress'
  6. Create dir 'group_vars' in /etc/ansible/ and give 'ansible_ssh_pass: ansible_become_pass: ansadmin: '
  Plugin : Publish Over SSH
  6. Configure Publish overssh in Managejenkins by giving ansibleserver ipaddress, username and password.
