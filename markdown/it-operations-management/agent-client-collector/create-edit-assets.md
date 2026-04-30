---
title: Create and edit Agent Client Collector plugins
description: You can edit the default plugins, or you can add new plugins, as needed. Creating and editing plugins customizes the Agent Client Collector monitoring capabilities.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Create and edit Agent Client Collector plugins

You can edit the default plugins, or you can add new plugins, as needed. Creating and editing plugins customizes the Agent Client Collector monitoring capabilities.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Configuration** &gt; **ACC Plugins**.

2.  Click **New**.

    The **Agent Client Collector Plugin - New record** page appears.

3.  Enter values in the fields on the page, as described in the following table.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the plugin. This field is populated automatically with the name of the tar.gz file attached to the plugin, and is visible only when selecting an existing record.|
    |Description|Description of the plugin.|
    |Operating System|Select the operating system to be monitored by the plugin.|
    |Platform|Select the platform to be monitored by the plugin.|
    |Active|Select to activate the plugin and download it to the MID server.|
    |Advanced|Select to enable selecting the operating system version to be monitored by the plugin.|
    |OS Version|Select the operating system version to be monitored by the plugin. This field is visible only when selecting the **Advanced** check box.|

4.  Attach the `tar.gz` file to the plugin record, according to the instructions that appear on the UI page.


