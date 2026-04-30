---
title: Set up the Atlassian Administration spoke
description: Integrate the ServiceNow instance and Atlassian Administration by using an API key to authenticate ServiceNow requests.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-11-12"
reading_time_minutes: 1
breadcrumb: [Atlassian Administration Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the Atlassian Administration spoke

Integrate the ServiceNow instance and Atlassian Administration by using an API key to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Atlassian Administration spoke.
-   Create an Atlassian Administration API key.
-   Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the record for **Atlassian Administration** alias.

3.  From the Related Links section, select **Create New Connection &amp; Credential**.

4.  On the form, fill in the fields.

<table id="table_vr3_ndm_jdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr class="sub-head"><td colspan="2">

Connection information

</td></tr><tr><td>

Name

</td><td>

Name of the Atlassian Administration connection.

</td></tr><tr><td>

Connection URL

</td><td>

URL for the connection.This field is automatically set to `https://api.atlassian.com`.

</td></tr><tr><td>

Organization ID

</td><td>

Atlassian Administration Organization ID that you find while [creating an Atlassian Administration API Key](create-atlassian-api-key.md).

</td></tr><tr class="sub-head"><td colspan="2">

Credential information

</td></tr><tr><td>

API Key

</td><td>

The API Key that you find while [creating an Atlassian Administration API Key](create-atlassian-api-key.md).

</td></tr></tbody>
</table>5.  Select **Create**.


