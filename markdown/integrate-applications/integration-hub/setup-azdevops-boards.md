---
title: Set up the Microsoft Azure DevOps Boards Spoke using personal access token
description: Integrate the ServiceNow instance and Azure DevOps Boards using basic authentication to authenticate ServiceNow requests.Authenticate Azure DevOps Boards by using the personal access tokens.Add and configure a Azure DevOps Boards connection to authenticate ServiceNow requests.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-09-10"
reading_time_minutes: 4
breadcrumb: [Microsoft Azure DevOps Boards Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the Microsoft Azure DevOps Boards Spoke using personal access token

Integrate the ServiceNow instance and Azure DevOps Boards using basic authentication to authenticate ServiceNow requests.

## Before you begin

-   Request Integration Hub subscription
-   Activate Azure DevOps Boards spoke
-   Role required: admin

## About this task

If you want to use different connections in your flow, subflows, and actions, create the child alias and select the default alias record as its parent. To configure the child alias, perform the same steps that are needed to configure the parent alias. Depending on your requirement and set up, you can choose either the parent alias or child alias in your flow, subflows, and actions.

You can also use multiple Azure DevOps accounts. In this case, you should provide the respective **Password** while configuring the credential record and specify the relevant **Connection URL** while configuring the connection record.

## Obtain the personal access token

Authenticate Azure DevOps Boards by using the personal access tokens.

### Before you begin

Role required: admin

### Procedure

1.  Log in to your Azure DevOps portal as an admin.

2.  Navigate to **User Settings** &gt; **Personal access tokens**.

    ![Generate personal access token.](../image/pat-devops.png)

3.  Click **New Token**.

4.  On the form, fill the required fields.

    ![Create personal access token.](../image/create-pat-devops.png)

5.  Click **Create**.

    ![Copy the personal access token.](../image/pat-display-devops.png)

    The token is displayed.

6.  Copy and record the value of token for later use.


## Configure a connection record for Microsoft Azure DevOps Boards Spoke

Add and configure a Azure DevOps Boards connection to authenticate ServiceNow requests.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **New**.

3.  Under What type of Credentials would you like to create?, select Basic Auth Credentials.

4.  Fill the form.

    |Field|Details|
    |-----|-------|
    |Name|Option to provide the name that identifies the record.|
    |Order|Option to provide the order in which the credentials are used. For example, enter `100`.|
    |User name|Option to provide the user name that you enter as credential.|
    |Password|Option to provide the password that you enter as credential.|
    |Active|Option to actively use the credential record. Select the option.|

5.  Select **Submit**.

    The credentials are created.

6.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

7.  Search for the alias Azure\_DevOps\_Boards.

8.  Select the alias Azure\_DevOps\_Boards.

9.  Under the **Connections** tab, select **New**.

10. Fill the form.

<table id="table_uvy_tzd_b2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Option to provide a unique name of the connection.

</td></tr><tr><td>

Active

</td><td>

Option to indicate that this connection is active.**Note:** You can keep either the connection record for the OAuth 2.0 or that for the Basic Auth active. If you want to keep both connection records active, create one of the connection records under a child alias under the Azure\_DevOps\_Boards connection and credential alias.

</td></tr><tr><td>

Credential

</td><td>

Option to select the credential that you have created earlier.

</td></tr><tr><td>

Domain

</td><td>

Option to provide the domain to which the connection belongs.

</td></tr><tr><td>

Connection alias

</td><td>

Option to provide the parent connection alias. This field is automatically set to `sn_azure_dev_spoke.Azure_DevOps_Boards`.

</td></tr><tr><td>

URL builder

</td><td>

Either manually enter the connection URL or use system to build the URL based on the inputs. Default is unchecked. If checked, the connection URL is calculated from the following fields: -   Mutual authentication — Check box if mutual authentication is used.
-   Protocol — If mutual authentication is not used, enter protocol. The default is HTTPs.
-   Protocol profile — If mutual authentication is used, enter protocol profile from sys\_protocol\_profile.
-   Host
-   Port
-   Base path — Path of the connection string.
 **Note:** If mutual authentication is checked, connection URL is built: Protocol + :// + host:port +URL. If mutual authentication is unchecked, connection URL is built: Protocol profile + :// + host:port +URL

</td></tr><tr><td>

Connection URL

</td><td>

If URL builder is unchecked, enter the connection URL into this field.**Note:** If mutual authentication is checked, connection URL is built: Protocol + :// + host:port +URL. If mutual authentication is unchecked, connection URL is built: Protocol profile + :// + host:port +URL

</td></tr><tr><td>

Use MID server

</td><td>

Option to specify MID server.

</td></tr><tr><td>

Connection timeout

</td><td>

Number of milliseconds the system waits for a successful host connection. If a successful connection does not occur during this time, the connection request times out. Leave this field empty to use the system default connection timeout value.

</td></tr></tbody>
</table>11. Select **Submit**.

12. Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

13. Click the **Integrations** tab.

14. Under **Connections**, toggle and enable the **Outbound** connections.

15. Locate the alias for **Azure\_DevOps\_Boards** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Azure DevOps Boards spoke, click **View Details**.

        ![Connection for Azure DevOps Board spoke](../image/conn-config-template-azdevops2.png)

    -   To manage more than one Azure DevOps Boards spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    ![First-time connection configuration](../image/conn-config-template-azdevops1.png)

16. On the **Configure Connection** form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to uniquely identify the connection record. For example, enter `Azure DevOps Boards Connection`.|
    |Connection URL|URL of the Azure DevOps instance. For example, enter the URL in this format: `https://dev.azure.com/<instance-name>`.|
    |User name|User name to log in to your Azure DevOps instance.|
    |Password|Personal access token to authenticate Azure DevOps.|

    ![Configure a connection for Azure DevOps Boards spoke.](../image/azdevops-conn-template.png)

17. Click **Configure Connection**.


### Result

The spoke connection is configured and ready to be used.

