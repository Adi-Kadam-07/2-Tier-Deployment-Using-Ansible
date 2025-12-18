# 2-Tier Application Deployment Using Ansible :

A hands-on **DevOps automation project** that demonstrates how to deploy a  
**2-Tier application architecture** using **Ansible**.

This project automates the configuration of:
-  **Application Server** (Nginx + PHP)
-  **Database Server** (MariaDB)

## Project Structure :
```.
├── Main_Script.yml      # Main Ansible playbook
├── inventory.ini        # Target server inventory
└── README.md            # Project documentation
|__ img                  # Images
```
---

##  Architecture Overview :

```text
Client
  |
  v
Application Server
(Nginx + PHP)
  |
  v
Database Server
(MariaDB)
```

## Technologies Used :

| Tool                    | Purpose                  |
| ----------------------- | ------------------------ |
| **Ansible**             | Configuration Management |
| **Nginx**               | Web Server               |
| **PHP / PHP-FPM**       | Backend Processing       |
| **MariaDB**             | Database                 |
| **Amazon Linux** | Operating System         |

##  Ansible Playbook Details :

###  Application Server Tasks :
- Install **Nginx**, **PHP**, and **PHP-FPM**
- Start and enable required services
- Deploy a sample PHP application (`phpinfo()`)

### Database Server Tasks :
- Install **MariaDB**
- Start and enable MariaDB service
- Create a database named **Project**

## How to Execute the Project :
### Step 1: Syntax Validation -
```ansible-playbook Main_Script.yml -i inventory.ini --syntax-check```

### Step 2: Run the Playbook -
```ansible-playbook Main_Script.yml -i inventory.ini```

##  Verification Steps :

- Open the **Application Server IP** in a web browser
- The **PHP info page** should load successfully
- **MariaDB service** should be running on the Database Server
- Database **Project** should be created successfully

## Screenshots :
![](/img/Ansi_servers.png)

![](/img/php_in_app.png)

![](/img/database_create.png)
