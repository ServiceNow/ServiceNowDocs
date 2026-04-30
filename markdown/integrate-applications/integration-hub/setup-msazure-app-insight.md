---
title: Set up the Azure Application Insights spoke
description: Create a connection alias on your ServiceNow instance. The alias enables your ServiceNow instance to request OAuth tokens from the Microsoft Azure Application Insights and enables the authenticate its requests.Provide the details in the connection alias form. Your ServiceNow instance uses these details to request OAuth tokens from Microsoft Azure Application Insights.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 2
breadcrumb: [Microsoft Azure Application Insights Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the Azure Application Insights spoke

Create a connection alias on your ServiceNow instance. The alias enables your ServiceNow instance to request OAuth tokens from the Microsoft Azure Application Insights and enables the authenticate its requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Microsoft Azure Application Insights spoke.
-   Role required: admin

## Create a connection alias record

Provide the details in the connection alias form. Your ServiceNow instance uses these details to request OAuth tokens from Microsoft Azure Application Insights.

### Before you begin

Role required: admin.

### Procedure

1.  Log in to your ServiceNow instance.

2.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

3.  Select **Integrations**.

4.  Select **Connections**.

5.  In the Search all connections field, search the Microsoft Azure Application Insights connection alias record.

    **Note:** The **Outbound** tab is enabled by default. Or else, toggle to enable it.

6.  On the Microsoft Azure Application Insights connection alias tile, select **View Details**.

7.  Select **Configure**.

8.  Fill the form.

<table id="table_usv_xlj_zcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the connection alias record.

</td></tr><tr><td>

Authorization URL

</td><td>

URL that your ServiceNow instance uses to request OAuth tokens from the Microsoft Azure Application Insights. The URL must in the following format: `https://login.microsoftonline.com/{tenant ID}/oauth2/v2.0/authorize`.

</td></tr><tr><td>

Token URL

</td><td>

URL that your ServiceNow instance uses to get the OAuth token. The URL must in the following format: `https://login.microsoftonline.com/{tenant ID}/oauth2/v2.0/token`.

</td></tr><tr><td>

Token Revocation URL

</td><td>

URL that your ServiceNow instance uses to cancel the OAuth token. The URL must in the following format: `https://login.microsoftonline.com/{tenant ID}/oauth2/v2.0/revoke`.**Note:** This field isn't mandatory.

</td></tr><tr><td>

Client ID

</td><td>

Unique ID of the OAuth application that you created on Microsoft Azure Application Insights. The Microsoft Azure Application Insights uses this ID to authenticate your ServiceNow instance requests.

</td></tr><tr><td>

Client Secret

</td><td>

The secret that Microsoft Azure Application Insights uses to authenticate your ServiceNow instance requests. You generate the client secret when you create the OAuth application on Microsoft Azure Application Insights.

</td></tr><tr><td>

Redirect URL

</td><td>

Specific address where the third-party application sends your ServiceNow instance back after the request is authenticated. You must set the redirect URL when you create the OAuth application on Microsoft Azure Application Insights.

</td></tr></tbody>
</table>9.  Select **Configure and Get OAuth Token**.

    You're required to log in to [https://portal.azure.com/](https://portal.azure.com/) before the OAuth token is provided.

    On successful authentication, the request is authenticated and the OAuth token is available.


