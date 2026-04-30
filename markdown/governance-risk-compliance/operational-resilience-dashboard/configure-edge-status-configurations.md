---
title: Configure the Edge status configurations
description: Configure the Edge status configurations for the selected Nexus map configuration. You can customize the display of connectors that meet specific conditions by assigning them distinct colors and connector types.
locale: en-US
release: zurich
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-11-06"
reading_time_minutes: 1
breadcrumb: [Configure the Edge configurations, Configure the Main node configurations, Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Configure the Edge status configurations

Configure the Edge status configurations for the selected Nexus map configuration. You can customize the display of connectors that meet specific conditions by assigning them distinct colors and connector types.

## Before you begin

Role required: sn\_oper\_res.admin

## Procedure

1.  Navigate to **All** &gt; **Data Relationships Framework** &gt; **Main node configuration** and open the desired Main node configuration from the list.

2.  Open the desired Nexus map configuration record from the Nexus map configurations related list.

3.  Open the Edge configuration record from the Edge configurations related list.

    In the Edge configuration record, the details of the edge are auto-selected.

4.  In the Edge status configurations related list, select **New**.

    You can customize the map display such as assigning specific colors and icons to nodes that meet certain conditions by configuring the Node status configuration record.

    ![Edge status configuration.](../image/edge-status-new-config.png)![Edge status configuration example.](../image/edge-status-config-example.png)

    For more information on the fields, see [Edge status configuration form](../reference/edge-status-configuration-form.md).

    The Edge status configuration record is displayed in which the **Edge configuration** and **Relationship table** are auto-populated.

5.  Add the conditions that must be satisfied for the node status configuration in the **Conditions** field.

6.  Select the color for the node status in the **Color** field.

7.  Select the Edge type for the node status in the **Edge type** field.

    The order for the node status is auto-selected.

8.  Select the label for the edge status in the **Label** field.

9.  To submit the details of the Edge status configuration, select **Submit**.

    The Edge status configuration record is displayed in the Edge status configurations related list.


