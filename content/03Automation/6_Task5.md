---
title: "Chapter 3 Quiz"
menuTitle: "Quiz"
chapter: false
weight: 5
---

## Quiz


### Question 1

* Active-Passive HA for FortiGate in GCP requires creation of a separate VPC Network for HA sync traffic  **(True or False)**

  <details>
  <summary> Click Here for <b>Answer</b> </summary>
  <ul>
    <li> <b>True</b> - As we learned in Chapter 2, VMs are allowed only one vNIC per VPC Network, meaning that we have to add a special network for HA sync traffic. </li>
  </ul>
  </details>

### Question 2

* What is one type of data that should not be shared between terraform deployments?  

    a) api keys  
    b) information that may change after deployment  
    c) subnet CIDR addresses  



  <details>
  <summary> Click Here for <b>Answer</b> </summary>
  <ul>
    <li> <b>b</b> - You should not share information that could change after initial deployment.  As an example, if ephemeral IP addresses are used, they may change upon reload of the vm, causing configuration drift.     </li>
  </ul>
  </details>





