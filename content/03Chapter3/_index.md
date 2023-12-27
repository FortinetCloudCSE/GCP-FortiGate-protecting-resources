---
title: "Ch 3 - Automation"
chapter: false
menuTitle: "Ch 3: Automation"
weight: 30
---

### ***Use Terraform to Deploy and Configure Infrastructure***

This lab is intended for network administrators looking to integrate firewall management with DevOps practices and workflow. First part of the lab focuses on deploying a pair of FortiGate virtual appliances using Terraform and bootstrapping their configuration to automatically build a multi-zone HA cluster. Second part deploys a simple web application and leverages fortios terraform provider to include FortiGate configuration changes necessary to protect that application.

All deployments and configuration are driven entirely by terraform code and do not require interactive log-in to FortiGate
