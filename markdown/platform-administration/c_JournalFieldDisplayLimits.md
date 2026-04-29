---
title: Journal field display limits
description: Journal fields can greatly increase the size of task records because they allow users to enter very large string values.You can set the maximum display size for journal fields by adding a system property.Set the size of the glide.max\_journal\_list\_size system property. When a journal field exceeds this size, the instance displays a preview rather than the field's entire contents. Users can click the Show All button to see the rest of the field's contents.To set the maximum number of entries the system shows in the activity formatter, edit the following system property. The activity formatter displays the entries starting with the most recent entry up to the maximum number.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Journal field type, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Journal field display limits

Journal fields can greatly increase the size of task records because they allow users to enter very large string values.

Display limits prevent the instance from loading the entire journal field into memory. Administrators have the option to:

-   Set the length at which journal fields stop displaying the entire field's contents and instead only display a portion \(called a preview\) of the field's contents. Users can still access the field's entire contents by clicking a **Show All** button.
-   Set the size of the preview text the journal field displays.
-   Set the maximum number of journal entries journal fields can display.

In Core UI, journal fields and the activity formatter must be in the same form section. You cannot place another field in between a journal field and the activities formatter. The Activity Stream is built to keep journal fields stacked on top of the activity formatter.

**Note:** Journal field display limits are not supported in the legacy **Comments and Worknotes** field.

## Set the maximum display size for journal fields

You can set the maximum display size for journal fields by adding a system property.

### Before you begin

Role required: admin

### About this task

When a journal field exceeds the length set in this property, the instance shows a preview of the journal field instead of the field's entire contents. The preview includes a **Show All** button to display the rest of the field's contents. A [separate property](c_JournalFieldDisplayLimits.md#) determines the number of characters the preview displays.

### Procedure

1.  [Add a system property](../../reference-pages/reference/r_AvailableSystemProperties.md#) with the following settings.

    |Property|Value|
    |--------|-----|
    |Name|glide.max\_journal\_list\_size|
    |Description|Size in megabytes when a journal field should display a preview rather than the field's entire contents.|
    |Type|Integer|
    |Value|10|

2.  Click **Submit**.


## Set the journal preview size

Set the size of the **glide.max\_journal\_list\_size** system property. When a journal field exceeds this size, the instance displays a preview rather than the field's entire contents. Users can click the **Show All** button to see the rest of the field's contents.

### Before you begin

Role required: admin

### Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  Select **New**.

3.  Set the values for the property as listed in the table.

    |Property|Value|
    |--------|-----|
    |Name|glide.shortened\_journal\_length|
    |Description|Number of characters to display as a preview of journal fields.|
    |Type|Integer|
    |Value|512000|

4.  Select **Submit**.


## Set the maximum number of journal entries

To set the maximum number of entries the system shows in the activity formatter, edit the following system property. The activity formatter displays the entries starting with the most recent entry up to the maximum number.

### Before you begin

Role required: admin

### Procedure

1.  Enter `sys_properties.list` in the navigation filter.

2.  Search for the property **glide.history.max\_entries**.

3.  Edit the **Value** of the property.

    |Property|Value|
    |--------|-----|
    |Name|glide.history.max\_entries|
    |Description|Maximum number of entries the system shows in the activity formatter. The default is 250.|
    |Type|Integer|
    |Value|250|

4.  Click **Update**.


**Related topics**  


[Activity formatter](../../form-administration/concept/c_ActivityFormatter.md#)

