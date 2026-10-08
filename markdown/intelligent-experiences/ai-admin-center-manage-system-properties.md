---
title: Manage system properties for AI applications in AI Admin Center \(Lux UI\)
description: Use the system property registry to view and edit the system properties for the AI applications in your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-admin-center-manage-system-properties.html
release: australia
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 2
keywords: [AI Admin Center, Now Assist Center, AI, AI setup]
breadcrumb: [Using other AI applications from AI Admin Center, Setting up AI capabilities and configurations, AI Admin Center, Enable AI experiences]
---

# Manage system properties for AI applications in AI Admin Center \(Lux UI\)

Use the system property registry to view and edit the system properties for the AI applications in your instance.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for deprecation in the November store release and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

## Before you begin

Role required: sn\_na\_center.nac\_admin

An elevated role may be required to perform some of the actions in this task. You must also have the role for the capability that the system property belongs to.

## About this task

Follow these steps to view and edit the system properties for the AI applications in your instance.

For more information on system properties, see [Available system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

**Note:** This topic describes the AI Admin Center feature based on the Lux user experience \(UI\). There is no Next Experience UI version of this topic.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** &gt; **Home** or **Admin** &gt; **AI Admin Center**.

2.  Select **Settings** \(\[Omitted image "icon-aiac-lux-nav-settings.png"\] Alt text: Settings icon.\) in the side navigation panel.

    The Settings page opens.

3.  Select **System Property Registry** under the **General** heading.

    The System Property Registry page opens showing a list of all AI-related system properties grouped by application scope.

    \[Omitted image "ai-admin-center-sys-prop-registry.png"\] Alt text: System properties registry page showing a list of AI-related system properties.

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


