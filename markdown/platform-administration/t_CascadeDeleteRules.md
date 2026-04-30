---
title: Configure cascade delete rules
description: When a record is deleted, there are different options for how the deletion will affect records that reference the deleted record. You can configure what happens to records that reference a record when that record is deleted.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Add a reference field, Reference field type, Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure cascade delete rules

When a record is deleted, there are different options for how the deletion will affect records that reference the deleted record. You can configure what happens to records that reference a record when that record is deleted.

## Before you begin

Role required: personalize\_dictionary

## About this task

For example, if you delete a user record that is referenced in the **Caller ID** field on several incident records, you can configure what happens to those incident records. By default, the references are cleared, so the incident records are maintained with an empty **Caller ID** field.

## Procedure

1.  Navigate to a reference field on a form.

2.  Right-click the field label and select **Configure Dictionary**.

3.  Under **Related Links**, click **Advanced view**.

4.  Locate the Reference Specification section.

5.  In the **Reference cascade rule** field, select one of the following options.

    **Note:** The option for this field have no effect for tables with m2m relationships, meaning that in this example, if the tables have an m2m relationship, the user record is deleted.

<table id="choicetable_vwv_kpx_rt"><thead><tr><th align="left" id="d365340e117">

Option

</th><th align="left" id="d365340e120">

Description

</th></tr></thead><tbody><tr><td id="d365340e126">

**__Clear__ or __-- None --__**

</td><td>

Deleting a record clears references \(default option\).

</td></tr><tr><td id="d365340e141">

**__Delete__ or __Cascade__**

</td><td>

Deleting a record also deletes all referencing records. For example, when a user record is deleted, any incidents assigned to the user are also deleted. **Caution:**

Use this method with caution.

</td></tr><tr><td id="d365340e159">

**__Restrict__**

</td><td>

Deleting a record is restricted unless there are no references to the record. For example, prevent the user record from being deleted if any incident includes a reference to the user.

</td></tr><tr><td id="d365340e171">

**__None__**

</td><td>

Deleting a record does not change records that reference the record.

</td></tr></tbody>
</table>6.  Click **Update**.


**Related topics**  


[Modify dictionary entries](../../data-dictionary-tables/task/t_ModifyADictionaryEntryFromAForm.md)

