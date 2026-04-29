---
title: Run Azure Cloud Discovery using Service Principal with SSH Certificates
description: Discover Linux virtual machines on Azure using Service Principal \(SP\) with short-lived SSH certificates. Using these certificates circumvents the need for passwords or public and private key-pairs.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Discovery for Microsoft Azure, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Run Azure Cloud Discovery using Service Principal with SSH Certificates

Discover Linux virtual machines on Azure using Service Principal \(SP\) with short-lived SSH certificates. Using these certificates circumvents the need for passwords or public and private key-pairs.

## Before you begin

Before creating a Cloud Discovery credentials, Service Principles must be set up on the Azure Portal. See the [Microsoft Azure](https://learn.microsoft.com/en-us/azure/?product=popular) documentation site for more information. After creating a Linux VM with Azure AD login enabled, be sure to verify the requirements for login with Azure AD using OpenSSH certificate-based authentication for Linux VMs. Configure suitable role assignments for the Service Principle and Resource Group.

Before creating credentials, the **External Credential Storage** plugin is required to connect Azure VM using OpenSSH certificates.

Role required: admin

## Procedure

1.  Navigate to **Discovery** &gt; **Credentials** and select **New**.

2.  For the type of credential, select **Azure Service Principal**.

3.  Fill in the form with the required info and submit.

    ![The Azure Service Principle record.](../image/azure-cloud-disc-ssh-new-record.png)

4.  Navigate to **Discovery** &gt; **Credentials** and select **New**.

5.  For this type of credential, select **Azure SSH Certificate Credential**.

6.  Fill in the form with the necessary information, including linking the Service Principle credential you created.

    The Azure Service Provider and SSH Certificate credentials have been created and linked. Continue the procedure to create the Cloud Discovery schedule.

7.  Navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Schedules**.

8.  Select **New Discovery** from the header of any tab on the Schedules page.

9.  Select **Cloud-based discovery** and select **Continue**.

10. Provide a name for the schedule and select **Azure** as the cloud provider.

11. Choose a MID Server.

12. Select **next**.

13. Create a new cloud account using your Azure Service Principal credential.

    For more information, see [Set up Azure service accounts](../../it-operations-management/task/setup-azure-service-accounts.md).

14. Select **next**.

15. Select cloud regions for the discovery schedule.

    You can choose to include all regions linked to the cloud account or select specific regions. There’s no restriction on the number of cloud regions that you can add.

    1.  To discover specific cloud regions, select the check box for the cloud region you want to scan from the **Available cloud regions** list.

    2.  If the cloud regions don't appear, select **Refresh cloud regions**.

16. Select **next**.

17. To complement your cloud schedule with an IP-based Discovery schedule, enable the **Create a server discovery schedule** toggle.

    1.  Select a MID Server or cluster that can discover the Virtual Machines \(VM\) and their attributes.

18. Select **next**.

19. Complete the schedule creation by selecting **Finish and run**.


## Result

The Discovery schedule should start, and the Discovery Admin Workspace should show the running status for the newly created schedule. After some time, the scheduled discovery should be completed and a new schedule for the VM discovery is then created and run. The new VM discovery schedule utilizes the SP we created for the generation of SSH certs to authenticate with the VMs. You can observe this in the Discovery IP Affinity section for the credential.

