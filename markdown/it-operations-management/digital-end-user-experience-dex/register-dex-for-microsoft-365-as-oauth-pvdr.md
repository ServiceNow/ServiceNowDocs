---
title: Configure a connection for DEX for Microsoft 365
description: Configure the Microsoft Teams connection to authenticate ServiceNow requests in DEX for Microsoft 365.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/register-dex-for-microsoft-365-as-oauth-pvdr.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-10-23"
reading_time_minutes: 1
breadcrumb: [Configuring DEX for Microsoft 365, Configure, Digital End-User Experience, IT Operations Management]
---

# Configure a connection for DEX for Microsoft 365

Configure the Microsoft Teams connection to authenticate ServiceNow requests in DEX for Microsoft 365.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select the **Integrations** tab.

3.  Select the **Connections** tab.

4.  Configure the **DEX for Microsoft 365** connection.

    1.  Locate the **DEX for Microsoft 365** connection alias and select **View Details**.

        **Note:** Don't select **Add Connection**.

    2.  Select **Edit** or, if you're configuring DEX for Microsoft 365 for the first time, select **Configure**.

    3.  In the **Configure Connection** form, fill in the fields.

<table id="table_shd_vqw_byb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the alias record associated with this connection. This is set to DEX for Microsoft 365.

</td></tr><tr><td>

Connection URL

</td><td>

Connection URL. Enter `https://graph.microsoft.com`.

</td></tr><tr><td>

API Version

</td><td>

The value is set to **v1.0** by default.If you are using any other API version, update the version number here.

</td></tr><tr><td>

Token URL

</td><td>

OAuth server token endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/token`.

</td></tr><tr><td>

Client ID

</td><td>

Application ID created during application registration.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret created during application registration.

</td></tr></tbody>
</table>    4.  Select **Configure and Get OAuth Token**.


