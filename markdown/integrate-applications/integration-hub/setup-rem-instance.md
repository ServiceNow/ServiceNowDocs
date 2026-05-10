---
title: Set up the ServiceNow Remote Instance spoke
description: Integrate the local and remote ServiceNow instances by creating an OAuth API endpoint in the remote ServiceNow instance to authenticate requests.Register remote ServiceNow instance as an OAuth provider so that the local ServiceNow instance can request OAuth 2.0 tokens.Create credential record for the remote ServiceNow instance. The ServiceNow Remote Instance spoke connection and credential alias uses these credentials to authorize actions.Create Connection record for your remote ServiceNow instance. The ServiceNow Remote Instance spoke connection and credential aliases use these connections to perform actions.Create credential record for the local ServiceNow instance. The ServiceNow Remote Instance spoke connection and credential alias uses these credentials to authorize actions.Create Connection record for your local ServiceNow instance. The ServiceNow Remote Instance spoke connection and credential aliases use these connections to perform actions.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [ServiceNow Remote Instance Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the ServiceNow Remote Instance spoke

Integrate the local and remote ServiceNow instances by creating an OAuth API endpoint in the remote ServiceNow instance to authenticate requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the ServiceNow Remote Instance spoke in remote and local ServiceNow instances.

    **Note:** The terms remote instance and local instance are used in these contexts:

    -   Local instance: This is the ServiceNow instance from which the communication is initiated and established.
    -   Remote instance: This is the ServiceNow instance with which the local instance communicates.
-   Role required: admin.

    **Note:** Admin role is required to only set up the spoke.

    To use the spoke, ensure that the spoke users have only the required minimum permissions to access data in ServiceNow tables. Do not assign elevated privilege roles to users of this spoke unless very much required. This practice ensures controlled access to data.

    The integration users must have the flow\_operator and other required roles to access the table they want to interact with. Also, they need roles to access the Table \[sys\_db\_object\] and Dictionary Entry \[sys\_dictionary\] tables to show dynamic options such as, table names and fields in a table.


## Register remote ServiceNow instance as an OAuth provider

Register remote ServiceNow instance as an OAuth provider so that the local ServiceNow instance can request OAuth 2.0 tokens.

### Before you begin

-   In the remote ServiceNow instance:
    -   Create an OAuth API endpoint for external clients. In **Redirect URL**, specify the URL of the local ServiceNow instance in this format: `https://<instance-name>.service-now.com/oauth_redirect.do`. For more information, see [Create an endpoint for clients to access the instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/t_CreateEndpointforExternalClients.md).
    -   Copy and record the values of Client ID and Client Secret.
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Open for the record, **RemoteSpoke**.

3.  On the form, fill these values.

<table id="table_y54_gpz_qlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Client ID

</td><td>

Client ID created in the remote ServiceNow instance.

</td></tr><tr><td>

Client Secret

</td><td>

Client Secret created in the remote ServiceNow instance.

</td></tr><tr><td>

Authorization URL

</td><td>

URL of the remote ServiceNow instance in this format: `https://<instance-name>.service-now.com/oauth_auth.do`.

</td></tr><tr><td>

Token URL

</td><td>

URL of the remote ServiceNow instance in this format: `https://<instance-name>.service-now.com/oauth_token.do`.

</td></tr><tr><td>

Redirect URL

</td><td>

URL of the local ServiceNow instance in this format: `https://<instance-name>.service-now.com/oauth_redirect.do`.

</td></tr><tr><td>

Default Grant Type

</td><td>

Grant type used to establish the token. Select **Authorization Code**.

</td></tr><tr><td>

Refresh Token Lifespan

</td><td>

Time, in seconds, that the refresh token is valid. The default time is 8,640,0000 seconds.

</td></tr><tr><td>

PKCE required

</td><td>

Option to enable public clients to require PKCE for an authorization.**Note:** You can use only **Authorization Code** as the **Default Grant type** when **PKCE** is enabled.

</td></tr><tr><td>

Application

</td><td>

Application scope that contains this record.

</td></tr><tr><td>

Accessible from

</td><td>

Application scope that this registry is accessible from.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the application registry.

</td></tr></tbody>
</table>4.  Right-click the form header, and click **Save**.


## Create Credential record for the remote ServiceNow instance

Create credential record for the remote ServiceNow instance. The ServiceNow Remote Instance spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin.

**Note:** You must perform this task in a local ServiceNow instance.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message `What type of Credentials would you like to create?`.

3.  Select **OAuth 2.0 Credentials**.

4.  On the form, fill in the fields.

    |Field|Value required|
    |-----|--------------|
    |Name|Name to uniquely identify the record. For example, `Remote Credentials`.|
    |Active|Option to actively use the credential record.|
    |OAuth Entity Profile|OAuth profile created during the registration of the remote ServiceNow instance as an OAuth provider. For example, select **RemoteSpoke default\_profile**.|
    |Order|Order that the credentials are used. For example, enter `100`.|

5.  Right-click the form header and click **Submit**.

6.  To generate the OAuth token, click the **Get OAuth Token** related link.


## Create Connection record for the remote ServiceNow instance

Create Connection record for your remote ServiceNow instance. The ServiceNow Remote Instance spoke connection and credential aliases use these connections to perform actions.

### Before you begin

Role required: admin.

**Note:** You must perform this task in a local ServiceNow instance.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open the alias record, **ServiceNowRemoteInstance**.

3.  From the **Connections** tab, click **New**.

4.  On the form, fill in the fields.

<table id="table_any_shp_gfb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, `Remote Connection`.

</td></tr><tr><td>

Credential

</td><td>

Credential record created for remote ServiceNow instance. For example, **Remote Credentials**.

</td></tr><tr><td>

Connection alias

</td><td>

Alias record associated with this connection.

</td></tr><tr><td>

URL builder

</td><td>

**Note:** Do not select the check box.

</td></tr><tr><td>

Connection URL

</td><td>

URL of the remote ServiceNow instance. For example, `https://<remote-instance-name>.service-now.com/`.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the connection.

</td></tr><tr><td>

Domain

</td><td>

Domain that the action or activity runs in.

</td></tr></tbody>
</table>5.  Click **Submit**.


## Create Credential record for the local ServiceNow instance

Create credential record for the local ServiceNow instance. The ServiceNow Remote Instance spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin.

**Note:** You must perform this task in a local ServiceNow instance.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message `What type of Credentials would you like to create?`.

3.  Select **Basic Auth Credentials**.

4.  On the form, fill in the fields.

    |Field|Value required|
    |-----|--------------|
    |Name|Name to uniquely identify the record. For example, `Local Credentials`.|
    |Username|Username to log in to the local ServiceNow instance.|
    |Password|Password to log in to the local ServiceNow instance.|
    |Active|Option to actively use the credential record.|

5.  Right-click the form header and click **Submit**.


## Create Connection record for the local ServiceNow instance

Create Connection record for your local ServiceNow instance. The ServiceNow Remote Instance spoke connection and credential aliases use these connections to perform actions.

### Before you begin

Role required: admin.

**Note:** You must perform this task in a local ServiceNow instance.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open the alias record, **ServiceNowRemoteInstanceLocalAlias**.

3.  From the **Connections** tab, click **New**.

4.  On the form, fill in the fields.

    |Field|Value required|
    |-----|--------------|
    |Name|Name to uniquely identify the record. For example, `Local Connection`.|
    |Credential|Credential record created for local ServiceNow instance. For example, **Local Credentials**.|
    |Connection alias|Alias record associated with this connection.|
    |Connection URL|URL of the local ServiceNow instance. For example, `https://<local-instance-name>.service-now.com/`.|
    |Active|Option to actively use the connection.|
    |Domain|Domain that the action or activity runs in.|

5.  Click **Submit**.


