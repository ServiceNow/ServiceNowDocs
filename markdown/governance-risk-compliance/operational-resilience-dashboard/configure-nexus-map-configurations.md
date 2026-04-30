---
title: Configure the Nexus map configurations
description: Configure the appearance of the Nexus map \(Resilience map\) for a specific main node by defining its UI settings. It involves defining visual elements such as colors, icons, and edge configurations. By configuring the settings at the Nexus map level, you can associate a single main node with multiple Nexus configurations, enabling flexible loading of settings for different entities.
locale: en-US
release: zurich
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-11-06"
reading_time_minutes: 3
breadcrumb: [Configure the Main node configurations, Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Configure the Nexus map configurations

Configure the appearance of the Nexus map \(Resilience map\) for a specific main node by defining its UI settings. It involves defining visual elements such as colors, icons, and edge configurations. By configuring the settings at the Nexus map level, you can associate a single main node with multiple Nexus configurations, enabling flexible loading of settings for different entities.

## Before you begin

Role required: sn\_oper\_res.admin

## About this task

**Note:** When you create the Nexus map configuration, the system automatically creates the nodes list and edges list from the Main node configuration, prompting you to configure the node and edge visualization. If you have already created a configuration for a specific node type in another Nexus map configuration, it is pre-populated with the most recently created configuration.

## Procedure

1.  Navigate to **All** &gt; **Data Relationships Framework** &gt; **Main node configuration**.

2.  Open the desired Main node configuration from the list.

    The following example shows the Main node configurations available in the instance.

    ![Main node configurations.](../image/main-node.png)

3.  In the Nexus map configurations related list, select **New**.

    The Nexus map configuration new record is displayed as shown in the example.

    ![New record.](../image/nexus-map-new-record-empty.png)

    For more information on the fields, see [Nexus map configuration form](../reference/nexus-map-configuration-form.md).

4.  Enter a unique name for the Nexus map configuration in the **Name** field.

    The Main node configuration record for which the Nexus map configuration is being configured is displayed by default in the **Main node configuration** field.

5.  Select the desired Workspace in the **Workspace type** field.

    **Note:** If the desired Workspace isn't available in the field, you can create a workspace record by accessing the "Nexus map configuration workspace type" module through the **All** menu.

6.  Add a short description for the Nexus map configuration in the **Short description** field.

7.  To mark the Nexus map configuration as active, select the **Active** option field.

    A sample record is shown for reference.

    ![Nexus map configuration new record.](../image/nexus-map-new-record.png)

8.  To submit the details of the Nexus map configuration, select **Submit**.

    The Nexus map configuration record is displayed in the Nexus map configurations related list as shown in the example.

    ![Nexus map configuration record.](../image/nexus-map-config-record.png)

    Opening the record shows the details of the Nexus map configuration as shown in the following examples.

    ![Tab1.](../image/nexus-map-config-record-tab1.png)![Tab2.](../image/nexus-map-config-record-tab2.png)

    The **Main node** tab displays the name of the Main node table along with its associated conditions. The **Node UI details** tab shows the Node UI type, which is set to "Node map default node" by default.

    After creating the Nexus map configuration, if any changes are made at the Main node level, such as adding or modifying relationships, you can synchronize those changes into the Nexus map configuration by using the **Sync from main node configuration** UI action.

    The Node configurations and Edge configurations related lists for the selected Nexus map configuration, as shown in the examples, are displayed in the record.


## What to do next

To configure the node settings for the Nexus map, see [Configure the Node configurations](configure-node-configurations.md).

To configure the edge settings for the Nexus map, see [Configure the Edge configurations](configure-edge-configurations.md).

