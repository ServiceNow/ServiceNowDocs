---
title: Configure an event pull connector
description: Configure event pull connectors that require a script, connector definition, and connector instance to pull events from external management systems. These connectors automate the data retrieval process, promoting the seamless integration of external events into your system for efficient monitoring and management.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Configure Telecom Assurance, Configure, Telecommunications Service Operations Management]
---

# Configure an event pull connector

Configure event pull connectors that require a script, connector definition, and connector instance to pull events from external management systems. These connectors automate the data retrieval process, promoting the seamless integration of external events into your system for efficient monitoring and management.

## Before you begin

Role required: TSOM Assurance admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation pane, select the Integrations Launchpad icon ![](../images/integrations_launchpad_icon.png).

3.  Select the **Browse Integrations** tab

4.  Search for the external management system integration \(for example, Meraki, Fortinet, or VeloCloud\).

5.  Select the integration tile labeled **Metrics**.

6.  On the Connector Instance New record page, in the **Name** field, enter a unique name for the connector type.

7.  In the **Connector definition** field, select the type of integration you're setting up.

8.  In the **Description** field, enter brief information about this connector.

9.  In the **Assignment group** field, select the group or team responsible for managing and maintaining the connector.

10. In the **Host IP** field, enter the IP address or host name used to select the appropriate MID Server for communicating with the event source host.

11. In the **Credential** field, select the valid credentials to access the event source host.

12. Validate the connectivity of the connector before activating it by selecting **Test Connector**.

13. Select **Update**.

14. Verify that the pull connector is configured correctly and events are flowing into the system by returning to the Integrations Launchpad.

    The tiles appear under the **Installed Integrations** tab.


**Parent Topic:**[Configure Telecom Assurance](../concept/set-up-fault-management.md)

**Related topics**  


[Exploring Metric Intelligence](https://www.servicenow.com/docs/access?context=exploring-metric-intelligence&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)

