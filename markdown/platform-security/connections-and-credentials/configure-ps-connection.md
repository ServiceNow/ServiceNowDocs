---
title: Create a basic connection for PowerShell and SSH
description: Configure connection information to use with a custom activity or action that uses the PowerShell or Secure Shell \(SSH\) protocol.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Get started with connections, Connections and Credentials, Access Management]
---

# Create a basic connection for PowerShell and SSH

Configure connection information to use with a custom activity or action that uses the PowerShell or Secure Shell \(SSH\) protocol.

## Before you begin

Role required: admin or connection\_admin

## Procedure

1.  Navigate to **All** &gt; **Credentials &amp; Connections** &gt; **Connections**.

2.  Click **New**.

3.  Select **Basic Connection for PowerShell &amp; SSH**.

4.  Complete the form.

<table id="table_wdx_hph_gdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the connection record.

</td></tr><tr><td>

Credential

</td><td>

Select the credential record used to authorize the connection.

</td></tr><tr><td>

Connection alias

</td><td>

Select the alias record to associate with this connection. Using an alias enables you to update the connection record without having to reconfigure any actions or activities that use the alias.

</td></tr><tr><td>

Host

</td><td>

Fully qualified domain name of the target host where the system runs the activity or action. For example, host.domain.com.

</td></tr><tr><td>

Active

</td><td>

Select to make this connection active.

</td></tr><tr><td>

Domain

</td><td>

Determines the domain the activity runs in. Flow Designer does not support domain separation and ignores this field.

</td></tr><tr><td>

Override default port

</td><td>

Target port used by the connection. If you leave this field blank, the system uses the default port value.

</td></tr><tr><td>

Use MID Server

</td><td>

Select to connect to the target host through a MID Server. If selected, define fields in the Advanced MID Server Configuration section. **Note:** PowerShell requires a MID Server.

</td></tr><tr><td>

MID Selection

</td><td>

Option to select a specific MID Server or MID Cluster. Choose any one of the following options. -   **Auto-Select MID Server**: Your ServiceNow instance selects the MID Server without manual input.
-   **Specific MID Server**: Your ServiceNow instance uses MID Server that you specify.
-   **Specific MID Cluster**: Your ServiceNow instance uses the MID Cluster that you specify.

A MID Cluster is a group of MID Servers that enables your ServiceNow instance to handle multiple integrations, and improve integration speed. For more information, see [Configure a MID Server cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_ConfigureAMIDServerCluster.md).

 This field is available when **Use MID Server** is checked. **Note:** Ensure that the Integration Hub connection record is referred, not an Orchestration connection record.

</td></tr><tr><td>

Capabilities

</td><td>

The capabilities the MID Server must support to be eligible for selection. The system runs the action or activity from a MID Server that supports the selected capabilities. Only displays if **Use MID server** is selected.

 Required capabilities determine which MID Server is selected at runtime. To learn more about how a MID Server is selected during runtime, see [MID Server selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/c_MIDServerSelector.md). This field is visible only when **Auto-Select MID Server** is selected from the MID Selection list.

</td></tr><tr><td>

MID Application

</td><td>

The application the MID Server must support to be eligible for selection. The system runs the action from a MID Server that supports the selected application. Only displays if **Use MID server** is selected.

 To learn more about how a MID Server is selected during runtime, see [MID Server selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/c_MIDServerSelector.md).

</td></tr><tr><td>

MID Server

</td><td>

Specific MID Server on which the step runs. This field is visible only when **Specific MID Server** is selected from the MID Selection list.

</td></tr><tr><td>

MID Cluster

</td><td>

The specific MID Cluster you want to use. This field is available when **Use MID Server** is checked, and **Specific MID Cluster** is selected from the MID Selection list.

</td></tr></tbody>
</table>5.  Click **Submit**.


**Parent Topic:**[Get started with connections](../reference/connection-information.md)

