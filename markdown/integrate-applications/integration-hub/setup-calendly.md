---
title: Set up the Calendly spoke
description: Set up an outbound integration between your ServiceNow instance and the Calendly APIs by creating an OAuth application in Calendly and a connection and credential record on your ServiceNow instance.Set up an OAuth application that authenticates requests from your ServiceNow instance.Create a connection and credential record that contains the details required to access the Calendly APIs.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-20"
reading_time_minutes: 2
breadcrumb: [Calendly Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the Calendly spoke

Set up an outbound integration between your ServiceNow instance and the Calendly APIs by creating an OAuth application in Calendly and a connection and credential record on your ServiceNow instance.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Calendly spoke.
-   Ensure that you have a Calendly account.
-   Role required: admin.

## About this task

After setting the outbound integration, you can set up a flow on the Workflow Studio using the Calendly spoke actions and automate tasks in Calendly. For example, you can set up a flow that cancels an event on Calendly. The connection and credentials record contains the credentials to establish a connection with the Calendly APIs before you automate the tasks on Calendly. The OAuth application authenticates the connection request from your ServiceNow instance.

## Set up an OAuth application in Calendly

Set up an OAuth application that authenticates requests from your ServiceNow instance.

### Before you begin

Role required: Calendly organization owner or admin

### Procedure

1.  Go to [https://developer.calendly.com/](https://developer.calendly.com/).

2.  Log in to the developer portal.

3.  Select **+ Create new app**.

4.  Fill the form.

    |Field|Description|Mandatory?|
    |-----|-----------|----------|
    |Name of app|Custom name of the OAuth application.|Yes|
    |Kind of app|Type of application the OAuth app will support. Select **Web**.|Yes|
    |Environment type|Type of environment in which the OAuth app will be deployed.|Yes|
    |Redirect URI|The URL of your ServiceNow instance.|Yes|

5.  Select **Save &amp; Continue**.

    The client ID and client secret that you use in the connection and credentials record are generated.

6.  To copy the client ID, select **Copy**.

7.  To copy the client secret, select **Copy**.

    ![Calendly OAuth details.](../image/calendly-spoke-oauth.png)

8.  Select **Return to My Apps**.

    The OAuth app is created.

    ![OAuth app created.](../image/calendly-spoke-oauth-created.png)


## Create a connection and credential record

Create a connection and credential record that contains the details required to access the Calendly APIs.

### Before you begin

Role required: ServiceNow admin

### Procedure

1.  Log in to your ServiceNow instance.

2.  Navigate to **Process Automation** &gt; **Workflow Studio**.

3.  Select **Integrations**.

4.  In the Search all connections field, enter `Calendly`.

    ![Enter Calendly in the search field.](../image/calendly-search.png)

    **Note:** The **Outbound** tab is enabled by default. Confirm that the **Outbound** tab is enabled already.

5.  On the Calendly card, select **View Details**.

    ![View Details button on Calendly card.](../image/calendly-click-view-details.png)

6.  Select **Configure**.

    ![Configure button for Calendly connection.](../image/calendly-click-configure-button.png)

7.  Fill the form.

<table id="table_ujr_ps1_wmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the connection.**Note:** The first and default connection name is read-only. To provide a custom name, create a connection by selecting **Add Connection**.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL for the Calendly Application Programming Interface \(API\). This field is automatically set to `https://api.calendly.com`.

</td></tr><tr><td>

OAuth Client ID

</td><td>

Client ID that you had generated on the Calendly developers portal. To learn how to generate a client ID, see [Set up an OAuth application in Calendly](setup-calendly.md#).

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client ID that you had generated on the Calendly developers portal. To learn how to generate a client secret, see [Set up an OAuth application in Calendly](setup-calendly.md#).

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

URL of the OAuth provider that users are redirected to after authentication. This field populates automatically based on your instance name.

</td></tr></tbody>
</table>8.  Select **Configure and Get OAuth Token**.

9.  Select **Connect to Calendly**.

    The OAuth refresh token becomes available.

    ![Connection and credential record created for Calendly.](../image/calendly-spoke-conn-cred-created.png)

10. To get the OAuth token, select **Get OAuth Token**.

    **Important:** To get the OAuth token, log in to [https://calendly.com/app/login](https://calendly.com/app/login) with your licensed account credentials.


