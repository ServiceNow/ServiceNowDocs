---
title: Configure list editor properties
description: Configure list editor properties that control whether lists can be edited and, in List v2, which field types cannot be edited.
locale: en-US
release: australia
product: List Administration
classification: list-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [List editor, Administer, List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure list editor properties

Configure list editor properties that control whether lists can be edited and, in List v2, which field types cannot be edited.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **UI Properties**.

2.  To disable list editing, set the **Enable list editing** \(**glide.ui.list\_edit**\) property to **No** by clearing the check box.

    This property is enabled by default, and it globally enables list editing. When you disable it, the list editor is disabled globally.

3.  To configure the field types that cannot be edited for v2 lists, complete the following steps.

    1.  Locate the **List of element types \(comma-separated\) that cannot be edited in the list editor** \(**glide.ui.list\_edit\_ignore\_types**\) property, which contains several element types that cannot be edited by default.

        **Note:** This property does not impact v3 lists. There is no equivalent property for List v3.

        The following field types are not editable from the list editor by default.

        -   Conditions \[conditions\]
        -   Currency \[currency\]
        -   Document ID \[document\_id\]
        -   Field List \[field\_list\]
        -   HTML \[html\]
        -   Image \[user\_image\]
        -   List \[glide\_list\]
        -   Price \[price\]
        -   Template Value \[template\_value\]
        -   Time \[glide\_time\]
        -   User Roles \[user\_roles\]
        -   Video \[video\]
        -   Array \[array\]
    2.  Add any other field types you want to disable to the end of the list, separated by a comma.

4.  Select **Save**.


