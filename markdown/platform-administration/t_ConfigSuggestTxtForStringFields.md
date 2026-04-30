---
title: Configure suggested text for string fields
description: You can configure the suggested text options for string fields.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Suggestion field type, Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure suggested text for string fields

You can configure the suggested text options for string fields.

## Before you begin

Role required: personalize\_choices

## Procedure

1.  Right-click the field label and select **Configure Choices**.

2.  Using the slushbucket, select options and the order in which you want them to appear.

    -   To create a new option, enter the suggested text in the **Enter new item field** and click **Add**.
    -   The **Apply to Table** field is available when the current table extends another table \(for example, Incident extends Task\). This field allows suggested text options to be configured for all tables that extend the parent or for only the current \(child\) table.
3.  Click **Save**.

4.  To edit existing options, right-click the field label and select **Show Choice List.**.


## Example

![Configure choices](../image/PersonalizeChoices.png)

