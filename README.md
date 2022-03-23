## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![](https://github.com/zacsheahan/ELK-Monitoring-Stack/blob/main/Diagrams/Topology1.png "Topology of ELK-Stack :D")

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the _____ file may be used to install only certain pieces of it, such as Filebeat.

[Ansible Playbooks](https://github.com/zacsheahan/ELK-Monitoring-Stack/tree/main/Ansible)

This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly available, in addition to restricting access to the network.

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the logs and system services.

Filebeat is a lightweight shipper for forwarding and centralizing log data. Installed as an agent on your servers, Filebeat monitors the log files or locations that you specify, collects log events, and forwards them either to Elasticsearch or Logstash for indexing.

Metricbeat takes the metrics and statistics that it collects and ships them to the output that you specify, such as Elasticsearch or Logstash. Metricbeat helps you monitor your servers by collecting metrics from the system and services running on the server, such as: Apache.


The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name     | Function | IP Address | Operating System |
|----------|----------|:------------:|:------------------:|
| Jump Box | Gateway  | 10.0.0.1   | Linux            |
| Web-1    |   Container       |     10.0.0.8       |           Linux       |
| Web-2     |      Container    |        10.0.0.9    |         Linux         |
| ELK     |       Monitoring   |     10.1.0.4       |            Linux      |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the Jump-Box machine can accept connections from the Internet.

Machines within the network can only be accessed by Jump-Box which is accessed by my Host machine via SSH.

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|:----------|:---------------------:|:----------------------:|
| Jump Box | Yes/No              | 10.0.0.1 10.0.0.2    |
|     Web-1     |          No           |                      |
|     Web-2     |            No         |                      |
| ELK |        No      | 168.61.69.77    |
### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
Automation removes the possible errors of Wet-Ware. More automation increases the probability that everything will work each time.

The playbook implements the following tasks:
```
Install Docker
Disable Firewall and Access Controls secureing ports
Install Elastisearch with config and playbook YAML files
Install Kibana with config and playbook YAML files
Install Logstash with config and playbook YAML files
Connect via IPaddress in search engine
```
The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![](https://github.com/zacsheahan/ELK-Monitoring-Stack/blob/main/Diagrams/sebp.elk.761.PNG)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_

We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._
