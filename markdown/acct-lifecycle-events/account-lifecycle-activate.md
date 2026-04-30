---
title: Activate Account Lifecycle Events
description: The Account Lifecycle Events \(com.sn\_acct\_lc\) plugin is available as a separate subscription. This plugin activates related plugins, if they aren’t already active.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring account onboarding, Account onboarding, Account Lifecycle Events]
---

# Activate Account Lifecycle Events

The Account Lifecycle Events \(com.sn\_acct\_lc\) plugin is available as a separate subscription. This plugin activates related plugins, if they aren’t already active.

## Before you begin

Role required: sn\_customerservice.customer\_admin

## About this task

The Account Lifecycle Events plugin activates these related plugins, if they aren’t already active.

|Plugin|Description|
|------|-----------|
|Technology core \[com.sn\_ti\_core\]|Technology industry vertical Customer Service Management extensions.|
|Customer Service \[com.sn\_customerservice\]|Automate your processes and give service agents visibility into the customer systems and tools that they require to deliver proactive services to your customers.|
|Customer Service Install Base Management \[com.snc.install\_base\]|Enables customers to capture the current state of their install base and establish the relationship to any downstream entities that might impact their functioning.|
|Playbook Experience Core \[com.glide.playbook\_experience.config\]|Enables you to customize the default Playbook user experience to create your desired business process workflow.|
|Playbooks for Customer Service Management \[com.sn\_csm\_playbook\]|Guides customer service agents through the various tasks to resolve customer issues, and visualizes the entire lifecycle ​across diverse and siloed processes​.|
|Customer Service Case Types \[com.snc.csm\_case\_types\]|Activating this plugin enables the system administrator to create and manage case types.|
|Record Related Items Connected \[com.snc.sn\_record\_related\_items\_connected\]|Enables record related items.|
|Guided Decisions Experience \[com.snc.guided\_decisions\_playbook\_experience\]|Enables activity types, definitions, and UI components for the display of guided decisions in a playbook on Workspace.|

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you can’t find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install**, and then in the Activate Plugin dialog box, select **Activate**.

    **Note:** When domain separation and delegated admin are enabled in an instance, you must be in the **global** domain. Otherwise, the following error appears:

    ```
    Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>
    ```

    .


