---
title: Set up the Qualtrics spoke
description: Integrate the ServiceNow instance and Qualtrics by registering Qualtrics as an OAuth provider to authenticate ServiceNow requests.Copy and record the values of token, Organization ID, Client ID, and Client secret from your Qualtrics account for authentication.Add and configure a Qualtrics connection to authenticate ServiceNow requests.Configure the system parameter sn\_qualtrics\_spoke.qualtrics\_directory and specify the Qualtrics Directory ID that can be used in the flows.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Qualtrics Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the Qualtrics spoke

Integrate the ServiceNow instance and Qualtrics by registering Qualtrics as an OAuth provider to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Qualtrics spoke.
-   Role required: admin.

## Obtain required details from Qualtrics account

Copy and record the values of token, Organization ID, Client ID, and Client secret from your Qualtrics account for authentication.

### Before you begin

Role required: admin

### Procedure

1.  Log in to your Qualtrics account as an admin.

2.  Navigate to **Account Settings** &gt; **Qualtrics IDs**.

3.  Under **User**, copy and record the values of **Organization ID** and **Datacenter ID**.

4.  Under **Directories**, copy and record the value of **Default Directory**.

5.  Under **API**, copy and record the value of **Token**.

    ![Copy the required values from Qualtrics account.](../image/qualtrics-values.png)

6.  Click the **OAuth Client Manager** tab.

7.  Click **Create Client**.

8.  On the form, fill the values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the client record.|
    |Scopes|Select `manage:all`.|
    |Grant Type|Select `Client Credentials`.|

9.  Click **Create Client**.

    ![Copy and record the values of client ID and client secret.](../image/qualtrics-clientvalues.png)

    The values of Client ID and Client Secret are displayed. Copy and record these values for later use.


## Configure a connection

Add and configure a Qualtrics connection to authenticate ServiceNow requests.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **Process Automation** &gt; **Flow Designer**.

2.  Click the **Connections** tab.

3.  Locate the alias for **Qualtrics** and click **View Details**.

    **Note:** Don't click **Add Connection**.

    ![View connection details.](../image/qualtrics-view.png)

4.  If you are configuring the spoke for the first time, click **Configure**.

    ![Configure connection record.](../image/qualtrics-conf.png)

5.  On the Configure Connection form, fill in the fields.

<table id="table_vfh_vjg_dtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name to identify the connection record.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL to connect to **Qualtrics**. Enter: `https:<Organization-ID>.qualtrics.com/API/v3`

</td></tr><tr><td>

X-API-TOKEN

</td><td>

Unique token you had copied from the Qualtrics account settings.

</td></tr><tr><td>

OAuth Name

</td><td>

Name to identify the application registry record.

</td></tr><tr><td>

OAuth Client ID

</td><td>

Client ID you had copied when you created a client in your Qualtrics account.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client Secret you had copied when you created a client in your Qualtrics account.

</td></tr><tr><td>

Token URL

</td><td>

OAuth server token endpoint. Enter: `https://<Data-Center-ID>.qualtrics.com/oauth2/token`.**Note:** Select the Qualtrics data center based on your geographic location.

</td></tr></tbody>
</table>6.  Click **Configure and Get OAuth Token**.


### Result

The spoke is configured and ready to be used.

## Configure system parameter

Configure the system parameter **sn\_qualtrics\_spoke.qualtrics\_directory** and specify the Qualtrics Directory ID that can be used in the flows.

### Before you begin

Role required: admin.

### Procedure

1.  In the filter navigator, enter `sys_properties.list`.

2.  Search and open the record with **Name** as **sn\_qualtrics\_spoke.qualtrics\_directory**.

3.  In **Value**, specify the Qualtrics Directory ID.

4.  Click **Update**.


