---
title: "Task 5 - FortiGate Routing"
menuTitle: "FortiGate Routing"
chapter: false
weight: 5
---

### Configure Routing in FortiGate

Log into the FortiGate using the Admin URL collected earlier from the Deployment manager screen.  You will get a certificate error, just accept and proceed.  Use admin as the username and the Admin Password collected earlier to log in.  You will be required to change the password.  Do so and login.

**Check Dashboard > Network, Routing widget and ensure that you have the 192.168.129.0/25 route.  If not, please complete this task.  If the route is there, move on to Task 3**

* Under **Network** > **Static Routes** click on **Create New** and add a route with Destination 192.168.129.0/25, Gateway IP 192.168.129.1 for port2.
