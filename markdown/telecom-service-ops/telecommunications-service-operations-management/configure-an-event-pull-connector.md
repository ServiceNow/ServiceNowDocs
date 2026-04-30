---
title: Configure an event pull connector
description: Configure event pull connectors that require a script, connector definition, and connector instance to pull events from external management systems. These connectors automate the data retrieval process, promoting the seamless integration of external events into your system for efficient monitoring and management.
locale: en-US
release: zurich
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-04-30"
reading_time_minutes: 1
breadcrumb: [Fault Management: Events and alerts, Telecom Assurance, Explore, Telecommunications Service Operations Management]
---

# Configure an event pull connector

Configure event pull connectors that require a script, connector definition, and connector instance to pull events from external management systems. These connectors automate the data retrieval process, promoting the seamless integration of external events into your system for efficient monitoring and management.

## Before you begin

Role required: TSOM Assurance admin

## Procedure

1.  Navigate to &gt; **Workspaces** &gt; **Service Operations Workspace**.

2.  From the left pane, select the Integrations Launchpad icon ![](../images/integrations_launchpad_icon.png).

3.  Select the **Browse Integrations** tab, and search for the desired integration \(for example, Meraki, Fortinet, or VeloCloud\).

    ![Integrations launchpad page](../images/integrations_laundpad.png "Integrations Launchpad page")

4.  Select the integration tile labeled **Metrics**.

    The pull connector setup page opens in a new window.

    ![Pull connector set-up page](../images/pull-connector-setup.png "Pull connectors details page")

5.  In the **Name** field, enter a unique name for the connector type.

6.  In the **Connector definition** field, select the type of integration you’re setting up.

7.  In the **Description** field, enter brief information about this connector.

8.  In the **Assignment group** field, select the group or team that is responsible for managing and maintaining the connector.

9.  In the **Host IP** field, enter the IP address that is used to select the appropriate MID Server for communicating with the event source host.

    You can use the host name instead of the host IP.

10. In the **Credential** field, select the valid credentials to access the event source host.

    To create a credential, select the search icon and then **New**.

11. To validate the connectivity of the connector before activating, select **Test Connector**.

12. To save changes, select **Update**.


## Result

To confirm the pull connector is configured correctly and events are flowing into the system, return to the Integrations Launchpad. The tiles appear under the **Installed Integrations** tab.

