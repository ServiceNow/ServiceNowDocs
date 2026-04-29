---
title: Activate Customer Success Management
description: The Customer Success Management \(com.sn\_acct\_lc\) plugin is available as a separate subscription. This plugin activates related plugins, if they aren’t already active.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Customer Success Management]
---

# Activate Customer Success Management

The Customer Success Management \(com.sn\_acct\_lc\) plugin is available as a separate subscription. This plugin activates related plugins, if they aren’t already active.

## Before you begin

Role required: sn\_customerservice.customer\_admin

## About this task

The Customer Success Management plugin activates these related plugins, if they aren’t already active.

<table id="table_f4r_m5k_1yb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Customer Service Install Base Management \[com.snc.install\_base\]

</td><td>

Enables customers to capture the current state of their install base and establish the relationship to any downstream entities that might impact their functioning.

</td></tr><tr><td>

Playbook Experience \[com.playbook\_experience\]

</td><td>

Enables you to customize the default Playbook user experience to create your desired business process workflow.

</td></tr><tr><td>

Record Related Items Connected \[com.snc.sn\_record\_related\_items\_connected\]

</td><td>

Enables record related items.

</td></tr><tr><td>

Playbooks for Customer Service Management \[com.sn\_csm\_playbook\]

</td><td>

Guides customer service agents through the various tasks to resolve customer issues, and visualizes the entire lifecycle ​across diverse and siloed processes​.

</td></tr><tr><td>

Technology core \[com.sn\_ti\_core\]

</td><td>

Technology industry vertical Customer Service Management extensions.

</td></tr><tr><td>

Guided Decisions Experience \[com.snc.guided\_decisions\_playbook\_experience\]

</td><td>

Enables activity types, definitions, and UI components for the display of guided decisions in a playbook on Workspace.

</td></tr><tr><td>

Customer Service Case Types \[com.snc.csm\_case\_types\]

</td><td>

Activating this plugin enables the administrator to create and manage case types.

</td></tr><tr><td>

Record lookup \[com.snc.sn\_record\_lookup\]

</td><td>

Record lookup component used to search and link a record from a table.

</td></tr><tr><td>

Data Context Engine \[com.sn\_data\_ctx\_engine\]

</td><td>

Enables for the creation and measuring of metrics and resolving them to specific context \(such as success engagements\) within the platform.

</td></tr><tr><td>

Touchpoint meetings \[com.sn\_meeting\_mgmt\]

</td><td>

Enables creation and management of single or recurring meetings with customers within the Touchpoint record.

</td></tr><tr><td>

Document management \[com.snc.platform\_document\_management\]

</td><td>

Enables customer success managers to store complex documents that can be saved as attachments or in the Knowledge Base.

</td></tr><tr><td>

Roadmap \[sn\_roadmap\]

</td><td>

Enables customer success manager to see and plan the roadmap of success initiatives tied to success objectives and outcomes.

</td></tr><tr><td>

Product capability core \[com.sn\_prod\_cap\_core\]

</td><td>

Enables organizations to define, manage, and assess capabilities across product models within the ServiceNow platform.

</td></tr><tr><td>

Customer central \[app-customer-central\]

</td><td>

Enables customer service agents to view complete information on the customer contacting support.

</td></tr><tr><td>

Seismic component for customer activity \[devsnc-sn-customer-activity\]

</td><td>

Shows all activities related to a contact, account, or consumer to an agent. This information can be used by an agent to assist the customer.

 This component accepts facets and activity feed items in JSON format along with a few other properties and renders given activities and facets.

</td></tr><tr><td>

Customer Success Advanced \(app-cust-succ-adv\)

</td><td>

New pro plus plugin for customer success. Used for product adoption roadmap.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **Application Manager**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you can’t find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install**, and then in the Activate Plugin dialog box, select **Activate**.

    **Note:** When domain separation and delegated admin are enabled in an instance, you must be in the **global** domain. Otherwise, the following error message appears:

    ```
    Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>
    ```

    .


