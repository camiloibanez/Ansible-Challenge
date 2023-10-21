# Advanced Ansible Course - Final Project

This Ansible playbook will create a distributed Flask app on AWS. It will create 1 database server that will run mysql and 2 web servers that will run the Flask app. It will create a load balancer to distribute traffic between the two web servers. It sends a confirmation email with SendGrid.

### Prerequisites

- Have run AWS configure
- Installed Python
- Installed Ansible
- Installed sshpass
- Installed boto3
- Installed sendgrid==1.6.22

### Create AWS Infrastructure

- Create Key Pair
- Create security groups
- Create ec2 instances

### Store IP addresses

Store ip addresses of new instances in inventory variables

### Install python dependencies

On all instances

### Install MySQL on db server

- install mysql
- Set root password
- add .my.cnf file
- Change bind-address
- Create database
- Create local and remote user
- Create Table
- Insert data

### Install Flask on web servers

- install Flask
- Copy app source code from github
- Start app

### Create Networking Infrastructure

- Create target group with new web instances
- Create security group for load balancer
- Create load balancer

#### Send confirmation email

### To run

ansible-playbook playbook.yml -i inventory --ask-vault-pass

### To Clean up resources

ansible-playbook cleanup-playbook.yml -i inventory --ask-vault-pass