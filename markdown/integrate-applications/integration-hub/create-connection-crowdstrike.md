---
title: Create a CrowdStrike connection
description: Create a connection between your CrowdStrike applications and your ServiceNow instance so that your instance can retrieve user data from your applications.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-02-04"
reading_time_minutes: 1
breadcrumb: [CrowdStrike Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Create a CrowdStrike connection

Create a connection between your CrowdStrike applications and your ServiceNow instance so that your instance can retrieve user data from your applications.

## Before you begin

ServiceNow Role required: admin

## Procedure

1.  Log in to your ServiceNow instance.

2.  Navigate to **Connection &amp; Credentials** &gt; **Connection &amp; Credentials Aliases**.

3.  Locate your CrowdStrike connection and select **Create New Connection &amp; Credential**.

4.  In the dialog box, fill in the fields.

<table id="table_xg1_fmt_hrb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td colspan="2">

Connection Information

</td></tr><tr><td>

Connection Name

</td><td>

Name of the CrowdStrike connection. This field populates automatically.

</td></tr><tr><td>

Connection URL

</td><td>

URL for the connection. This field is automatically set to `https://api.crowdstrike.com`.Each CrowdStrike cloud has a different base URL. Use the base URL that corresponds to the cloud where your integration is hosted.

-   **US-1**: `https://api.crowdstrike.com`
-   **US-2**: `https://api.us-2.crowdstrike.com`
-   **EU-1**: `https://api.eu-1.crowdstrike.com`
-   **US-GOV-1**: `https://api.laggar.gcw.crowdstrike.com`
-   **US-GOV-2**: `https://api.us-gov-2.crowdstrike.mil`


</td></tr><tr><td colspan="2">

Credential Information

</td></tr><tr><td>

OAuth Client ID

</td><td>

Client ID that you generated while configuring the CrowdStrike API settings.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client Secret that you generated while configuring the CrowdStrike API settings.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

`https://<instance name>/oauth_redirect.do`, where the instance name is the name of your ServiceNow instance.

</td></tr></tbody>
</table>5.  Select **Create and Get OAuth Token**.

    The OAuth token is generated successfully.


