---
title: Preserve your custom Next Experience theme during a clone
description: Preserve your custom Next Experience theme during a clone by using a data preserver.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Next Experience themes, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Preserve your custom Next Experience theme during a clone

Preserve your custom Next Experience theme during a clone by using a data preserver.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Clone** &gt; **Clone Definition** &gt; **Preserve Data**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name for your data preserver. An example is Next Experience Theme Properties.|
    |Theme|Option to determine whether this preserver is theme-related. In this case, select the option to mark it as true.|
    |Table|Table that is affected by this data preserver. In this case, use **System property \[sys\_properties\]**.|
    |Conditions|Conditions that this data preserver acts on. Build the condition as **Name is glide.ui.polaris.theme.custom**.|

4.  Right-click the header and select **Save**.

    The Clone Profiles related list appears.

5.  Create a new record for each of the following tables, and leave the condition field empty.

    -   **sys\_ux\_theme**
    -   **sys\_ux\_style**
    -   **m2m\_theme\_style**
    -   **m2m\_style\_asset**
    -   **sys\_ux\_theme\_asset**
    -   **sys\_ux\_theme\_m2m\_asset**
    -   **sys\_ux\_theme\_customization**
    -   **m2m\_app\_theme**
6.  Create a new record for each of the table, including the associated condition.

    |Table|Conditions|
    |-----|----------|
    |**sys\_properties**|**Name is glide.ui.polaris.theme\_builder.override\_logo**.|
    |**sys\_user\_preference**|**Name is glide.ui.polaris.theme**.|
    |**sys\_user\_preference**|**Name is glide.ui.polaris.theme.variant**.|
    |Add this table for themes with custom logos: **sys\_attachment**|Name or unique identifier of the sys\_attachment record on the target.|

7.  If you have a clone profile you would like to add, select **Edit**, move your clone profile to your data preserver, and select **Save**.

    **Note:** A clone profile enables you to store predefined target and clone options. If you don’t have a clone profile, or don’t need one, skip this step.


**Parent Topic:**[Configuring Next Experience themes and preferences](config-next-experience-themes-prefs.md)

