---
title: Out Of Box Actions
description: The Out of the Box Actions comprise OOB deployment, tagging, retrieving and post-provisioning operations. All these actions are based on Flow Designer and implemented as Integration Hub Sub-flows.
locale: en-US
release: australia
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Out Of Box Catalogs using Cloud Services Catalog, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Out Of Box Actions

The Out of the Box Actions comprise OOB deployment, tagging, retrieving and post-provisioning operations. All these actions are based on Flow Designer and implemented as Integration Hub Sub-flows.

<table id="simpletable_a4m_l5y_nxb"><thead><tr><th>

Actions

</th><th>

Flow Designer Sub-flow Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Deploy ACC-\* in post provisioning

</td><td>

CSC Content- Post Provisioning- Deploy ACC in Stack VMs

</td><td>

ACC \(agent client collector\) is deployed through a Flow Designer action. This is called as post-provision step for the Linux basic VM deployment catalog item. Pre-requisites:

 1.  ACC Listener must be configured in any MID Server. This will generate a mid web server endpoint and a MID Server API Key.
2.  In the post provisioning operation parameters of the Basic Linux VM catalog, these two parameters – web server end point \(typically in format wss://&lt;IP\_Address&gt;:3389/ws/events\) and MID Server API Keys, need to be set. Out of the box, these parameters have empty values.

**Note:** If the generated WS endpoint URL returns the private IP of the MID Server, then that private IP needs to be replaced with public IP of the MID Server VM for the internet-based connectivity.

3.  There should be connectivity over SSH port from the MID Server to the provisioned VM.

 In case of any failure in installing agent on the provisioned VM, a task is created, and stack is set to a 'follow-up required' state and automatically turns active, once all the follow-on tasks are closed.

</td></tr><tr><td>

CCG Scan in post provisioning

</td><td>

CSC Content- Create CCG Policy Scan on Stack Items

</td><td>

CCG Scan with the default OOB Policy Set in CCG is called with the simple windows and Linux deployment. When a CCG scan fails owing to violation, the stack is set to a follow-up needed state. The operator must ensure that the violation is remediated and close the violation task. Once all the follow-on tasks are closed, the stack automatically turns to active state and can be used by requester.

</td></tr><tr><td>

Tagging Action

</td><td>

CSC Content- Post Provisioning- Update Key Values in CMDB

</td><td>

All catalog items have a tagging action run as post-provision step. This action only updates the key-value entries in CMDB, not in cloud. The standard tags updated are StackName, Application, CostCenter and BusinessService. Fields with empty values will not be saved as key-value records.

</td></tr><tr><td>

Retrieve Windows Password

</td><td>

CSC Content- Post Provisioning- Retrieve Windows Password

</td><td>

All windows catalogs have a retrieve password action, which emails the Administrator, the password of the provisioned windows VM to the requester. The password is obtained from AWS after the deployment is complete using a ssh key \('pem'\) file to decrypt the password. Follow these pre-requisite steps to set up this pem file on the Terraform Linux server:

 1.  Ensure that the SSH Private Key credential to the VM with Terraform CLI installed, is associated with the credential alias named 'TFO Server Credential Alias'. This alias is already created with installation of CSC Content pack. This alias is used to SSH into the terraform server to get the windows password from output variable.
2.  Ensure that in the Catalog’s Provision variable set, the variable called 'keypath' has the default value set to the path of the management key \(the key which can decrypt the password\) on the terraform VM.
3.  Ensure that the requester has set up the email

 **Note:** For custom catalogs, this operation is available for use only, with Terraform Opensource- Linux based catalog items.

</td></tr><tr><td>

Email URL For Microsoft Azure Scalable Web Server Application

</td><td>

CSC Content- Email URL For Microsoft Azure Scalable Web Server Application

</td><td>

This action is added as a post provision operation in 'CSC Microsoft Azure Linux with Scalable Web Server' catalog item, which emails the deployed application's end point URL to the requester.

The URL is obtained from Microsoft Azure after the deployment is complete. Ensure the requester has set up the email.

</td></tr><tr><td>

Retrieve Microsoft Azure Function App Host name

</td><td>

CSC Content- Post Provisioning- Retrieve Microsoft Azure Function App Host name

</td><td>

This action is added as a post provision operation in 'CSC Microsoft Azure Function App catalog item which retrieves the deployed function app's host name to the requester.

</td></tr></tbody>
</table>**Parent Topic:**[Out Of Box Catalogs using Cloud Services Catalog](../concept/out-of-the-box-catalog-items.md)

