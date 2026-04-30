---
title: Set up Saba spoke
description: Integrate your Saba application with your ServiceNow instance. Register an OAuth application in Saba and authenticate requests from a ServiceNow instance.Use the information generated during the Saba application creation and configuration to register Saba as an OAuth provider and allow the instance to request OAuth 2.0 tokens.Create connection records to your Saba application. The Saba spoke connection and credential alias uses these connections to perform actions in Saba.Authorize the Saba spoke actions by creating credential records for the application registered in Saba. The Saba spoke connection and credential alias uses these credentials to authorize actions.Integrate the ServiceNow instance and Saba instance by using the basic Auth credentials to authenticate ServiceNow requests.Create a record to provide details and credentials of the required Saba user. The Saba spoke uses these user credentials to perform actions in Saba.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Saba Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up Saba spoke

Integrate your Saba application with your ServiceNow instance. Register an OAuth application in Saba and authenticate requests from a ServiceNow instance.

## Before you begin

-   Request Integration Hub subscription.
-   Activate the Saba spoke.
-   Saba integration user or admin credentials.
-   Role required: admin.

**Note:** Make sure that the application registry, connections, and credentials are within the application scope.

## Register Saba as an OAuth provider

Use the information generated during the Saba application creation and configuration to register Saba as an OAuth provider and allow the instance to request OAuth 2.0 tokens.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **System OAuth** &gt; **Application Registry**.

2.  Open the record for the Saba spoke.

3.  On the form, fill in the fields.

    |Field|Value required|
    |-----|--------------|
    |Name|Name to uniquely identify the record.|
    |Client ID|Client ID created during the application configuration in Saba.|
    |Client Secret|Client Secret created during the application configuration in Saba.|
    |Default Grant type|Grant type used to establish the token: **Authorization Code**|
    |Application|Application scope that contains this record: **Saba Spoke**|
    |Accessible from|Application scope that this registry is accessible from.|
    |Active|Option to actively use the application registry. Select the option.|
    |Token URL|OAuth server token endpoint.|

4.  Right-click the form header, and click **Save**.


## Create connection record for the Saba spoke

Create connection records to your Saba application. The Saba spoke connection and credential alias uses these connections to perform actions in Saba.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the record for the Saba spoke.

3.  From the **Connections** tab, click **New**.

4.  On the form, fill these values.

<table id="table_any_shp_gfb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the connection record.

</td></tr><tr><td>

Credential

</td><td>

OAuth credential record you created for Saba.

</td></tr><tr><td>

Connection alias

</td><td>

Alias record associated with this connection. For example, enter `sn_saba_spoke.Saba`

</td></tr><tr><td>

URL builder

</td><td>

**Note:** Do not select the check box.

</td></tr><tr><td>

Connection URL

</td><td>

URL of the Saba instance.

</td></tr><tr><td>

Use MID server

</td><td>

This field isn't applicable.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the connection. Select the option.

</td></tr><tr><td>

Domain

</td><td>

Domain that the action or activity runs in.

</td></tr></tbody>
</table>5.  Click **Submit**.


## Create credential record for the Saba spoke

Authorize the Saba spoke actions by creating credential records for the application registered in Saba. The Saba spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

3.  Select OAuth 2.0 Credentials.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, Saba.|
    |Active|Option to actively use the credential record. Select the option.|
    |OAuth Entity Profile|Default OAuth entity profile of the Saba spoke.|
    |Order|Order that the credentials are used. For example, enter `100`.|

5.  Right-click the form header and click **Save**.


## Create basic Auth credentials for the Saba spoke

Integrate the ServiceNow instance and Saba instance by using the basic Auth credentials to authenticate ServiceNow requests.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

3.  Select Basic Auth Credentials.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, Saba.|
    |User name|User name to be entered as credential.|
    |Password|Password to be entered as credential.|
    |Active|Option to actively use the credential record. Select the option.|
    |Order|Order that the credentials are used. For example, enter `100`.|

5.  Right-click the form header and click **Save**.


## Provide Saba user credentials

Create a record to provide details and credentials of the required Saba user. The Saba spoke uses these user credentials to perform actions in Saba.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **Saba** &gt; **Credentials**.

2.  Click **New**.

3.  On the form, fill these values.

    |Field|Descriptions|
    |-----|------------|
    |Credential|Reference to the Saba integration user credential record.|
    |Connection &amp; Credential Alias|Default alias record associated with the Saba spoke.|
    |Refresh Token Expires|Date and time by when the Saba refresh token expires. Once the Get Saba Token flow is activated, the Saba spoke generates a new token periodically, before the current refresh token expires.|

4.  Click **Submit**.

5.  To generate the Saba token, click the **Get Saba Token** related link.


