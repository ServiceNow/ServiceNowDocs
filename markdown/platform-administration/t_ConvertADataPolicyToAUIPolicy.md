---
title: Convert a data policy to a UI policy
description: Convert a data policy to a UI policy if a data policy already exists but needs to apply only to records created or updated in the browser.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data policy, Administering fields, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Convert a data policy to a UI policy

Convert a data policy to a UI policy if a data policy already exists but needs to apply only to records created or updated in the browser.

## Before you begin

Role required: admin

## About this task

Converting deactivates the data policy. The new UI policy is applied only at the UI layer only and not to import sets or data imported from SOAP web services.

**Note:** An alternative to converting from a data policy to a UI policy is to select the **Use as UI Policy on client** checkbox on the data policy record. This field extends the data policy to the UI. The main difference between converting and using the **Use as UI Policy on client** checkbox is that converting provides the Visible field on the UI policy record. Use the **Visible** field to select how the UI policy affects the visible state of the field.

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Rules** &gt; **Data Policies** and click an existing data policy.

2.  Under **Related Links**, click **Convert this to UI Policy**.

    A new UI policy record appears.

3.  Edit the fields on the UI policy record as necessary.

    For details about the fields, see [Create a UI Policy](../../form-administration/task/t_CreateAUIPolicy.md#).


