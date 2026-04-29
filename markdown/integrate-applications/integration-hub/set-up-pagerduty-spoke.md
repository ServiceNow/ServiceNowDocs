---
title: Set up PagerDuty spoke
description: Set up an outbound integration between your ServiceNow instance and the PagerDuty server with a connection and credential record.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [PagerDuty Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up PagerDuty spoke

Set up an outbound integration between your ServiceNow instance and the PagerDuty server with a connection and credential record.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the PagerDuty spoke.
-   Access to the PagerDuty application so you can set up the OAuth 2.0 app.
-   Role required: admin.

## Procedure

1.  Set up PagerDuty as the OAuth provider.

    1.  Log in to the PagerDuty application.![Log in page for PagerDuty application.](../image/pagerduty-spoke-log-in.png)

    2.  Navigate to **Integrations** &gt; **DEVELOPER TOOLS** &gt; **App Registration.**![App registration link.](../image/pagerduty-spoke-app-reg.png)

    3.  Select **Create New App**.

    4.  In the App Name field, enter a unique name for the OAuth app.

    5.  In the Brief Description field, enter a brief description of the OAuth app.

    6.  Select **Save**.

    7.  Under the Classic User OAuth heading, select **Add**.![Add OAuth button.](../image/pagerduty-spoke-add-oauth.png)

    8.  In the Redirect URL field, enter your ServiceNow instance URL.

    9.  Select **Save**.

        PagerDuty generates the client ID and client secret.![Client ID and secret.](../image/pagerduty-oauth-secret.png)

    10. Copy and store the client ID and secret.

        You need the client ID and secret when you set up the connection and credential record.

        You have set the PagerDuty OAuth app.

2.  Set up the connection and credential record.

    1.  Log in to your ServiceNow instance.

    2.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer.**

    3.  Select Connections.

    4.  In the Search all connections field, enter `PagerDuty`.

    5.  On the PagerDuty tile, select **View Details**.

    6.  Select **Configure**.

    7.  Fill the Create Connection form.

<table id="table_mqb_dnl_4xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the connection.**Note:** The default and read-only name of the first connection is PagerDuty. To provide a custom name for the connection, select **Add Connection**.

</td></tr><tr><td>

Name

</td><td>

Name of the credential.**Note:** The default and read-only name of the first credential is PagerDuty. To provide a custom name for the credential, select **Add Connection**.

</td></tr><tr><td>

OAuth Client ID

</td><td>

OAuth client ID that you generated when you set up the OAuth app.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

OAuth client secret that you generated when you set up the OAuth app.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

The redirect URL that you had provided when you set up the OAuth app.

</td></tr></tbody>
</table>    8.  Select **Create and Get OAuth Token**.

        The OAuth token becomes available.![OAuth token is available.](../image/pagerduty-oauth-generated.png)


