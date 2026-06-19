---
title: Configure the Node configurations
description: Configure the settings for the selected node. It helps you to determine the UI display in the Nexus map. You can select the table associated with the node and configure the primary label, icon, secondary label, tooltip, and so on for the node.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/configure-node-configurations.html
release: zurich
topic_type: task
last_updated: "2025-11-06"
reading_time_minutes: 2
breadcrumb: [Configure the Main node configurations, Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Configure the Node configurations

Configure the settings for the selected node. It helps you to determine the UI display in the Nexus map. You can select the table associated with the node and configure the primary label, icon, secondary label, tooltip, and so on for the node.

## Before you begin

Role required: sn\_oper\_res.admin

## Procedure

1.  Navigate to **All** &gt; **Data Relationships Framework** &gt; **Main node configuration** and open the desired Main node configuration from the list view.

2.  Open the Nexus map configuration record from the Nexus map configurations related list.

    The following example shows the Nexus map configuration record with the Node configurations related list.

    \[Omitted image "nexus-map-config-record-tab1.png"\] Alt text: Tab1.

3.  In the Node configurations related list, select **New**.

    The Node configuration new record is displayed as shown in the example.

    \[Omitted image "node-config-new-record.png"\] Alt text: Node configuration new record.

    For more information on the fields, see [Node configuration form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/node-configuration-form.md).

4.  Select the table in the **Table** field.

    The Nexus map configuration record for which the Node configuration is being configured is displayed by default in the **Nexus map configuration** field.

5.  Select the primary and secondary labels for the node in the **Primary label** and **Secondary label** fields.

6.  Select the icon and tooltip for the node in the **Icon** and **Tooltip** fields.

7.  To mark the Node configuration as active, select the **Active** option field.

8.  To enable the 'Make this primary' functionality at the node level, configure the setting by selecting the Nexus map configuration in the **Configuration for set as main node** field.

    This configuration reflects the hierarchy flow for the node that is designated as primary.

9.  Select the 360° view type in the **Configuration for 360° view** field.

10. Select the Context record in the **Context record** field.

    A sample record with the details filled in is shown for reference.

    \[Omitted image "node-config-sample.png"\] Alt text: Sample.

11. To clear the selections for the context record, primary label, secondary label, tooltip, select **Clear selections**.

12. To submit the details of the Node configuration, select **Submit**.

    The Node configuration record is displayed in the Nexus map configurations related list.

    \[Omitted image "nexus-map-config-record-tab1.png"\] Alt text: Record.


## What to do next

To customize the map display such as assigning specific colors and icons to nodes that meet certain conditions, configure the Node status configuration. For more information, see [Configure the Node status configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/configure-node-status-configurations.md).

