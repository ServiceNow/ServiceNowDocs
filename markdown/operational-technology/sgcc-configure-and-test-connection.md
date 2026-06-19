---
title: Configure and test connections
description: The SGC Central playbook launches when you start to configure and test connection.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/sgcc-configure-and-test-connection.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: task
last_updated: "2026-05-19"
reading_time_minutes: 1
breadcrumb: [SGC Central, Service Graph Connector for ServiceNow Operational Technology \(OT\) Discovery, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Configure and test connections

The SGC Central playbook launches when you start to configure and test connection.

## Before you begin

Role required: admin

## Procedure

1.  From **Setup** section, select **Configure and test connections**.

    After you select the **Create connection** button, a guided playbook experience launches automatically. The playbook walks you through each required configuration step for the Operational Technology Discovery connector.

2.  Select the **Create connection** button.

    \[Omitted image "sgc-central-configure-connections-2.png"\] Alt text: Create connection

    The **Create connection** window opens.

3.  In the **Create connection** window, select **OT Discovery**.

4.  Select the **Create connection** button in this window.

5.  Fill in the connection details as explained in the following table.

    \[Omitted image "config-and-test-connection-11.png"\] Alt text: Configure and test connection

<table id="table_utt_3fc_23c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Enter a unique name for the connection. The default connection has the name as OT Discovery and is read-only. For additional connections, enter a unique name for each.

This field is mandatory.

</td></tr><tr><td>

Connection URL

</td><td>

Navigate to the Console and copy its URL and paste it into the Connection URL field. For example: https://OTDiscoveryConsole.net:8443/

This field is mandatory.

</td></tr><tr><td>

API Key

</td><td>

To get the API Key: 1.  Go to your Console and navigate to the **Settings** page.
2.  Open the **API** tab and select the Add \[Omitted image "add-icon-msi.jpg"\] Alt text: Add icon.
3.  In the **Generate API Token** window, select the expiration length you want and select **Generate Token**.
4.  The generated token is listed in the Active token list.
5.  Select the Copy icon to copy the token.
6.  Paste the token key into the **API Key** field.
7.  Select **Save**.
This field is mandatory.

</td></tr><tr><td>

Use MID Server

</td><td>

This is optional. Check this box to use a MID Server for the connection.

</td></tr></tbody>
</table>6.  Select the **Create and test connection** button.

7.  If successful, you see the **Connections verified** banner.

8.  Select **Continue** to move to the next step.


