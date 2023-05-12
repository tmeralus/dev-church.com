# dev-church.com 

This project is to showcase a solution 
for an issue my church was having during migration based
issues. 

---
The Problem
The engineers at my church have 1 Nginx server that 
load balances 3 wordpress servers that connect to databases on each of the vm's. Each of them had phpMyAdmin installed on them as well. Their current method of updating wordpress across the 3 vm's or syncing updates across them was to login to phpMyAdmin across all 3 vm's and make the updates manually. This was the case for updates or changes to wordpress plugins as well. 
The team needed to move away from Centos 6/7 servers to Debian or Ubuntu based servers to avoid licensing changes coming from Redhat. To receive a specific donation they were required to isolate the database and make sure secure connections were being made to the single database for compliance reasons. 

I drew out a simple digram and wrote down a list of problems they needed solutions for. 

![Simple Digram](/img/quick-church-diagram.jpg)

Problems: 
* They need to find an easier solution for managing plugins
* They need to find an easier solution for updating the database 
* They need to crate one database and secure it. 
* They need to move away from redhat/centos to debian or ubuntu to prevent licensing costs. 
* They are looking to limit the amount of downtime required for this migration. 
* They want to limit access to whos making updates and changes to 

and that nginx was connected to the new machines in a way that wouldn't trigger any additional downtime aside from the scheduled downtime. 
