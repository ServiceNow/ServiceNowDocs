---
title: Manage system properties for AI applications in AI Admin Center
description: Use the system property registry to view and edit the system properties for the AI applications in your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-admin-center-manage-system-properties.html
release: zurich
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 1
keywords: [AI Admin Center, Now Assist Center, AI, AI setup]
breadcrumb: [Managing AI assets, Setting up AI capabilities and configurations, AI Admin Center, Enable AI experiences]
---

# Manage system properties for AI applications in AI Admin Center

Use the system property registry to view and edit the system properties for the AI applications in your instance.

## Before you begin

Role required: sn\_na\_center.nac\_admin

An elevated role may be required to perform some of the actions in this task.

## About this task

Follow these steps to view and edit the system properties for the AI applications in your instance.

For more information on system properties, see [Available system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/r_AvailableSystemProperties.md).

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** or **Workspaces** &gt; **AI Admin Center**.

2.  Select **Settings** \(\[Omitted image "icon-aiac-lux-nav-settings.png"\] Alt text: Settings icon.\) in the side navigation panel.

    The Settings page opens.

3.  Select **System Property Registry** under the **General** heading.

    The System Property Registry page opens showing a list of all AI-related system properties grouped by application scope.

    \[Omitted image "ai-admin-center-sys-prop-registry.png"\] Alt text: \[Omitted image ""\] Alt text: System properties registry page showing a list of AI-related system properties.

4.  Select one or more options from the **Application scope** filter to refine the list.

5.  Edit the system properties as needed.

    1.  Go to the selected application scope.

        Editing is enabled only for the selected application scope. Select **Switch to this scope** to enable editing for properties in a different scope.

        The scope panel displays **Editing enabled**.

    2.  Select the system property to edit.

        The system property panel opens showing the property details.

    3.  Edit the value in the configuration box based on the value type.

        -   Type a new value within the stated restrictions.
        -   Toggle the **On-Off** option to a different value.
    4.  Select **Save changes**.


**Parent Topic:**[Managing AI assets in AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-center-using-asset-inventory.md)

**Related topics**  


[View and manage your AI assets in the asset inventory]()

[Create an AI asset in the asset inventory]()

