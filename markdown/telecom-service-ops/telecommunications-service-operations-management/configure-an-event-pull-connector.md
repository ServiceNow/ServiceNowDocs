---
title: Configure a metric pull connector
description: Configure metric pull connectors to retrieve performance data from external management systems such as Meraki, Fortinet, or VeloCloud.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/configure-an-event-pull-connector.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 2
breadcrumb: [Configure Telecom Assurance, Configure, Telecommunications Service Operations Management]
---

# Configure a metric pull connector

Configure metric pull connectors to retrieve performance data from external management systems such as Meraki, Fortinet, or VeloCloud.

## Before you begin

Role required: TSOM Assurance admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation pane, select the Integrations Launchpad icon \[Omitted image "integrations\_launchpad\_icon.png"\] Alt text:.

3.  Select the **Browse Integrations** tab

4.  Search for the external management system integration \(for example, Meraki, Fortinet, or VeloCloud\).

5.  Select the integration tile labeled **Metrics**.

6.  On the Connector Instance New record page, in the **Name** field, enter a unique name for the connector type.

7.  In the **Connector definition** field, select the type of integration you're setting up.

8.  In the **Description** field, enter brief information about this connector.

9.  In the **Assignment group** field, select the group or team responsible for managing and maintaining the connector.

10. In the **Host IP** field, enter the IP address or host name used to select the appropriate MID Server for communicating with the event source host.

11. In the **Credential** field, select the valid credentials to access the event source host.

12. In the **Metrics collection schedule \(seconds\)** field, enter the polling interval for metric collection.

    **Important:** For a device performance \(CPU usage\) connector instance, if you enter a value below 1800 seconds \(30 minutes\), the system automatically resets the schedule to 1800 seconds and displays a message. For a Fortinet interface logs connector instance, if you enter a value above 600 seconds \(10 minutes\), the system automatically resets the schedule to 600 seconds and displays a message. In both cases, the record saves successfully. This enforcement applies only when a numeric value is entered; an empty or blank field bypasses it.

13. Validate the connectivity of the connector before activating it by selecting **Test Connector**.

14. Select **Update**.

15. Verify that the pull connector is configured correctly and events are flowing into the system by returning to the Integrations Launchpad.

    The tiles appear under the **Installed Integrations** tab.


**Parent Topic:**[Configure Telecom Assurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/set-up-fault-management.md)

**Related topics**  


[Exploring Metric Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/exploring-metric-intelligence.md)

[Arista VeloCloud installed integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/arista-velocloud-installed-integrations.md)

[Cisco Meraki installed integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/meraki-installed-integrations.md)

[Fortinet installed integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/fortinet-installed-integrations.md)

