---
title: Enable support for right-to-left languages
description: When the session language is a right-to-left language, the direction of the portal user interface is mirrored to display from right to left.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Admin configurations, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Enable support for right-to-left languages

When the session language is a right-to-left language, the direction of the portal user interface is mirrored to display from right to left.

## Before you begin

Understand how the UI works for a right-to-left language, see [CSS for right-to-left languages in portals](https://servicenow.com/docs/bundle/vancouver-platform-user-interface/page/build/service-portal/concept/css-directives-right-to-left-languages.html).

Role required: sp\_admin or admin

## About this task

Based on the selected language preferences, the entire hierarchy of existing infrastructure for styling left-to-right languages—the theme, page, widget, and widget instance SCSS—is converted to CSS for right-to-left languages.

-   When the session language is a right-to-left language, for example Hebrew, the direction of the portal user interface displays from right to left.
-   The arrow next to View Org Chart in employee\_profile widget, View All in ec\_pro\_dashboard, employee taxonomy topic widget, and across Employee Center points to left per the RTL format.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Portals**.

2.  Select the Employee Center portal.

3.  Select the **Support right-to-left languages** option.

4.  Select **Update**.

    CSS that mirrors the direction of a portal user interface for right-to-left languages is generated.


## Result

When the session language is a right-to-left language, the direction of the portal user interface displays from right-to-left. The arrow next to View Org Chart in employee\_profile widget, View All in ec\_pro\_dashboard, employee taxonomy topic widget, and across Employee Center points to left per the RTL format.

**Note:** When you support Right-to-Left languages, change the **Card Content Alignment** field value to Right. Alternatively, use the center alignment to avoid issues.

For more information, see [Modify the Quick links widget display](../task/config-quick-links-widget.md).

