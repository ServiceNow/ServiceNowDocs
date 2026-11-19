---
title: Configure list editor properties
description: Configure list editor properties that control whether lists can be edited and, in List v2, which field types cannot be edited.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/list-administration/t\_ConfigureListEditorProperties.html
release: brazil
product: List Administration
classification: list-administration
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [List editor, Administer, List administration, Forms, fields, and lists, Configure core features, ServiceNow AI Platform]
---

# Configure list editor properties

Configure list editor properties that control whether lists can be edited and, in List v2, which field types cannot be edited.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **UI Properties**.

2.  To turn off list editing, set the **Enable list editing** \(**glide.ui.list\_edit**\) property to **No** by clearing the check box.

    This property is selected by default. When you clear it, list editing is turned off for all lists.

3.  To configure the field types that cannot be edited for v2 lists, complete the following steps.

    1.  Locate the **List of element types \(comma-separated\) that cannot be edited in the list editor** \(**glide.ui.list\_edit\_ignore\_types**\) property, which contains several element types that cannot be edited by default.

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
    2.  Add any other field types to exclude from list editing to the end of the list, separated by a comma.

4.  Select **Save**.


