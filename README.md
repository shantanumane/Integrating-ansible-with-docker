# Integrating-ansible-with-docker
Automated docker using ansible. Ansible helps to launch new container and host our website at managed node .
Ansible:
Ansible is an open-source software provisioning, configuration management, and application-deployment tool enabling infrastructure as code. It runs on many Unix-like systems and can configure both Unix-like systems as well as Microsoft Windows. Wikipedia





# Docker:
Docker is a set of the platform as service products that use OS-level virtualization to deliver software in packages called containers. Containers are isolated from one another and bundle their own software, libraries, and configuration files; they can communicate with each other through well-defined channels. Wikipedia





# What is httpd?
The Apache HTTP Server, colloquially called Apache, is a Web server application notable for playing a key role in the initial growth of the World Wide Web. Originally based on the NCSA HTTPd server, the development of Apache began in early 1995 after work on the NCSA code stalled. Apache quickly overtook NCSA HTTPd as the dominant HTTP server and has remained the most popular HTTP server in use since April 1996.






# Ansible playbook:
An Ansible playbook is an organized unit of scripts that defines work for a server configuration managed by the automation tool Ansible. Ansible is a configuration management tool that automates the configuration of multiple servers by the use of Ansible playbooks.

# Pre-requisites:

# 1) Installation of Ansible:

 In the RedHat8, Python3 is already installed. So, we have to install ansible on the top of python3. For installing the Ansible use the following command:

 pip3 install ansible
After that, You can check the version of Ansible, for the check whether ansible is installed properly or not!!

No alt text provided for this image




# 2) Configuration of Ansible:

A) In the /etc/myhosts.txt file we have created a group of the Managed Node Ip as a host in Controller Node. By this approach, we can control the automation that Node which is in the group. After the IP, give your username and password of that Managed Node.

No alt text provided for this image
B) Ansible works against multiple systems in your infrastructure at the same time. It does this by selecting portions of the systems listed in Ansible’s inventory file. You can specify a different inventory file using the -i <path> option on the command line. Not only is this inventory configurable, but you can also use multiple inventory files at the same time.

No alt text provided for this image
By using the following command you can the list of hosts you have:

No alt text provided for this image
We need to check, that all managed node is properly connected to the controller node or not. For that use the following command.

No alt text provided for this image
Now the setup of the Ansible is done here. So, we can go to the next step that is creating our own ansible-playbook. Ansible Support YAML language in the playbook. Hence I have created the docker.yml ansible-playbook.
