---
title: "Ch 3 - Automation"
chapter: false
menuTitle: "Ch 3: Automation"
weight: 30
---

### ***Use Terraform to Deploy and Configure Infrastructure***

This lab is intended for network administrators looking to integrate firewall management with DevOps practices and workflow. First part of the lab focuses on deploying a pair of FortiGate virtual appliances using Terraform and bootstrapping their configuration to automatically build a multi-zone HA cluster. Second part deploys a simple web application and leverages fortios terraform provider to include FortiGate configuration changes necessary to protect that application.

All deployments and configuration are driven entirely by terraform code and do not require interactive log-in to FortiGate

In this chapter you will:

- Deploy a standard FortiGate HA cluster into Google Cloud using Terraform
- Verify bootstrapping of FortiGate VMs and forming an HA cluster correctly
- Learn how to share data between Terraform deployments
- Deploy a simple web application and reconfigure firewalls to allow traffic to it
- Verify the traffic is passing through the firewall and is protected
- Detect and correct FortiGate configuration drift
- Delete the application and associated firewall configuration
