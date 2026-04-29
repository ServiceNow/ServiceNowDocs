---
title: Create connection records for the Microsoft Exchange Online spoke
description: Perform actions in Microsoft Exchange Online by creating connection records for your Microsoft Exchange Online account. The Microsoft Exchange Online spoke connection and credential alias uses these connections to perform actions.
locale: en-US
release: australia
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up Microsoft Office 365 integration for Walk-up Experience, Integrate Microsoft Office 365 calendar with Walk-up Experience, Configure, Walk-up Experience, IT Service Management]
---

# Create connection records for the Microsoft Exchange Online spoke

Perform actions in Microsoft Exchange Online by creating connection records for your Microsoft Exchange Online account. The Microsoft Exchange Online spoke connection and credential alias uses these connections to perform actions.

## Before you begin

Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the record, **Microsoft\_Exchange\_Online**.

3.  In the Connections related list, click **New**.

4.  On the form, fill in the fields.

<table id="table_c4p_lzg_2hb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, `Exchange_Online_Connection`.

</td></tr><tr><td>

Credential

</td><td>

Credential record created for Microsoft Exchange Online. For example, `Exchange_Online_Credentials`.

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

Connection URL. Enter `https://graph.microsoft.com`.

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
</table>5.  Click **Update**.

6.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

7.  Open the record, **Microsoft\_Exchange\_Online\_clientCred**.

8.  In the Connections related list, click **New**.

9.  On the form, fill in the fields.

<table id="table_vjd_1md_qnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, `Exchange_Online_Connection_clientCred`.

</td></tr><tr><td>

Credential

</td><td>

Credential record created for Microsoft Exchange Online. For example, `Exchange_Online_Credentials_clientCred`.

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

Connection URL. Enter `https://graph.microsoft.com`.

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
</table>10. Click **Update**.


## Result

The Microsoft Exchange Online spoke is set up and integrated with the Walk-up Experience instance.

**Parent Topic:**[Set up Microsoft Office 365 integration for Walk-up Experience](setup-walkup-msoffice365-cal-integ.md)

