---
title: "Task 1 - Compute Engine API "
menuTitle: "Task 1 - Enable APIs"
weight: 5
---

## Task 2 Enable Compute Engine APIs

Using the link from the email, login to the GCP console using your Fortinet AD Credentials.

- As this project is newly built, you will need to enable several different APIs.  There are two methods to accomplish this:

  - **Using the Console** we will enable the **Compute Engine API**: 
      - From the original GCP Console, click the "hamburger" menu on the top left of the screen, select **Compute Engine > VM instances**
      ![CE_hamburger](CE_hamburger.png)
      - This will take you to a screen where you can enable the Compute Engine API.  Select **Enable**
      ![CE_api_enable](CE_api_enable.png)
      - Once enabled, you will be re-directed to the VM instances Screen.
  
  - **Using Cloud Shell** we will enable **Service Usage API**, **Identity and Access Management (IAM) API** and **Cloud Resource Manager API**:
      - On the top right hand side of the screen, click on the Activate Cloud Shell icon 
      ![en-shell](en-shell.png)

      - This will open a cloud shell at the bottom of the screen.  You will need to be sure that you are in the correct project using the below command (authorize as necessary):

      ```
      gcloud config set project <project-id>

      ```
      - Now we can enable the appropriate APIs  
      ```
          gcloud services enable serviceusage.googleapis.com
          gcloud services enable iam.googleapis.com
          gcloud services enable cloudresourcemanager.googleapis.com
      ``` 
