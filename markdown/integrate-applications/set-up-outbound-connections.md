---
title: Set up outbound connections
description: Outbound connections enable ServiceNow to send data to, read data from, or trigger actions in external systems.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Connections and Credentials, Connect, Workflow Data Fabric Home, Workflow Data Fabric]
---

# Set up outbound connections

Outbound connections enable ServiceNow to send data to, read data from, or trigger actions in external systems.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Connect Hub**.

2.  Click the **Connections and Credentials** tab.

3.  You can [create a new external system](connecthub-create-external-systems.md#).

4.  Click **Create** and select **Outbound Connection**.

5.  In the **System** field, select the external system.

6.  In the **Connector Type** field, select the type of connector that this incoming connection will use.

7.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection name|Name of the external system that you want to create an outbound connection to. For example, *Jira*.|
    |Description|A description for the connection to the external system.|
    |Protocol|The connection protocol to connect to the external system.|
    |Retry Policy|Retry policy for the connection. For more information, see Retry policy.|
    | | |

8.  Choose between using a configuration template or custom credentials for adding an endpoint.

9.  Enable the **Configuration Template** option to choose a preexisting configuration.

10. Configure the **Endpoint 1** connection settings:

    |Field|Description|
    |-----|-----------|
    |Endpoint name|Name of the endpoint.|
    |Endpoint URL|Connection URL for the server.|
    |Authentication Method|Select an authentication method and provide the details for your chosen method.|

11. Enable the MID server option and configure the server information.

    For more information, see Configure a MID Server cluster.

12. Click **Add Endpoint** to add additional endpoints for different environments.

13. Click **Save**.


