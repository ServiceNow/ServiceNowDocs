---
title: Configure assignment group types
description: Use the Type field to define categories of groups. Once defined, you can use these categories to filter assignment groups based on the group type using a reference qualifier.You can add additional group types to filter assignment groups for tasks.You can assign group types to filter assignment groups for tasks.
locale: en-US
release: australia
product: User Administration
classification: user-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Creating groups, User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure assignment group types

Use the **Type** field to define categories of groups. Once defined, you can use these categories to filter assignment groups based on the group type using a reference qualifier.

For example, when selecting an assignment group from the Incident form, **Type** can be used to filter groups based on whether they’re typically involved in the Incident management process. Groups such as Network or Help Desk are displayed as they’re typically involved. Groups such as HR or New York are omitted.

The following items are provided in the base system.

-   The types **catalog**, **itil**, and **survey**.
-   The reference qualifier on \[task.assignment\_group\] filters on **\[Type\] \[equals\] \[itil\]**.
-   A reference qualifier named **GetGroupFilter** is available to filter for group types using [Create a dynamic filter option](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/t_DynamicFilterOptions.md).

**Note:** Dictionary overrides enable administrators to filter a group type on an extended table using a simple [reference qualifier](../../../script/server-scripting/concept/c_ReferenceQualifiers.md) override.

**Parent Topic:**[Creating groups](../../roles/concept/ua-creating-groups.md)

## Add a group type

You can add additional group types to filter assignment groups for tasks.

### Before you begin

Role required: admin

### About this task

You may need to configure the form to display the **Type** field. For more information see: [Personalize a form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/t_PersonalizeAForm.md)

### Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Groups**.

2.  Select a group record.

3.  Select the lock icon beside **Type**.

4.  Select the lookup icon beside the selection field.

    The Group Types dialog opens.

5.  Complete the following steps.

    1.  Select **New**.

    2.  Enter the group type name and description.

        For example, to define a type for a group as **incident** and **problem**, enter: **incident,problem**.

        Select **Submit**.

    The Group form reopens with the new type listed.

6.  Add additional group types if needed.

7.  Select **Update**.


## Assign a group type

You can assign group types to filter assignment groups for tasks.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Groups** and select the desired group.

2.  Select the lock icon beside **Type**.

3.  Select the lookup icon beside the selection field and select one or more group types.

    **Note:** Because the default behavior of task.assignment\_group is to filter out groups with group types defined, adding a type to a group filters it out of the **Assignment Group** field on tasks. To change the behavior, set up the reference qualifier.

4.  Select **Update**.


