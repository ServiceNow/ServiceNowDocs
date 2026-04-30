---
title: Run Azure Cloud Discovery using Service Principal with SSH Certificates
description: Discover Linux virtual machines on Azure using Service Principal \(SP\) with short-lived SSH certificates. Using these certificates circumvents the need for passwords or public and private key-pairs.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-12-16"
reading_time_minutes: 1
breadcrumb: [Discovery for Microsoft Azure Cloud, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Run Azure Cloud Discovery using Service Principal with SSH Certificates

Discover Linux virtual machines on Azure using Service Principal \(SP\) with short-lived SSH certificates. Using these certificates circumvents the need for passwords or public and private key-pairs.

## Before you begin

Before creating a Cloud Discovery credentials, Service Principles must be set up on the Azure Portal. See the [Microsoft Azure](https://learn.microsoft.com/en-us/azure/?product=popular) documentation site for more information. After creating a Linux VM with Azure AD login enabled, be sure to verify the requirements for login with Azure AD using OpenSSH certificate-based authentication for Linux VMs. Configure suitable role assignments for the Service Principle and Resource Group.

Before creating credentials, the **External Credential Storage** plugin is required to connect Azure VM using OpenSSH certificates.

Role required: admin

## Procedure

1.  On the instance, navigate to **Discovery** &gt; **Credentials** and select **New**.

2.  For the type of credential, select **Azure Service Principal**.

3.  Fill in the form with the required info and submit.

    ![The Azure Service Principle record.](../image/azure-cloud-disc-ssh-new-record.png)

4.  Navigate to **Discovery** &gt; **Credentials** and select **New**.

5.  For this type of credential, select **Azure SSH Certificate Credential**.

6.  Fill in the form with the necessary information, including linking the Service Principle credential you created.

    The Azure Service Provider and SSH Certificate credentials have been created and linked. Continue the procedure to create the Cloud Discovery schedule.

7.  Navigate to the Cloud Discovery Workspace home page and select **Cloud discovery**.

    ![The Cloud discovery workspace home page.](../image/azure-cloud-disc-ssh-workspace.png)

8.  Select **New discovery schedule**.

9.  Provide a name for the schedule and select **Azure** as the cloud provider.

10. Create a new cloud account using your Azure Service Principal credential.

    For more information, see [Set up Azure service accounts](../../it-operations-management/task/setup-azure-service-accounts.md).

11. Select data centers.

12. Enable the option to discover virtual machines.

13. Complete the schedule creation by selecting **Finish and run**.


## Result

The discovery schedule should start, and the Cloud Operations homepage should show the running status for the newly created schedule. After some time, the scheduled discovery should be completed and a new schedule for the VM discovery is then created and run. The new VM discovery schedule utilizes the SP we created for the generation of SSH certs to authenticate with the VMs. You can observe this in the Discovery IP Affinity section for the credential.

