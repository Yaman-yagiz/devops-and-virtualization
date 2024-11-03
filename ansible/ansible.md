# Ansible Nginx and Apache Project

This project provides automated installation and management of Nginx and Apache web servers on an Ubuntu virtual machine using Ansible. The project includes various playbooks to facilitate the installation and stopping of web server services.

## Requirements

- Ansible
- An Ubuntu virtual machine
- SSH access

## Project Structure

- **inventory.ini**: Ansible inventory file containing virtual machine details.
- **install_nginx.yml**: Ansible playbook to perform the Nginx installation.
- **install_apache.yml**: Ansible playbook to perform the Apache installation.
- **stop_nginx.yml**: Ansible playbook to stop the Nginx service.
- **stop_apache.yml**: Ansible playbook to stop the Apache service.
- **README.md**: Document providing information about the project.

## Installation Steps

1. **Update the Inventory File**  
   Open the `inventory.ini` file and update it with your virtual machine's IP address and username in the following format:
   ```ini
   [webservers]
   your_vm_ip_address ansible_ssh_user=your_username

- Nginx Installation To install Nginx, run the following command:
  - ansible-playbook -i inventory.ini install_nginx.yml
- Apache Installation To install Apache, run the following command:
  - ansible-playbook -i inventory.ini install_apache.yml
- Stopping Nginx Service To stop the Nginx service, run the following command:
  - ansible-playbook -i inventory.ini stop_nginx.yml
- Stopping Apache Service To stop the Apache service, run the following command:
  - ansible-playbook -i inventory.ini stop_apache.yml

