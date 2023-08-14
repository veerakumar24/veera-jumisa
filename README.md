# Ansible Overview

 - Ansible simplifies the process of configuring, deploying and orchestrating the tasks across multiple servers and devices.
 - Ansible will work based on linux commands. it's based on push mechanism.
 - In ansible no need to install agents and targets systems, to communicates via SSH or WinRM.
 - It orchestrate more advanced tasks like continous deployments and zere downtime. Adhoc commads are used to execute single tasks.
 - Playbooks used to automate everything form system configuration to complex multi-step process, playbooks are written in YAML format.    
 - It consists of a set of tasks used to configure a host to server. Ansible manages the machines in agent-less mannner.

![image](https://github.com/veerakumar24/terraform/assets/130571444/78e2af62-dedc-4449-a3c3-dc0275963b01)

 
# Anisble installation
You can install a released version of Ansible with pip or a package manager. For details on installing Ansible on a variety of platforms: https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html

# Ansible concepts

## Control Node:  
This is the machine where you have Ansible installed and from which you will be running Ansible commands and playbooks. The control node is where you define the tasks and configurations you want to apply to the managed nodes.
 
## Managed Nodes: 
The remote systems that you want to manage using Ansible. These can be servers, virtual machines, network devices, or any other systems that you want to automate tasks on managed nodes are where Ansible will execute the tasks defined in your playbooks.

## Inventory: 
The inventory file defines the remote systems that Ansible can connect to and perform tasks. It also provides information about the hosts, such as their IP addresse and hostnames.   

## Playbooks: 
Playbooks allow you to automate complex workflows, configurations, and application deployments in a structured and repeatable manner.Each playbook consists of one or more plays and each play consists of a set of tasks that are executed in sequence on a specific group of hosts from the inventory.

## Roles: 
Roles tyoically follows the specific directory structure, here roles helps to breakdown the complex automation tasks into smaller. Each can acts as collection of playbooks. 

## Tasks: 
The definition of an action to be applied to the managed host. We can execute a single task once with an ad hoc command using ansible or ansible-console.

## Handelers: 
Handlers are defined at the same level as tasks within a playbook, and they are placed in a dedicated section called handlers. Each handler is defined as a task with a name and module that specifies the action to be taken.

# Project Overview
## Prerequisites
- Ansible installed on the deployment machine.
- JFrog Artifactory account with appropriate permissions.

This project aims to streamline the deployment process of a complex web application composed of a Java Spring Boot backend and a React/Node.js frontend using Ansible. Ansible is an open-source automation tool that simplifies and automates various IT tasks, including application deployment, configuration management, and orchestration.

### The main objectives of this project
- Automate the deployment process of a Java Spring Boot backend application.
- Automate the deployment process of a React Nodejs frontend application.

# Directory Structure

![Screenshot from 2023-08-13 16-35-58](https://github.com/veerakumar24/terraform/assets/130571444/f89678fc-772e-4665-9280-1089db95b9b7)


# Deployment Process
Here the deployment java and react application contains the ansible configuration files ex:
- In installed ansible machine will have the dependencies files are ansible.cfg, main.yml and inventory.ini 
- In ansible.cfg file provides a way to mange the configuration settings like plugins, extensions, control over SSH, and specifing paths.
- The Inventory.ini file in ansible is used to define the inventory of the hosts and groups that ansible can manage such as IP addresses, hostnames, and SSH credentials.

## Main.yaml File
- In Ansible main.yml commonly used to organize tasks ans roles within a playbook.
- The main.yml file serves as an entry point to define the core tasks of the roles.

![Screenshot from 2023-08-13 20-36-57](https://github.com/veerakumar24/terraform/assets/130571444/b2857c70-22ee-4c49-a426-d9e7e643c501)

## Ansible.cfg File
- In ansible.cfg file that allows various option during in deployment stages are setting the defaults optins, enabling the SSH conncection, mainly specifing the roles path.
- The default ansible configuration file which is located under the /etc/ansible/ansible.cfg.
- In ansible configuration file has many parameters like inventory file location, library location, modules and etc,.

![Screenshot from 2023-08-13 20-37-22](https://github.com/veerakumar24/terraform/assets/130571444/32b7635c-af73-46f9-8dc1-ce5b2e2cf170)

## Inventory.ini File
- Inventory file is used to define the hosts and groups of hosts on which you want to perform operations or deployments.
- The inventory file can be stored in two formats: INI and YAML. The default location of the inventory file is/etc/ansible/hosts.
- Mainly defining the hosts and groups and Connection information.

![Screenshot from 2023-08-13 20-37-05](https://github.com/veerakumar24/terraform/assets/130571444/aa6e564c-7ff1-4054-bb47-5717bbcd3c33)

## Backend and Frontend Deployment File
- In tasks folder having the backend path and frontend path wich is stored in the /opt/java-backend/ for Java Springboot and /opt/react-frontend for React Nodejs.
- In deployment process our backend and frontend code were stored in jfrog artifactory in ansible deployment stage we were using the username and token for download the build and un-zip file.

![Screenshot from 2023-08-13 21-21-47](https://github.com/veerakumar24/terraform/assets/130571444/8843554a-4e50-4885-b57f-f2b2a297a93a)

## output 

![Screenshot from 2023-08-12 21-05-07](https://github.com/veerakumar24/terraform/assets/130571444/e6e527da-6ac2-4545-ad46-0d34f033c9d4)



        


