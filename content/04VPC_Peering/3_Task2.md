---
title: "Deploy Network and Server"
menuTitle: "Deploy Server"
chapter: false
weight: 2
---

### Using **vpc-peering** module you will deploy a nginx web server in a VPC

### Customizing deployment through variables
Before deploying the **vpc-peering** module you have an opportunity to customize it. The module expects an input variable indicating the region to use.

Open **vpc-peering/terraform.tfvars** file:

You have to indicate the GCP project to deploy to by setting `project` variable in **vpc-peering/terraform.tfvars** to the name of your qwiklabs project indicated as **GCP Project ID** in the **Lab Details** panel. 

### Web Server deployment
Web Server deployment consists of 3 steps. Execute them now as described below:

1.	In **vpc-peering** directory initialize terraform using command

```sh
    terraform init
```

This will make terraform parse your **.tf** files for submodules and providers, and download necessary additional files. Re-run `terraform init` every time you add or remove providers and submodules

2.	Build a terraform plan and save it to **tf.plan** file by issuing command  

```sh
    terraform plan
```

Terraform plan file describes every resource to be created and dependencies between them. Planning phase also connects to every provider and checks the state file to verify if any of the resources described in the code already exist or have changed. You should always verify the output of `terraform plan` to understand what resources will be created, changed or destroyed.

3.	Create the resources according to the plan by issuing command  

```sh
    terraform apply
```

This command will attempt to create, delete or change the resources according to the plan. If run without providing a plan file `terraform apply` will create a new plan and immediately execute it after confirmation from operator. `terraform apply` should be executed every time after the code or variables change.  

Enter `yes` at the **Enter a value:** prompt.

After `terraform apply` command completes you will see several output values which will be necessary in later steps. Terraform outputs can be used to provide additional information to the operator.

### Reviewing the deployment
Once everything is deployed you can see the sample page of the Web Server when you enter the External IP of the Compute Engine Instance.
{{% notice note %}} It is recommended not to have an External IP for this Web Server. {{% /notice %}}
