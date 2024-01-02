---
title: "Change Directory and Open Editor"
menuTitle: "Change Repo Directory"
chapter: false
weight: 1
---

All code for this lab can be found in the same repo you cloned in the Automation lab above

1.	Change current working directory to **/GCP-supporting-resources/vpc-peering** inside the cloned repository:

```sh
    cd ~/GCP-supporting-resources/vpc-peering
```

2. In the **Cloud Shell Editor** part of your Cloud Shell tab choose **File > Open** from the top menu and open the **GCP-supporting-resources/vpc-peering** folder. Cloud Shell Editor will be useful to navigate, review and edit terraform code during this lab.

For the Terraform, each directory containing **.tf** files is a module. A directory in which you run terraform command is the *root module* and can contain *submodules*. In this lab you will deploy a root module: **vpc-peering** containing submodules.

