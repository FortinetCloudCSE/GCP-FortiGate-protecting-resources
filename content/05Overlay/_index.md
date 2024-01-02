---
title: "Ch 5- Overlay and SD-WAN"
chapter: false
menuTitle: "Ch 5: Overlay and SD-WAN"
weight: 30
---

In previous labs, we built a Cloud on-ramp using two FortiGates deployed as a High Availability pair sandwiched between two Load Balancers.  We also built a remote site using a single FortiGate and Ubuntu server.  The next step is to securely connect the remote location with the cloud on-ramp.  In the following excercises, we will configure the IPsec overlay.  BGP will be used to share routes between locations.  Once the overlay is in place, we will configure SD-WAN to monitor SLA

* Network Diagram

    ![full-network-diagram](full-network-diagram.png)

