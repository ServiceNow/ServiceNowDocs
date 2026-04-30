---
title: Set up Azure service accounts
description: Create and configure cloud service accounts at ServiceNow AI Platform for the corresponding Microsoft Azure accounts.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Setting up a cloud service account, Access to cloud environments for ITOM products, IT Operations Management]
---

# Set up Azure service accounts

Create and configure cloud service accounts at ServiceNow AI Platform for the corresponding Microsoft Azure accounts.

## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

## Before you begin

-   **Ensure the configuration of Azure credentials**

    For more information, see [Create Azure cloud credentials](../../discovery/task/create-azure-cloud-credentials.md) and [Configuration steps for Azure Service Principal User and Credentials \(KB2202765\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2202765)

-   **Ensure that you are familiar with the hierarchy of the Azure service accounts in your environment.**

    Set up the service accounts at ServiceNow AI Platform to reflect the hierarchy of your environment. You can set up the Azure service accounts for the following Azure account types:

    -   Management group.
    -   Subscription.

Role required: discovery\_admin

## About this task

A service account is a secure record on your instance that stores the credentials and access information for your provider account. Discovery uses the information to access your provider account to get data on each resource in each specified datacenter. A cloud account is the logical representation in cloud management of all or part of your managed cloud infrastructure. A cloud account can include multiple service accounts—even service accounts from different providers. For each service account, you specify which datacenter to include in the cloud account.

## Procedure

1.  In the navigation filter, enter `cmdb_ci_cloud_service_account.list`.

2.  Select **New**.

3.  Fill in the fields by the following order:

    1.  Select the datacenter.
    2.  Select the check box of the **Is management account** if your are creating a service account for a management group.
    3.  Select **Should pull events** to preform event-based discovery. For more information, see [Microsoft Azure Alert driven discovery](../concept/microsoft-azure-alert-driven-discovery.md#)
<table id="table-azure-service-acct-form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The unique and meaningful name for this service account.

</td></tr><tr><td>

Account ID

</td><td>

If you are creating a service account for a management group, fill in the Azure management group ID that belongs to the management group. If you are creating a service account for a subscription, fill in the Azure subscription ID.

</td></tr><tr><td>

Discovery credentials

</td><td>

The credentials needed for ServiceNow applications to access this account.

</td></tr><tr><td>

Datacenter URL

</td><td>

URL of the datacenter.

 Configuring this field is required for Azure Gov Cloud \(US\) accounts. For example, [https://management.usgovcloudapi.net/.](https://management.usgovcloudapi.net/.)

</td></tr><tr><td>

Datacenter type

</td><td>

Type of the datacenter where the account is hosted.Select **Azure datacenter**.

</td></tr><tr><td>

Datacenter discovery status

</td><td>

Auto-generated value: Status and timestamp of the last execution of discovery on the datacenter.

</td></tr><tr><td>

Parent account

</td><td>

When setting up a service account for an Azure subscription, fill in the management group ID.

 When the **Is management account** check box is selected, the **Parent account** field is not applicable

</td></tr><tr><td>

Accessor account

</td><td>

Not applicable for Azure service accounts.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Setting up a cloud service account](../concept/setup-cloud-service-account.md)

**Related topics**  


[Azure Cloud Discovery](../../discovery/concept/azure-cloud-discovery.md)

