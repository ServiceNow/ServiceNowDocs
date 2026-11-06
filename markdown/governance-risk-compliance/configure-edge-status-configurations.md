---
title: Configure the Connector status configurations
description: Configure the Connector status configurations for the selected Nexus map configuration. You can customize the display of connectors that meet specific conditions by assigning them distinct colors and connector types.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/governance-risk-compliance/configure-edge-status-configurations.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure the Connector configurations, Configure the Main node configurations, Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Configure the Connector status configurations

Configure the Connector status configurations for the selected Nexus map configuration. You can customize the display of connectors that meet specific conditions by assigning them distinct colors and connector types.

## Before you begin

Role required: sn\_oper\_res.admin

## Procedure

1.  Navigate to **All** &gt; **Data Relationships Framework** &gt; **Main node configuration** and open the desired Main node configuration from the list.

2.  Open the desired Nexus map configuration record from the Nexus map configurations related list.

3.  Open the Connector configuration record from the Connector configurations related list.

    In the Connector configuration record, the details of the connector are auto-selected.

4.  In the Connector status configurations related list, select **New**.

    You can customize the map display such as assigning specific colors and icons to nodes that meet certain conditions by configuring the Node status configuration record.

    \[Omitted image "edge-status-new-config.png"\] Alt text: Connector status configuration.\[Omitted image "edge-status-config-example.png"\] Alt text: Connector status configuration example.

    For more information on the fields, see [Connector status configuration form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/edge-status-configuration-form.md).

    The Connector status configuration record is displayed in which the **Connector configuration** and **Relationship table** are auto-populated.

5.  Add the conditions that must be satisfied for the node status configuration in the **Conditions** field.

6.  Select the color for the node status in the **Color** field.

7.  Select the connector type for the node status in the **Connector type** field.

    The order for the node status is auto-selected.

8.  Select the label for the connector status in the **Label** field.

9.  To submit the details of the Connector status configuration, select **Submit**.

    The Connector status configuration record is displayed in the Connector status configurations related list.


