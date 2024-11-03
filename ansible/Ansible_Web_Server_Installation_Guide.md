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

2. **Run the ansible-playbook**   
   - Running the Playbook for Nginx, run the following command:
      ```ini
      ansible-playbook -i inventory.ini install_nginx.yml
      
   - Running the Playbook for Apache, run the following command:
      ```ini
      ansible-playbook -i inventory.ini install_apache.yml

      
3. **Checking**   
   Go to the address below:
   ```ini
   http://your_vm_ip_address

If everything worked correctly, you should see the default welcome page of Nginx or Apache.

4. **Control webserver status**
   - Nginx:
       ```ini
      sudo sysystemctl status nginx
   - Apache:
       ```ini
      sudo sysystemctl status apache2

5. **Stop Services**   
   To stop running services:
   - Nginx:
       ```ini
      ansible-playbook -i inventory.ini stop_nginx.yml
   - Apache:
       ```ini
      ansible-playbook -i inventory.ini stop_apache.yml


