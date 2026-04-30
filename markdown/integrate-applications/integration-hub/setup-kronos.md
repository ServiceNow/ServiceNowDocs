---
title: Set up the UKG spoke
description: Integrate your Kronos application with your ServiceNow instance. Register an OAuth application in Kronos and authenticate requests from ServiceNow.Add and configure a connection using the connection template to authenticate ServiceNow requests in UKG spoke.Create a connection record and credential record for setting up the UKG spoke.Use the information generated during the Kronos application creation and configuration to register Kronos as an OAuth provider and allow the instance to request OAuth 2.0 tokens.Authorize the Kronos spoke actions by creating credential records for the application registered in Kronos. The Kronos spoke connection and credential alias uses these credentials to authorize actions.Create a record to provide details and credentials of the required Kronos user. The Kronos spoke uses these user credentials to perform actions in Kronos.Create Connection records to your Kronos application. The Kronos spoke connection and credential alias uses these connections to perform actions in Kronos.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [UKG Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the UKG spoke

Integrate your Kronos application with your ServiceNow instance. Register an OAuth application in Kronos and authenticate requests from ServiceNow.

## Before you begin

-   Request Integration Hub subscription
-   Activate the UKG spoke
-   Kronos manager user or superuser credentials
-   Role required: admin

**Note:** Make sure that the application registry, connections, and credentials are within the application scope.

You can choose to set up the UKG spoke using the connection template or using connection and credentials records according to your requirement.

## Option 1: Configure a connection for the UKG spoke

Add and configure a connection using the connection template to authenticate ServiceNow requests in UKG spoke.

### Before you begin

Role required: admin

**Note:** If you're updating from a previous version \(before version 3.3.0\) of the spoke, first you need to remove the current connection record, credentials record, and Kronos user credentials. Then, you can set up the connection using the template.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select the **Connections** tab.

3.  Locate the **UKG connection** alias and click **View Details**.

    **Note:** Don't click **Add Connection**.

    ![Connection template for UKG spoke.](../image/ukg-spoke-conn-template.png)

4.  Click **Edit**.

    If you are configuring the spoke for the first time, click **Configure**.![Configure a connection for the UKG spoke](../image/ukg-spoke-config-conn.png)

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to uniquely identify the connection record. For example, enter Kronos Conn.|
    |Connection URL|URL of the Kronos instance.|
    |App Key|Application key of the Kronos instance.|
    |OAuth Entity Name|Unique name to identify the OAuth entity profile of the UKG spoke. For example, select `UKG OAuth entity`.|
    |OAuth Client ID|Client ID created during the application configuration in Kronos.|
    |OAuth Client Secret|Client Secret created during the application configuration in Kronos.|
    |Token URL|OAuth server token endpoint. For example, `https://<Kronos-Instance>.com/api/authentication/access_token`.|

6.  Click **Configure and Get OAuth Token**.

    A modal page displays to enter your Kronos credentials.

7.  Enter your Kronos username and password and click **Get OAuth Token**.


### Result

Once your OAuth token has been successfully fetched, you can begin using your UKG spoke connection.

## Option 2: Using connection and credentials records for UKG spoke setup

Create a connection record and credential record for setting up the UKG spoke.

### Before you begin

Role required: admin

**Note:** If you have already configured a connection using the connection template, you can ignore this procedure.

### Register Kronos as an OAuth provider

Use the information generated during the Kronos application creation and configuration to register Kronos as an OAuth provider and allow the instance to request OAuth 2.0 tokens.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Open the record for the Kronosspoke.

3.  On the form, fill in the fields.

    |Field|Value required|
    |-----|--------------|
    |Name|Name to uniquely identify the record. For example, enter `Kronos OAuth profile`.|
    |Client ID|Client ID created during the application configuration in Kronos.|
    |Client Secret|Client Secret created during the application configuration in Kronos.|
    |Default Grant type|Grant type used to establish the token. Select **Resource Owner Password Credentials**.|
    |Application|Application scope that contains this record. Select **Kronos Spoke**.|
    |Accessible from|Application scope that this registry is accessible from.|
    |Active|Option to actively use the application registry. Select the option.|
    |Token URL|OAuth server token endpoint. For example, `https://<Kronos-Instance>.com/api/authentication/access_token` .|
    |Redirect URL|OAuth callback endpoint. For example, `https://<ServiceNow-Instance>.com/oauth_redirect.do`.|

4.  Right-click the form header, and click **Save**.

5.  In the **OAuth Entity Scopes** tab, insert a row and provide these values.

    |Field|Value|
    |-----|-----|
    |Name|Kronos|
    |OAuth scope|givenName mail nonce openid profile sn uid|

6.  Click **Update**.

7.  In the **OAuth Entity Profile** tab, click the default profile, **Kronos oAuth default\_profile**.

8.  Insert a record in the OAuth Entity Scope related list and select the default entity scope for the Kronos spoke, for example, `Kronos`.

9.  Click **Update**.


### Create Credential record for the Kronos spoke

Authorize the Kronos spoke actions by creating credential records for the application registered in Kronos. The Kronos spoke connection and credential alias uses these credentials to authorize actions.

#### Before you begin

Role required: admin.

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message `What type of Credentials would you like to create?`.

3.  Select **OAuth 2.0 Credentials**.

4.  On the form, fill in the fields.

    |Field|Value required|
    |-----|--------------|
    |Name|Name to uniquely identify the record. For example, `Kronos Cred`.|
    |Active|Option to actively use the credential record. Select the option.|
    |OAuth Entity Profile|Default OAuth entity profile of the Kronos spoke. For example, select **Kronos oAuth default\_profile**.|
    |Order|Order that the credentials are used. For example, enter `100`.|

5.  Right-click the form header and click **Save**.


### Provide Kronos user credentials

Create a record to provide details and credentials of the required Kronos user. The Kronos spoke uses these user credentials to perform actions in Kronos.

#### Before you begin

Role required: admin.

#### About this task

Ensure that you provide credentials of a manager user or Kronos superuser. With these credentials, time off requests of both employee and manager can be managed.

#### Procedure

1.  Navigate to **All** &gt; **Kronos** &gt; **Credentials**.

2.  Click **New**.

3.  On the form, fill these values.

    |Field|Descriptions|
    |-----|------------|
    |Name|Name to uniquely identify the record.|
    |Application Key|Application Key of the Kronos user.|
    |User name|User name to log in to the user's account in Kronos.|
    |Password|Password of the Kronos user account.|
    |Connection &amp; Credential Alias|Default alias record associated with the Kronos spoke.|
    |Refresh Token Expires|Date and time by when the Kronos refresh token expires. The Kronos spoke generates a new refresh token periodically, before the current refresh token expires.|

4.  Click **Submit**.

5.  To generate the Kronos token, click the **Get Kronos Token** related link.


#### Result

The Kronos - Get Kronos Token subflow is triggered. The subflow uses the details provided during spoke setup to retrieve a valid refresh token from Kronos. The subflow then, updates the value of **Refresh Token Expires**.

**Note:** To access more details about the Kronos refresh token, navigate to **System OAuth** &gt; **Manage Tokens.**. Here, a record is created for each refresh token.

### Create Connection record for the Kronos spoke

Create Connection records to your Kronos application. The Kronos spoke connection and credential alias uses these connections to perform actions in Kronos.

#### Before you begin

Role required: admin.

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the record for the Kronos spoke.

3.  From the **Connections** tab, click **New**.

4.  On the form, fill these values.

<table id="table_any_shp_gfb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the connection record. For example, enter `Kronos Conn`.

</td></tr><tr><td>

Credential

</td><td>

Credential record you created for Kronos. For example, select **Kronos Cred**. See [Create Credential record for the Kronos spoke](setup-kronos.md#) for more information.

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

URL of the Kronos instance.

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
</table>5.  In the **Attributes** tab, fill these values.

    |Field|Description|
    |-----|-----------|
    |u\_app\_key|Application Key of the Kronos user.|
    |u\_version|Kronos version of your instance. Enter `v1`.|

6.  Click **Submit**.


