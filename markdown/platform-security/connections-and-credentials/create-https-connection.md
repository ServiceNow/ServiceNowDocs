---
title: Create an HTTP\(s\) connection
description: The HTTP\(s\) connection provides the information custom HTTP\(s\) actions or activities use to connect.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Get started with connections, Connections and Credentials, Access Management]
---

# Create an HTTP\(s\) connection

The HTTP\(s\) connection provides the information custom HTTP\(s\) actions or activities use to connect.

## Before you begin

Role required: connection\_admin

## Procedure

1.  Navigate to **All** &gt; **Credentials &amp; Connections** &gt; **Connections**, click **New**, and select **HTTP\(s\) Connection**.

2.  Add the following connection information and click **Submit**:

<table id="table_cpw_z5c_zpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of this HTTP\(s\) connection.

</td></tr><tr><td>

Credential

</td><td>

Select the credential record used to authorize the connection.

</td></tr><tr><td>

Connection Alias

</td><td>

Select the alias record to associate with this connection. Using an alias enables you to update the connection record without having to reconfigure any actions or activities that use the alias.

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

Active

</td><td>

Check the box to make this connection active.

</td></tr><tr><td>

Domain

</td><td>

Determine the domain the action or activity runs in.

</td></tr><tr><td>

Use MID Server

</td><td>

Check to use a MID Server for this action or activity. If selected, define fields in the Advanced MID Server Configuration section.

</td></tr><tr><td>

MID Selection

</td><td>

Option to select a specific MID Server or MID Cluster. Choose any one of the following options. -   **Auto-Select MID Server**: Your ServiceNow instance selects the MID Server without manual input.
-   **Specific MID Server**: Your ServiceNow instance uses MID Server that you specify.
-   **Specific MID Cluster**: Your ServiceNow instance uses the MID Cluster that you specify.

A MID Cluster is a group of MID Servers that enables your ServiceNow instance to handle multiple integrations, and improve integration speed. For more information, see Configure a MID Server cluster.

 This field is available when **Use MID Server** is checked. **Note:** Ensure that the Integration Hub connection record is referred, not an Orchestration connection record.

</td></tr><tr><td>

Capabilities

</td><td>

The capabilities the MID Server must support to be eligible for selection. The system runs the action or activity from a MID Server that supports the selected capabilities. Only displays if **Use MID server** is selected. Required capabilities determine which MID Server is selected at runtime. To learn more about how a MID Server is selected during runtime, see MID Server selection. This field is visible only when **Auto-Select MID Server** is selected from the MID Selection list.

</td></tr><tr><td>

MID Application

</td><td>

The application the MID Server must support to be eligible for selection. The system runs the action from a MID Server that supports the selected application. Only displays if **Use MID server** is selected. To learn more about how a MID Server is selected during runtime, see MID Server selection.

</td></tr><tr><td>

MID Server

</td><td>

Specific MID Server on which the step runs. This field is visible only when **Specific MID Server** is selected from the MID Selection list.

</td></tr><tr><td>

MID Cluster

</td><td>

The specific MID Cluster you want to use. This field is available when **Use MID Server** is checked, and **Specific MID Cluster** is selected from the MID Selection list.

</td></tr><tr><td>

Connection Timeout

</td><td>

Number of milliseconds the system waits for a successful host connection. If a successful connection does not occur during this time, the connection request times out. Leave this field empty to use the system default connection timeout value.**Note:** Avoid setting the **Connection Timeout** value to zero, as this may cause a stale connection.

</td></tr><tr><td>

additional\_http\_headers \(Attributes tab\)

</td><td>

Include any additional headers required, such as sap-client=100. If adding multiple headers, separate them with a semi-colon.

</td></tr><tr><td>

odata\_ping\_url \(Attributes tab\)

</td><td>

The default OData ping URL is /sap/bc/ping. To edit the ping URL for OData heartbeat, select the lock icon, edit the URL, and select the lock icon again.

</td></tr></tbody>
</table>3.  Click **Submit**.

    You are ready to create a custom HTTP\(s\) action or activity.


**Parent Topic:**[Get started with connections](../reference/connection-information.md)

