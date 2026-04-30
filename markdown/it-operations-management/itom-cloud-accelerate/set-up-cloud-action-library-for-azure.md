---
title: Set up Cloud Action Library for Microsoft Azure
description: Set up access to the Microsoft Azure cloud accounts in Cloud Action Library to enable interaction between the application and the cloud.
locale: en-US
release: zurich
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exploring Cloud Action Library, Cloud Action Library, ITOM Cloud Accelerate, IT Operations Management]
---

# Set up Cloud Action Library for Microsoft Azure

Set up access to the Microsoft Azure cloud accounts in Cloud Action Library to enable interaction between the application and the cloud.

## Before you begin

Role required: admin

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


**Parent Topic:**[Exploring Cloud Action Library](../concept/exploring-cloud-actions-library.md)

