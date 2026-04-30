---
title: Add an Azure service account
description: During Cloud Provisioning Day 1 setup, you added one service account to the cloud account. To compartmentalize your infrastructure or to include different datacenters, you can add another service account. A particular datacenter, however, cannot be selected in more than one service account in a cloud account. Note: Resource ID
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Day 1 setup guide for Microsoft Azure Cloud on Cloud Provisioning and Governance, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Add an Azure service account

During Cloud Provisioning Day 1 setup, you added one service account to the cloud account. To compartmentalize your infrastructure or to include different datacenters, you can add another service account. A particular datacenter, however, cannot be selected in more than one service account in a cloud account.

## Before you begin

Role required: sn\_cmp.cloud\_admin

## Procedure

1.  Open the `Azure-Credentials.txt` text file that you created during the [Create a Microsoft Azure service principal](azure-create-serv-princ-cloud-mgt-1.md) procedure.

2.  Navigate to **Cloud Admin Portal** &gt; **Manage** &gt; **Service Accounts**.

3.  Click **New**, enter a unique and meaningful **Name**, and then fill in the form.

    ![Paste the Azure Subscription ID value that you copied from the Azure Portal into the text file.](../image/azure-copy-to-service-account.png)

<table id="table_gs3_bdy_my"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Account ID**

</td><td>

The Azure **Subscription ID** value that you copied from the Azure Portal into the text file.

 See [Discovery for Microsoft Azure Cloud](../../discovery/concept/azure-cloud-discovery.md) to learn Management Groups subscription IDs.

</td></tr><tr><td>

**Discovery credentials**

</td><td>

Name of the credentials that you created in the [Store the Azure service principal credentials in the instance](azure-create-creds-cloud-mgt-1.md) procedure. In the example, you used the name `Azure service principal credentials`.

</td></tr><tr><td>

**Datacenter URL**

</td><td>

URL of the datacenter.This field is required only for the government and regional accounts.

 Discovery and Service Mapping Patterns supports the US, Germany, and China Microsoft Azure government clouds.

</td></tr><tr><td>

**Datacenter type**

</td><td>

Select **Azure Datacenter**.

</td></tr><tr><td>

**Datacenter discovery status**

</td><td>

Auto-generated value: Status and timestamp of the last execution of Discovery on the datacenter.

</td></tr><tr><td>

**Should pull events**

</td><td>

Option to enable the ServiceNow AI Platform® to collect resource change information from the Microsoft Azure cloud. The ServiceNow AI Platform® uses the resource change information to update the Configuration Management Database \(CMDB\). For more information on the supported Azure resource types, see [Azure change processing](../../it-operations-management/concept/azure-change-processing.md). If you select the Should pull events check box for a management group, the ServiceNow AI Platform enables Azure change processing for all the subscriptions in the management group.

</td></tr></tbody>
</table>4.  Click **Update** or **Submit**.

    The system creates the service account and displays the list of all discovered datacenters.


## What to do next

After you complete all procedures in this initial "Day 1" setup, you can create additional cloud accounts and service accounts to organize and compartmentalize your cloud infrastructure.

**Note:**

If you are on a domain separated instance, only those events that are updated to the CMDB and belong to your domain are visible. Events create configuration items \(CI\) in the same domain as the cloud service account they are mapped to.

**Related topics**  


[Discovery for Microsoft Azure Cloud](../../discovery/concept/azure-cloud-discovery.md)

