---
title: Configure the OT Discovery connections &amp; credentials
description: To configure the Service Graph Connector, set up the authentication credentials and configuration used to connect to the ServiceNow OT Discovery components.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Graph Connector for ServiceNow Operational Technology\(OT\) Discovery, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Configure the OT Discovery connections &amp; credentials

To configure the Service Graph Connector, set up the authentication credentials and configuration used to connect to the ServiceNow OT Discovery components.

## Before you begin

Role required: admin

**Note:** It's recommended that you switch the application scope to Service Graph Connector for ServiceNow OT Discovery.

## Procedure

1.  Verify that the application scope is set to **Service Graph Connector for OT Discovery** by using the application picker.

2.  Under **Configure the connection** section only configuring the MID Server is optional.

    **Note:** The MID Server is required when the Console cannot be reached from the internet. If the Console is reachable to the ServiceNow instance then MID Server is not needed.

3.  Download and install the MID Server on the host machine, test the connection, and then validate the MID Server.

    To configure the MID Server following the MID Server Guided Setup.

    The MID Server access is a secure proxy between the ServiceNow Instance and the Console, allowing ServiceNow to schedule jobs and make REST calls into the environment to pull various pieces of information such as Assets, installed software, and so on. Without the MID Server, ServiceNow cannot initiate direct communication if the Discovery Console is not reachable from the ServiceNow Instance

4.  Use the MID Server certificate check policies link to review the policies.

    **Note:** Enable/Disable the required security policies for the MID Server based on the network configuration.

5.  Next to the **Configure the OT Discovery Connection &amp; Credentials** task, select **Configure**.

    **Note:** Depending on your ServiceNow version, you're directed to Workflow Studio or the Workflow Studio Connections list. The Outbound connections are listed in alphabetical order.

6.  Navigate to or search for the OT Discovery Connections record.

7.  You can view and edit connections by selecting **View Details**.

    OT Discovery is the default connection.

8.  On the OT Discovery connection page, select **Configure**.

    The **Create Connection** window opens. To create a connection, select**Add Connection**.

9.  Fill in the following connection details as explained in the Connection details table.

    ![Create Connection](../images/connection-window.png)

<table id="table_utt_3fc_23c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Enter a unique name for the connection. The default connection has the name as "OT Discovery" and is read-only. For additional connections, enter a unique name for each.

This field is mandatory.

</td></tr><tr><td>

Connection URL

</td><td>

Navigate to the Console and copy its URL and paste it into the Connection URL field. For example: `https://OTDiscoveryConsole.net:8443/`

This field is mandatory.

</td></tr><tr><td>

Use MID Server

</td><td>

Optionally, check this box to use a MID Server for the connection.

</td></tr><tr><td>

MID Server

</td><td>

Optionally, select a MID Server for the connection.

</td></tr><tr><td>

API Key

</td><td>

To get the API Key: 1.  Go to your Console and navigate to the **Settings** page.
2.  Open the **API** tab and select the Add ![](../../msi-console/image/add-icon-msi.jpg) icon.
3.  In the **Generate API Token** window, select the expiration length you want and select **Generate Token**.
4.  The generated token is listed in the Active token list.
5.  Select the Copy icon to copy the token.
6.  Paste the token key into the **API Key** field.
7.  Select **Save**.
This field is mandatory.

</td></tr></tbody>
</table>10. Navigate back to the **Configure the connection** page and select **Mark as complete**.


## What to do next

The next step is to [Generate imports and validate the connections](generate-imports-validate-connections.md).

