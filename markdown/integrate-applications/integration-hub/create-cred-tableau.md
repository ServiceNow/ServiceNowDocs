---
title: Create a connection and credential for the Tableau spoke
description: Create a connection and credential record for the Tableau Cloud application. The Tableau connection and credential alias uses these credentials to authorize actions.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Tableau spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Create a connection and credential for the Tableau spoke

Create a connection and credential record for the Tableau Cloud application. The Tableau connection and credential alias uses these credentials to authorize actions.

## Before you begin

Role required: ServiceNow admin or Tableau Cloud Site administrator

Register your Tableau Cloud application.

-   If you’re using the Personal Access Token \(PAT\) authentication type, record the Personal Access Token Secret.
-   If you’re using the JSON Web Token \(JWT\) authentication type, record the Client ID and Client Secret.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Select the **TableauCloud** record.

    The Connection &amp; Credential Aliases page opens.

3.  Under the Related Links section, select **Create New Connection &amp; Credential**.

4.  In the dialog box, fill in the fields.

<table id="table_jq1_xry_bbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr class="sub-head"><td colspan="2">

Please Enter the Connection Information

</td></tr><tr><td>

Connection Name

</td><td>

Name of the connection. This field is automatically set to `Tableau Cloud Connection`.

</td></tr><tr><td>

Connection URL

</td><td>

The URL used for connecting to the server on which Tableau Cloud is installed.

</td></tr><tr><td>

Content URL

</td><td>

The permanent name of the site to sign in to. The content URL appears in the URL path of Tableau content in your browser address bar after the Tableau Server URL. mySite is the content URL in the following example: `http://<server or cloud URL>/#/site/mySite/explore`.

</td></tr><tr class="sub-head"><td colspan="2">

Please Enter the Credential InformationSelect the PAT or JWT authentication type. The fields change based on the authentication type that you select.

</td></tr><tr class="sub-head"><td colspan="2">

Fields for the PAT authentication type

</td></tr><tr><td>

Token Name

</td><td>

The Token name that you provided while setting up the Tableau spoke by using the PAT authentication type.For more information, see [Set up the Tableau spoke](set-up-tableau-spoke.md)

</td></tr><tr><td>

Token Secret

</td><td>

The Token secret that you copied while setting up the Tableau spoke by using the PAT authentication type.For more information, see [Set up the Tableau spoke](set-up-tableau-spoke.md).

.

</td></tr><tr><td>

Expiry Interval \(sec\)

</td><td>

Life span of the generated Personal Access Token \(PAT\).Default value: 14400 sec

**Important:** You mustn't modify the value of this field.

</td></tr><tr class="sub-head"><td colspan="2">

Fields for the JWT authentication type

</td></tr><tr><td>

Secret ID

</td><td>

The Secret ID that you copied while setting up the Tableau spoke by using the JWT authentication type.For more information, see [Set up the Tableau spoke](set-up-tableau-spoke.md).

</td></tr><tr><td>

Secret Value

</td><td>

The Secret Value that you copied while setting up the Tableau spoke by using the JWT authentication type.For more information, see [Set up the Tableau spoke](set-up-tableau-spoke.md).

</td></tr><tr><td>

Username

</td><td>

User name, that is, the email address of the authenticated Tableau Cloud user.

</td></tr><tr><td>

Client ID

</td><td>

The Client ID that you copied while setting up the Tableau spoke by using the JWT authentication type.For more information, see [Set up the Tableau spoke](set-up-tableau-spoke.md).

</td></tr><tr><td>

Expiry Interval \(sec\)

</td><td>

Life span of the generated JSON Web Token \(JWT\).Default value: 3600 sec

**Important:** You mustn't modify the value of this field.

</td></tr></tbody>
</table>5.  Select **Create and Get OAuth Token**.


## Result

A connection and credential record is created in the ServiceNow instance.

