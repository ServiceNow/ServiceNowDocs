---
title: Customize the Zoom chat form
description: Customize the chat form for additional ServiceNow Collaboration services tables by creating a chat configuration.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Chat-specific configuration for Collaboration services for Zoom, Enhance employee experience by integrating ServiceNow with Zoom, Integrating and using ServiceNow with Zoom, ServiceNow for Zoom, Unified Employee Experience, Employee Service Management]
---

# Customize the Zoom chat form

Customize the chat form for additional ServiceNow® Collaboration services tables by creating a chat configuration.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Collaboration Services** &gt; **Zoom** &gt; **Chat Configuration**.

2.  Click  **Default ** to view the default base system configuration.

3.  Navigate to **All** &gt; **Collaboration Services** &gt; **Zoom** &gt; **Chat Configuration**.

4.  Create a new chat configuration Select **New**.

5.  On the form, fill in the fields.

<table id="id_ely_h4x_3vb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Value for the configuration.

</td></tr><tr><td>

Order

</td><td>

Order of the configuration.

 You can define multiple chat configurations for a single table. The system executes the query based on the descending order.

</td></tr><tr><td>

Active

</td><td>

Option to activate the configuration.

 Select the check box to activate the configuration.

</td></tr><tr><td>

Messaging Type

</td><td>

Option to select the messaging platform.

</td></tr><tr><td>

Default

</td><td>

Option to keep the configuration as default.

 **Note:** You cannot define multiple default values for chat configuration.

</td></tr><tr><td>

Auto Import

</td><td>

Option to automatically import the chat.

 Select the check box to automatically import the chat.

</td></tr><tr><td>

Table

</td><td>

Option to select specific chat feature for a table.

</td></tr><tr><td>

Inherit

</td><td>

Extend and apply to the configuration to the child tables.

</td></tr><tr><td>

Conditions

</td><td>

Option to define a condition for a chat for customizations.

</td></tr><tr><td>

Enable opening message

</td><td>

Option to provide a text message that displays to the user when the agent initiates a chat.

</td></tr><tr><td>

Opening message

</td><td>

Option to enable a text message that displays to the user when the agent initiates a chat.

 This field is enabled only if the  **Enable opening message**  option is selected.

</td></tr></tbody>
</table>6.  Select **Submit**.

    The defined chat configuration defined is applicable only for the selected table. You can extend the chat configuration to other tables by creating another chat configuration record.


**Parent Topic:**[Chat-specific configuration for Collaboration services for Zoom](../concept/additional-configuration-sn-cs-zoom.md)

