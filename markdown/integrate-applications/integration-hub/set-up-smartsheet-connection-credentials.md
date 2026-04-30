---
title: Set up Smartsheet spoke connection and credentials
description: Set up the connection and credential record to enable the ServiceNow instance to get authenticated and connected to Smartsheet.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-05-09"
reading_time_minutes: 1
breadcrumb: [Set up the Smartsheet spoke, Smartsheet Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up Smartsheet spoke connection and credentials

Set up the connection and credential record to enable the ServiceNow® instance to get authenticated and connected to Smartsheet.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Connection &amp; Credential Aliases**.

2.  Open the record for the Smartsheet alias.

3.  From the Related Links section, select **Create New Connection &amp; Credential**.

    The following example shows the Create New Connection &amp; Credential link that you select to set up a connection and credential record.

    ![Smartsheet connection and credential record creation link.](../image/smartsheet-connection-cred1.png "Smartsheet connection and credential record creation link")

4.  On the form, fill in these fields.

<table id="table_kgr_cxz_1wb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

User name that is used to connect to Smartsheet.

</td></tr><tr><td>

Connection URL

</td><td>

This field is automatically set to `https://api.smartsheet.com`. **Note:** Based on regions, replace the Connection URL with these respective URLs:

-   Smartsheet Gov: `https://api.smartsheetgov.com/`
-   Smartsheet Regions Europe: `https://api.smartsheet.eu/`
-   Smartsheet Regions Australia: `https://api.smartsheet.au/`


</td></tr><tr><td>

API Key

</td><td>

Application Programming Interface \(API\) key that is generated on Smartsheet. **Note:** To learn how to generate the API key, see [Generate the Smartsheet Application Programming Interface \(API\) key](generate-smartsheet-api-key.md).

</td></tr></tbody>
</table>5.  Select **Create**.

    A new connection and credential record is created in the **Connections** tab. This record is the default record unless you create another record and set that one as the default.

    The following example shows that a connection and credential record is created and available under the **Connections** tab.

    ![Smartsheet connection and credential record created.](../image/smartsheet-connection-cred-created.png)


