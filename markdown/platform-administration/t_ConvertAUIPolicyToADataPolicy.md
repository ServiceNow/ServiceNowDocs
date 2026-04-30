---
title: Convert a UI policy to a data policy
description: To make a UI policy the default setting, convert the UI policy to a data policy.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data policy, Administering fields, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Convert a UI policy to a data policy

To make a UI policy the default setting, convert the UI policy to a data policy.

## Before you begin

Role required: ui\_policy\_admin

## About this task

You can also apply a UI policy to import sets or to data imported by SOAP web services when you convert it to a data policy. Converting a UI policy to a data policy deactivates the UI policy. To retain the policy in the UI, ensure that the **Use as UI Policy on client** check box is selected on the data policy record.

For a UI policy to be eligible for conversion to a data policy, the following conditions must be met on the UI Policy form.

-   The **Run scripts** check box must be cleared.
-   The **Global** check box must be selected.
-   None of the UI policy actions can have **Visible** set to **True** or set to **False**. **Visible** must be set to **Leave Alone**.

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **UI Policies**.

2.  Open an existing UI policy.

3.  Under **Related Links**, click **Convert this to Data Policy**.

    A new data policy record is created.

4.  Edit the fields on the data policy record as necessary.


**Related topics**  


[Data policy](../../field-administration/concept/c_DataPolicy.md)

