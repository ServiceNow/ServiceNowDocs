---
title: Configure the Connector configurations
description: Review and update the Connector configurations for the selected Nexus map configuration. You can configure the label, tooltip, and default Connector type for each connector between nodes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/governance-risk-compliance/configure-edge-configurations.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure the Main node configurations, Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Configure the Connector configurations

Review and update the Connector configurations for the selected Nexus map configuration. You can configure the label, tooltip, and default Connector type for each connector between nodes.

## Before you begin

Role required: sn\_oper\_res.admin

## About this task

The system automatically creates a Connector configuration for each Node relationship configuration in the Main node configuration when you create the Nexus map configuration. To pick up later changes to the Main node configuration, use the **Sync from main node configuration** UI action on the Nexus map configuration.

## Procedure

1.  Navigate to **All** &gt; **Data Relationships Framework** &gt; **Main node configuration** and open the desired Main node configuration from the list view.

2.  Open the Nexus map configuration record from the Nexus map configurations related list.

3.  In the **Connector configurations** related list, open the Connector configuration record that you want to configure.

    For more information on the fields, see [Connector configuration form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/edge-configuration-form.md).

    \[Omitted image "edge-config-record.png"\] Alt text: Connector configurations related list.

    The Nexus map configuration, Node relationship configuration, Source table, Target table, and Relationship table fields are read-only in the Connector configuration record.

4.  To mark the Connector configuration as active, select the **Active** option field.

5.  Select the label for the connector in the **Label** field.

6.  Select the tooltip for the connector in the **Tooltip** field.

7.  Select the default connector type in the **Default Connector type** field.

8.  To clear the selections for the label and tooltip, select **Clear selections**.

9.  To save your changes to the Connector configuration, select **Save**.


