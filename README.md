# N.ChavezRepo22
N.Chavez-CS22
## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![TODO: Update the path with the name of your diagram](Images/diagram_filename.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the _____ file may be used to install only certain pieces of it, such as Filebeat.

  - _TODO: Enter the playbook file._

This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly _____, in addition to restricting _____ to the network.
- _TODO: What aspect of security do load balancers protect? What is the advantage of a jump box?_

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the _____ and system _____.
- _TODO: What does Filebeat watch for?_
- _TODO: What does Metricbeat record?_

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name     | Function | IP Address | Operating System |
|----------|----------|------------|------------------|
| Jump Box | Gateway  | 10.0.0.1   | Linux            |
| Web-2    |          | 10.0.0.6   | Ubuntu 20.04     |
| Web-1    |          | 10.0.0.5   | Ubuntu 20.04     |
|Project1VM| ELK-STACK| 10.1.0.4   | Ubuntu 20.04     |

Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the JUMPBOX-PROVISIONER_ machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
-my personal home IP.

Machines within the network can only be accessed by JumpBox-Provisoner.
- _TODO: Which machine did you allow to access your ELK VM? What was its IP address?Persoanal IP

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes                 | 10.0.0.1             |
| Web-1    | no                  | 10.1.0.4             |
| Web-2    | no                  | 10.1.0.4             |

Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
-It can accepts a ongoing known config. Elk on the other hand can be modified instantly.

The playbook implements the following tasks:
-install docker .io , python3-pip and apt
- Enable systemd docker .io
- Run my docker containers



The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![elkp1](https://user-images.githubusercontent.com/101543246/158514800-09f07208-cbc9-46d6-a854-9e03612de54e.png)


### Target Machines & Beats
This ELK server is configured to monitor the following machines:
-Web-1-10.0.0.5
-Web-2-10.0.0.6

We have installed the following Beats on these machines:
Filebeat
Metricbeat

These Beats allow us to collect the following information from each machine:
- Filebeat passes logs to my web-1 and web-2 servers
- Metricbeat reports logs and stats to my Web-1 and Web-2 servers

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the Filebeat-playbook.yml file to etc/ansible/files.
- Update the /etc/ansible/hosts file to include the Project1vm
- Run the playbook, and navigate to /etc/ansible/file to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._
