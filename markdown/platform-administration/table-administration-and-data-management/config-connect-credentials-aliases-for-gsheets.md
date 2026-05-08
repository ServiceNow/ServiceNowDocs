---
title: Configure ServiceNow connection and credential aliases for Google sheets
description: Configure connection and credential aliases to authenticate an integration between your ServiceNow instance and Google Drive.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Exporting your table records to Google Sheets, Exporting data, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure ServiceNow connection and credential aliases for Google sheets

Configure connection and credential aliases to authenticate an integration between your ServiceNow instance and Google Drive.

## Before you begin

Role required: admin

## About this task

The connection and credential aliases record is used to manage the secure connection of your ServiceNow instance with Google Sheets. A connection alias tells the system how to connect to Google Sheets. It defines the endpoint URL of the Google Drive API and tells the system who is connecting. For example, it stores the authentication details, such as the OAuth token and API keys.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    1.  Select **New**.

    2.  On the form, fill in the fields.

<table id="table_xch_c2v_hfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the alias. An alias can only contain alphanumeric characters and underscores. For example, Sheets\_Alias.During an upgrade, the tag in the credential record migrates to a Connection &amp; Credential alias. If the credential tag contains special characters other than alphanumeric characters and underscores, it preserves the tag name after the upgrade. You can still use this migrated alias, but you can't update the alias until you change the name to meet the naming restrictions.

</td></tr><tr><td>

ID

</td><td>

Unique identifier for the Connections &amp; Credentials alias, based on the format `scope_name.alias_name`. -   If the scope is Global, the ID is the alias name. For example, if you create a Sheets alias in the global scope, it sets the ID to `sheets`.
-   If you create a workday alias in the HR app scope, it sets the ID to `x_hr_app.sheets`.


</td></tr><tr><td>

Parent Alias

</td><td>

Connection and credential alias record of the Google Drive.

</td></tr><tr><td>

Type

</td><td>

Type that is either Credential or Connection and Credential. The default is Connection and Credential.

</td></tr><tr><td>

Connection type

</td><td>

Name of the connection type, either Basic, HTTP, JDBC, JMS, or Kafka. The default is HTTP.

</td></tr><tr><td>

Support Multiple Active Connections

</td><td>

Option that indicates whether the alias supports multiple active connections. You can add connections by using the Connections \[sys\_connection\] table. You can associate the connections to the alias by using the Connections related list.

</td></tr><tr><td>

Default Retry Policy

</td><td>

Retry policy for the alias. For more information, see Retry policy.

</td></tr><tr><td>

Configuration Template

</td><td>

Configuration template to use to create a connection and credential record.

</td></tr></tbody>
</table>    3.  Select **Submit**.

    A connection and credential alias record is created.

2.  Create an OAuth 2.0 credential to use in the connection and credential alias record.

    1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

    2.  Select **New**.

    3.  From the list of credential types, select **OAuth 2.0 Credentials**.

    4.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Unique name of the credential to differentiate it from the default credentials that are provided by the application. For example, Sheet credentials.|
        |Active|Option to activate the credential.|
        |OAuth Entity Profile|Default OAuth entity profile that was generated when you performed the application registry in [Create an application registry for Google Sheets on a ServiceNow instance](configure-app-registry-gsheets.md).|
        |Applies to|Option to specify if the credential record is applicable for all MID Servers, or a specific MID Server. If specific, add the MID Servers as necessary.|
        |Order|Order \(sequence\) in which Discovery tries this credential as it attempts to log on to devices. The smaller the number means that the higher in the list this credential appears.|

    5.  Select **Submit**.

        The OAuth 2.0 credential record is created.

    6.  Open the OAuth 2.0 credential record from the Credentials list.

    7.  From the Integration Type list, select **Personal**.

3.  Create a connection record for your alias.

    1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections**.

    2.  Select **New**.

    3.  From the list of connection types, select **HTTP\(s\) Connection**.

    4.  On the form, fill in the fields.

<table id="table_ltf_rt5_hfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the connection. This field must be unique on the table.For example, Sheets credentials.

</td></tr><tr><td>

Credential

</td><td>

Credential to use with this connection.For example, select the OAuth 2.0 credential record created in step 2.

</td></tr><tr><td>

Connection alias

</td><td>

Connection alias that resolves your connection and credentials at run time. Only one connection is active per connection alias at any one time.

</td></tr><tr><td>

Active

</td><td>

Option to make this connection active.

</td></tr><tr><td>

Domain

</td><td>

Domain that the action or activity runs in.

</td></tr><tr><td>

URL builder

</td><td>

Option to use the system to build a URL that is based on the inputs, such as host, port, and base path.

</td></tr><tr><td>

Connection URL

</td><td>

URL that the MID Server uses to connect to the specified weblink. If URL builder is not selected, enter the connection URL in this field. For example,`https://www.googleapis.com/upload/drive/v3/files?uploadType=multipart&fields=id`.

</td></tr><tr><td>

Mutual authentication

</td><td>

Option to enable authentication by using a protocol profile.**Note:** If the mutual authentication is selected, a connection URL is built: Protocol + :// + host:port +URL. If a mutual authentication isn’t selected, a connection URL is built: Protocol profile + :// + host:port +URL.

This field appears only when **URL builder** is selected.

</td></tr><tr><td>

Use MID server

</td><td>

Option to define the fields in the Advanced MID Server Configuration section.If a successful connection doesn’t occur during this time, the connection request times out. Leave this field empty to use the system default connection timeout value.

**Note:** Avoid setting the **Connection Timeout** value to zero, because doing so may cause a stale connection.

</td></tr><tr><td>

Connection timeout

</td><td>

Number of seconds that the system waits for a successful host connection.

</td></tr></tbody>
</table>    5.  Select **Submit**.

    The connection record is created.

4.  Copy the sys\_id of the alias record.

    **Note:** This sys\_id is required when setting up the **export to sheets alias** system property.

    1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    2.  From the Connection and Credentials Aliases list, select and open the alias that you created in step 1.

    3.  Right-click the header of the alias page and select **Copy sys\_id**.

5.  Configure the **export to sheets alias** system property.

    1.  In the navigation filter, enter `sys_properties.list`

        The entire list of properties in the System Properties \[sys\_properties\] table appears.

    2.  Select **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the property that you’re creating. In this case, `glide.oauth.export.to.sheets.alias`.|
        |Description|Brief, descriptive phrase that describes the function of the property.|
        |Type|Data type. In this case, `string`.|
        |Value|Value for the property. In this case, paste the sys\_id that you copied from the alias record in step 4.|

    4.  Select **Submit.**

        **Note:** If the **Ignore cache** check box is selected, the system flushes the server cache when the parameter is changed.


## Result

The connection and credential alias record is configured to connect your ServiceNow instance with Google Sheets.

**Parent Topic:**[Exporting your table records to Google Sheets](../concept/setup-gsheet-export.md)

