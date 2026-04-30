---
title: Set up Cloud Configuration Governance for Microsoft Azure
description: Set up access to the Microsoft Azure cloud accounts in Cloud Configuration Governance to enable interaction between the application and the cloud. The application requires access to the cloud accounts of your organization to scan the cloud resources for non-compliant configurations and remediate them.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Exploring Cloud Configuration Governance, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Set up Cloud Configuration Governance for Microsoft Azure

Set up access to the Microsoft Azure cloud accounts in Cloud Configuration Governance to enable interaction between the application and the cloud. The application requires access to the cloud accounts of your organization to scan the cloud resources for non-compliant configurations and remediate them.

## Before you begin

Role required: sn\_itom\_ccg.scheduling\_admin

## Procedure

1.  Create Microsoft Azure credentials that can access the Microsoft Azure account.

    For more information, see [Create Azure cloud credentials](../../discovery/task/create-azure-cloud-credentials.md).

2.  Create an Integration Hub connection for Microsoft Azure.

    1.  Navigate to **Process Automation** &gt; **Flow Designer**, and select the **Integrations** tab.

    2.  On the **Azure Connection** tile, select **Add Connection**.

    3.  On the form, fill in the fields.

<table id="table_zts_4jv_gsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name of the connection.

</td></tr><tr><td>

OAuth client ID

</td><td>

Microsoft Azure application ID.

</td></tr><tr><td>

OAuth client secret

</td><td>

Microsoft Azure application key.

</td></tr><tr><td>

OAuth token URL

</td><td>

Tenant ID of the Microsoft Azure account.Replace `{tenant}` with the Microsoft Azure tenant ID.

</td></tr></tbody>
</table>    4.  Select **Create and Get OAuth Token**.

3.  Run datacenter discovery to identify the datacenters attached with the service accounts.

    For more information, see [Run datacenter discovery](../../cloud-management-v2-setup/task/disco-datacntrs-in-srv-acct.md).


**Parent Topic:**[Exploring Cloud Configuration Governance](../concept/exploring-cloud-configuration-governance.md)

