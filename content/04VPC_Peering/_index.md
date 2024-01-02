---
title: "Ch 4- VPC Peering"
chapter: false
menuTitle: "Ch 4: VPC Peering"
weight: 30
---

### Google Cloud VPC Network Peering connects two Virtual Private Cloud (VPC) networks

#### Benefits of VPC Network Peering

VPC Network Peering has the following benefits:
Network Latency: Connectivity that uses only internal addresses provides lower latency than connectivity that uses external addresses.
Network Security: Service owners do not need to have their services exposed to the public Internet and deal with its associated risks.
Network Cost: Google Cloud charges egress bandwidth pricing for networks using external IP addresses to communicate even if the traffic is within the same zone. If however, the networks are peered they can use internal IP addresses to communicate and save on those egress costs. Regular network pricing still applies to all traffic.

https://cloud.google.com/vpc/docs/vpc-peering

#### Overview
This lab is intended to Create/Configure VPC Peering between two Virtual Private Cloud (VPC) networks and secure the workloads by routing the traffic through FortiGate(Hub).


#### Objectives
In this lab you will:

- Create/Configure VPC peering between "Internal/Private/Trust VPC Network of FortiGate's Cluster" and "Web Server VPC Network". 
- Notice on how the routes are exchanged and the traffic flow between the instances which reside in different VPC's, once  VPC Peering is created/configured.
