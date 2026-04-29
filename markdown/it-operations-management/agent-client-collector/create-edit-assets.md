---
title: Create and edit Agent Client Collector plugins
description: You can edit the default plugins, or you can add new plugins, as needed. Creating and editing plugins customizes the Agent Client Collector monitoring capabilities.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
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


-   **[Secure a custom plugin with a certificate](../concept/acc-self-sign-certificate.md)**  
When you customize or create an Agent Client Collector plugin, you can secure the plugin with either a third-party certificate or an internal secure certificate in the plugin's script. Official plugins are signed by an external certificate authority.

**Parent Topic:**[Deploying Agent Client Collector on servers](../concept/acc-server-deployment.md)

