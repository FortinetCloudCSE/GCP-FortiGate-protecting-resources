---
title: "Clone Repo"
menuTitle: "Clone Repo"
chapter: false
weight: 1
---

### Clone github repository 

All code for this lab is hosted in a public git repository. To use it start by creating a local copy of its contents.

1.	Run the following command in your Cloud Shell to clone the git repository contents:

```sh
cd
git clone https://github.com/fortinetsolutions/terraform-modules.git
```
2.	Change current working directory to **GCP/qwiklabs/vpc-peering** inside the cloned repository:

```sh
    cd terraform-modules/GCP/qwiklabs/vpc-peering
```

3. In the **Cloud Shell Editor** part of your Cloud Shell tab choose **File > Open** from the top menu and open the **terraform-modules/GCP/qwiklabs/vpc-peering** folder. Cloud Shell Editor will be useful to navigate, review and edit terraform code during this lab.

For the Terraform, each directory containing **.tf** files is a module. A directory in which you run terraform command is the *root module* and can contain *submodules*. In this lab you will deploy a root module: **vpc-peering** containing submodules.

