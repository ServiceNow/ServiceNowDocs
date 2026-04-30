---
title: Create connection and credential for Zoom
description: Setup connection and credentials alias for Zoom.
locale: en-US
release: yokohama
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Connect Workplace Reservation Management with Zoom, Configure, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Create connection and credential for Zoom

Setup connection and credentials alias for Zoom.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message, `What type of Credentials would you like to create?`

3.  Select **OAuth 2.0 Credentials**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record.|
    |Active|Option to actively use the credential record.|
    |OAuth Entity Profile|OAuth profile created in the application registration of the provider. For example, Zoom default\_profile|
    |Applies to|MID Servers that can use this credential. For example, select **All MID Servers**.|
    |Order|Order that the credentials are used. For example, enter `100`.|

5.  **Save** the form.

    Right-click the form header and click **Save**.

6.  To generate the OAuth token, click the **Get OAuth Token** related link.

7.  Create a connection

    1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection**.

    2.  Click **New**.

    3.  On the form, fill in the fields.

<table id="table_ns5_4tf_15b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, `Zoom Connection`.

</td></tr><tr><td>

Credential

</td><td>

Credential record created for this connection.

</td></tr><tr><td>

Connection alias

</td><td>

Alias record associated with this connection. Select `sn_zoom_spoke.Zoom` Connection &amp; credential alias record.

</td></tr><tr><td>

URL builder

</td><td>

**Note:** Do not select the check box.

</td></tr><tr><td>

Connection URL

</td><td>

Connection URL. Enter `https://api.zoom.us`.

</td></tr><tr><td>

Use MID server

</td><td>

Option to use a MID Server. If the check box is selected, define the fields in the Advanced MID Server Configuration related list.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the connection.

</td></tr><tr><td>

Domain

</td><td>

Domain that the action or activity runs in.

</td></tr></tbody>
</table>    4.  Click **Submit**.


**Parent Topic:**[Connect Workplace Reservation Management with Zoom](connect-rsv-mtm-with-zoom.md)

**Previous topic:**[Setup OAuth connectivity between ServiceNow and Zoom](setup-connectivity-between-servicenow-and-zoom.md)

**Next topic:**[Display permanent seat assignments on floor maps](display-permanent-seats-on-maps.md)

