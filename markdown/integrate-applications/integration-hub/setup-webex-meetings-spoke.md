---
title: Set up Cisco Webex Meetings spoke
description: Integrate your ServiceNow instance and the Cisco Webex Meetings application by creating a custom OAuth application in Cisco DevNet to authenticate ServiceNow requests.Create a custom OAuth application in Cisco DevNet to enable OAuth 2.0 authentication with the Cisco Webex Meetings spoke.Add and configure a Cisco Webex Meetings connection to authenticate ServiceNow requests in the Cisco Webex Meetings spoke.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Cisco Webex Meetings Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up Cisco Webex Meetings spoke

Integrate your ServiceNow instance and the Cisco Webex Meetings application by creating a custom OAuth application in Cisco DevNet to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Cisco Webex Meetings spoke.
-   Role required: admin.

## Create a Webex OAuth application in Cisco DevNet

Create a custom OAuth application in Cisco DevNet to enable OAuth 2.0 authentication with the Cisco Webex Meetings spoke.

### Before you begin

Webex Meetings requirements:

-   Webex Meetings account
-   Role required: Webex Meetings administrator

### Procedure

1.  Navigate to [https://developer.webex.com/](https://developer.webex.com/) and log in.

2.  Click on your profile icon and select **My Webex Apps**.

3.  Click **Create a New App**.

4.  Click **Create an Integration**.

5.  On the form, fill in the fields.

<table id="table_hdn_c55_mjb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Integration name

</td><td>

Name of the integration as it appears in Webex. For example, ServiceNow integration.

</td></tr><tr><td>

Icon

</td><td>

Icon that displays in Webex. Upload your own icon and select from the available default icons.

</td></tr><tr><td>

App Hub Description

</td><td>

Short description about the integration.

</td></tr><tr><td>

Redirect URI\(s\)

</td><td>

`https://<instance-name>.service-now.com/oauth_redirect.do`, where `<instance-name>` is the name of your ServiceNow instance

</td></tr><tr><td>

Scope

</td><td>

Webex Meetings application scope permissions you want the application to support.**Note:** Select the **admin\_schedule\_read scope** for the integration.

</td></tr></tbody>
</table>6.  Click **Add Integration**.

    After the integration is successfully created, the values of **Client ID** and **Client Secret** are displayed.

7.  Record the client ID and client secret to register the application as a third-party OAuth provider on your ServiceNow instance.


## Configure a connection for Cisco Webex Meetings spoke

Add and configure a Cisco Webex Meetings connection to authenticate ServiceNow requests in the Cisco Webex Meetings spoke.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the **Webex** connection alias and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Cisco Webex Meetings spoke, click **View Details**.

        ![Click View Details to configure the default connection and credential alias record.](../image/cisco-webex-meetings-conf1.png)

    -   To manage more than one Cisco Webex Meetings spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    ![Click Configure if you are configuring the spoke for the first time.](../image/cisco-webex-meetings-conf2.png)

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Information|
    |Connection URL|`https://<site>.webex.com/WBXService/XMLService`, where *site* is the name of your Webex site.|
    |Webex Admin User Name|User name for the Webex administrator account.|
    |Credential Information|
    |OAuth Client ID|Client ID you created during the Webex app configuration.|
    |OAuth Client Secret|Client Secret you created during the Webex app configuration.|
    |OAuth Redirect URL|`https://<instance-name>.service-now.com/oauth_redirect.do`, where *instance-name* is the name of your ServiceNow instance.|

    ![Configure a connection for the Cisco Webex Meetings spoke.](../image/cisco-webex-meetings-conf3.png)

6.  Click **Configure and Get OAuth Token**.


### Result

The spoke is configured and ready to be used.

