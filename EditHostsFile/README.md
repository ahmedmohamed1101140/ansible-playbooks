![](https://miro.medium.com/max/3600/1*xD5TMdgRQ8uRQlvSnZAZ0g.png)
# Edit etc/hosts Playbook

- Requires Ansible 2.9.15


This example is an extension of the simple way in order to update the etc/hosts file on multiple servers

### Initial Site Setup

First we configure the entire stack by listing our hosts in the 'hosts'
inventory file, grouped by their purpose:

		[webservers]
		webserver1
		webserver2
		
		[webservers:vars]
		ansible_user=webservers_username
        ansible_password=webservers_passwor


After which we execute the following command to deploy the site:

		ansible-playbook -i hosts playbook.yml
