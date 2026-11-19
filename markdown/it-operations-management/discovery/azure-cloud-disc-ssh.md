---
title: Run Azure Cloud Discovery using Service Principal with SSH Certificates
description: Discover Linux virtual machines on Azure using Service Principal \(SP\) with short-lived SSH certificates. Using these certificates circumvents the need for passwords or public and private key-pairs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/azure-cloud-disc-ssh.html
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-24"
reading_time_minutes: 2
breadcrumb: [Discovery for Microsoft Azure Cloud, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Run Azure Cloud Discovery using Service Principal with SSH Certificates

Discover Linux virtual machines on Azure using Service Principal \(SP\) with short-lived SSH certificates. Using these certificates circumvents the need for passwords or public and private key-pairs.

## Before you begin

Before creating a Cloud Discovery credentials, Service Principles must be set up on the Azure Portal. See the [Microsoft Azure](https://learn.microsoft.com/en-us/azure/?product=popular) documentation site for more information. After creating a Linux VM with Azure AD login enabled, be sure to verify the requirements for login with Azure AD using OpenSSH certificate-based authentication for Linux VMs. Configure suitable role assignments for the Service Principle and Resource Group.

Before creating credentials, the **External Credential Storage** plugin is required to connect Azure VM using OpenSSH certificates.

Role required: admin

## Procedure

1.  Navigate to **Discovery** &gt; **Credentials**.

2.  Select **New**.

3.  For the type of credential, select **Azure Service Principal**.

4.  Fill in the form with the required information.

    \[Omitted image "azure-cloud-disc-ssh-new-record.png"\] Alt text: Azure Service Principle record

5.  Select **Submit**.

6.  Navigate to **Discovery** &gt; **Credentials**.

7.  Select **New**.

8.  For this type of credential, select **Azure SSH Certificate Credential**.

9.  Fill in the form with the necessary information, including linking the Service Principle credential you created.

    The Azure Service Provider and SSH Certificate credentials have been created and linked. Continue the procedure to create the Cloud Discovery schedule.

10. Navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Schedules**.

11. Select **New Discovery** from the header of any tab on the Schedules page.

12. Select **Cloud-based discovery** and select **Continue**.

13. Provide a name for the schedule and select **Azure** as the cloud provider.

14. Choose a MID Server.

15. Select **next**.

16. Create a cloud account using your Azure Service Principal credential.

    For more information, see [Set up Azure service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/setup-azure-service-accounts.md).

17. Select **next**.

18. Select cloud regions for the Discovery schedule.

    You can choose to include all regions linked to the cloud account or select specific regions. There’s no restriction on the number of cloud regions that you can add.

    1.  To discover specific cloud regions, select the check box for the cloud region you want to scan from the **Available cloud regions** list.

    2.  If the cloud regions don't appear, select **Refresh cloud regions**.

19. Select **next**.

20. To complement your cloud schedule with an IP-based Discovery schedule, enable the **Create a server discovery schedule** toggle.

    1.  Select a MID Server or cluster that can discover the Virtual Machines \(VM\) and their attributes.

21. Select **next**.

22. Complete the schedule creation by selecting **Finish and run**.


## Result

The Discovery schedule should start, and the Discovery Admin Workspace should show the running status for the newly created schedule. After some time, the scheduled discovery should be completed and a new schedule for the VM discovery is then created and run. The new VM discovery schedule utilizes the SP we created for the generation of SSH certs to authenticate with the VMs. You can observe this in the Discovery IP Affinity section for the credential.

