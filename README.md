# 2_Tier_With_Ansible

> A simple Ansible project demonstrating automation of a 2-tier architecture  
> (Web Server + Database Server)

---

## 📁 Project Structure

2_Tier_With_Ansible/<br>
├── img/<br>
│ └── architecture.png (visual diagrams & screenshots)<br>
├── 2-tier.yml<br>
├── inventory.ini<br>
└── README.md<br>

---

## 🧠 Overview

This repository contains an **Ansible implementation** for deploying a **2-tier architecture** with:

- 🖥️ **Web Server**
- 🗄️ **Database Server**

Using Ansible’s automation capabilities, infrastructure is defined as code and can be provisioned consistently with minimal manual effort.

---

## 📋 Files Description

### 📌 `inventory.ini`

    Defines host groups for Ansible:

    ```ini
    [web]
    # Add your web server hosts here
    web1 ansible_host=YOUR_WEB_SERVER_IP

    [db]
    # Add your database server hosts here
    db1 ansible_host=YOUR_DB_SERVER_IP


📌 2-tier.yml
The main Ansible playbook that runs roles/tasks against the web and db groups.

How to Run :

Package installation

Configuration of web and DB server services

Running commands via SSH (agent-less)

Replace host/group variables as needed for your setup.

📌 img/
Contains architecture images, diagrams, or screenshots to illustrate:

How the 2-tier setup works

Ansible flow

Deployment design visuals

🚀 How to Run <br>
Make sure Ansible is installed on your control machine

bash
Copy code
ansible --version
Update your inventory.ini with real host IPs.

Apply the playbook:

bash
Copy code
ansible-playbook -i inventory.ini 2-tier.yml
Verify that:

Your web server is reachable via browser/port

Database service is up and running

💡 Tips
✔ Use SSH keys for Ansible connections
✔ Ensure python is installed on remote hosts
✔ Test with ansible-ping before running the playbook

👏 Acknowledgments
Thanks to [@iamtruptimane] for insights & guidance on best practices.

📌 Hashtags

#Ansible #DevOps #Automation #InfrastructureAsCode #IaC 
#WebServer #DatabaseServer #2TierArchitecture #Linux #Cloud