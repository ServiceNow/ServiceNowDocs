---
title: View the LDAP monitor
description: You can view current information about LDAP servers and listeners using LDAP monitor.
locale: en-US
release: australia
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [LDAP integration troubleshooting, LDAP integration, Authentication, Access Management]
---

# View the LDAP monitor

You can view current information about LDAP servers and listeners using LDAP monitor.

## Before you begin

Role required: admin

## About this task

The available states are:

-   Active
-   Inactive
-   Error
-   Active \(Shutting down...\)
-   Error \(Shutting down...\)

In addition to its current state, the monitor also shows:

-   The last message detected by the listener, such as waiting for LDAP changes, error connecting, and so forth.
-   The last LDAP user change, such as new user, updated user, and so forth.
-   The last error that occurred.

To view LDAP monitor:

## Procedure

1.  Navigate to **All** &gt; **LDAP** &gt; **System LDAP** &gt; **LDAP Monitor**.

    ![LDAP monitor](../image/LDAPMonitor.png)

    See the table for descriptions of the properties and fields in the screen.

<table id="table_ojk_xvt_xp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Refresh

</td><td>

You can configure the refresh rate by clicking the **Refresh** field in the LDAP Server Monitor header bar, and selecting the number of seconds between each data refresh. You can also select **None** to suppress refreshing.

</td></tr><tr><td>

Connection Status

</td><td>

The server connection indicator is located on the right side, above the LDAP Listener Status fields. When the server is connected, the box is green and shows Connected. When the server is not connected, the box is red and shows Not Connected. When the server connection is being tested, the box is yellow and shows Testing Connection.

</td></tr><tr><td class="sub-head" colspan="2">

LDAP Server Properties

</td></tr><tr><td>

Edit

</td><td>

As you monitor LDAP servers, you can [make changes to the properties](t_DefineAnLDAPServer.md) by clicking **Edit** in the LDAP Server Monitor screen.

</td></tr><tr><td>

Server URL

</td><td>

The combination of the server name and server port where the LDAP Server is listening. Frequently, the port is set to one of the following: -   389: the default port for connecting to LDAP in clear text
-   636: the standard port for connecting to LDAP via an SSL connection
 Example value: ldap://10.10.10.3:389/

 Your LDAP Server may have more than one URL address. This does NOT establish multiple directory structures from which you can import data, which is done by creating another LDAP Server entry, but does provide for redundancy when you have multiple LDAP Servers to avoid a single point of failure. The LDAP URL addresses are separated with a space character, and the system automatically tries each server address in turn until a valid connection can be made.

</td></tr><tr><td>

Starting search directory

</td><td>

The starting directory or RDN \(Relative Distinguished Name\) where the system begins searching for users or groups. Example value: DC=service-now,DC=com

 No data ABOVE this point is available for import. The instance has visibility into the specified directory and directories BELOW it in the LDAP hierarchy.

</td></tr><tr><td>

MID Server Status

</td><td>

The current connection status of the MID Server.

</td></tr><tr><td class="sub-head" colspan="2">

LDAP Listener Status

</td></tr><tr><td>

Current Status

</td><td>

This indicates whether the listener is active.

</td></tr><tr><td>

Last Info Message

</td><td>

This shows the last message the LDAP server received relating to user and group changes, and the time the message was received.

</td></tr><tr><td>

Last Change

</td><td>

This shows the last change made to the LDAP server, and the time it was made.

</td></tr><tr><td>

Last Error

</td><td>

This shows the last error that occurred on to the LDAP server, and the time it occurred.

</td></tr></tbody>
</table>
