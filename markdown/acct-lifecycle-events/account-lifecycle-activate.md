---
title: Activate Customer Success Management
description: The Customer Success Management \(com.sn\_acct\_lc\) plugin is available as a separate subscription. This plugin activates related plugins, if they aren’t already active.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring Customer Success Management, Customer Success Management]
---

# Activate Customer Success Management

The Customer Success Management \(com.sn\_acct\_lc\) plugin is available as a separate subscription. This plugin activates related plugins, if they aren’t already active.

## Before you begin

Role required: sn\_customerservice.customer\_admin

## About this task

The Customer Success Management plugin activates these related plugins, if they aren’t already active.

|Plugin|Description|
|------|-----------|
|Customer Service Install Base Management \[com.snc.install\_base\]|Enables customers to capture the current state of their install base and establish the relationship to any downstream entities that might impact their functioning.|
|Playbook Experience \[com.playbook\_experience\]|Enables you to customize the default Playbook user experience to create your desired business process workflow.|
|Record Related Items Connected \[com.snc.sn\_record\_related\_items\_connected\]|Enables record related items.|
|Playbooks for Customer Service Management \[com.sn\_csm\_playbook\]|Guides customer service agents through the various tasks to resolve customer issues, and visualizes the entire lifecycle ​across diverse and siloed processes​.|
|Technology core \[com.sn\_ti\_core\]|Technology industry vertical Customer Service Management extensions.|
|Guided Decisions Experience \[com.snc.guided\_decisions\_playbook\_experience\]|Enables activity types, definitions, and UI components for the display of guided decisions in a playbook on Workspace.|
|Customer Service Case Types \[com.snc.csm\_case\_types\]|Activating this plugin enables the system administrator to create and manage case types.|
|Record lookup \[com.snc.sn\_record\_lookup\]|Record lookup component used to easily search and link a record from a table.|
|Data Context Engine \[com.sn\_data\_ctx\_engine\]|Allows for the creation and measuring of metrics and resolving them to specific context \(such as success engagements\) within the platform.|
|Touchpoint meetings \[com.sn\_meeting\_mgmt\]|Enables creation and management of one-time or recurring meetings with customers within the Touchpoint record.|
|Document management \[com.snc.platform\_document\_management\]|Allows customer success managers to store complex documents that can be saved as attachments or in the Knowledge Base.|
|Roadmap \[sn\_roadmap\]|Allows customer success manager to see and plan the roadmap of success initiatives tied to success objectives and outcomes.|

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you can’t find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install**, and then in the Activate Plugin dialog box, select **Activate**.

    **Note:** When domain separation and delegated admin are enabled in an instance, you must be in the **global** domain. Otherwise, the following error message appears:

    ```
    Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>
    ```

    .


