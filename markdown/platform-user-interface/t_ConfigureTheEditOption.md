---
title: Configure the edit option
description: You can configure the edit option that allows users to add records to related lists in forms.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Related lists, Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Configure the edit option

You can configure the edit option that allows users to add records to related lists in forms.

## Before you begin

Role required: admin

## About this task

The **Edit** button is available for related lists that represent many-to-many and one-to-many relationships. Defined related lists may not have an **Edit** button, as related records are added to these lists automatically based on the relationship between the records.

## Procedure

1.  Navigate to the related list, such as the **Incidents** related list on a problem record.

2.  Perform the appropriate action for the list version.

    |Version|Action|
    |-------|------|
    |**List v2**|Right-click any column heading and select **Configure** &gt; **List Control**.|
    |**List v3**|Open the list title menu and select **List Control**.|

3.  Perform one of the following actions.

<table id="choicetable_qwf_wjx_5t"><tbody><tr><td id="d107450e126">

**Show the Edit option**

</td><td>

Clear the **Omit edit button** check box.

</td></tr><tr><td id="d107450e138">

**Hide the Edit option**

</td><td>

Select the **Omit edit button** check box.

</td></tr><tr><td id="d107450e150">

**Show the Edit option if the check box is cleared and the button does not appear.**

</td><td>

Click **Enable Edit**.

</td></tr></tbody>
</table>4.  If the list represents a one-to-many relationship \(example, incidents can be associated with only one problem, but problems can be associated with many incidents\), complete the following steps.

    1.  Open a record in the target table \(example, Incident\).

    2.  Right-click the header and select **Configure** &gt; **Dictionary**.

    3.  Open the dictionary entry for the reference field \(example, **Problem ID** on **Incident**\).

    4.  In the Reference Specification section, select the **Reference floats** check box.

        ![Reference floats check box](../image/ReferenceFloatsBox.png)

5.  Click **Update**.


**Parent Topic:**[Related lists](../concept/c_RelatedLists.md)

**Related topics**  


[Select or create records in a related list](t_SelectRelatedRecords.md)

[Configure when a related list loads](t_ConfigureWhenARelatedListLoads.md)

[Create a default filter for a related list](t_CreateADefaultFilter.md)

[Create defined related lists](../../../administer/form-administration/task/t_CreateDefinedRelatedLists.md)

[Add fields to selections in a related list](../../../administer/form-administration/task/t_AddingFieldsToARelatedList.md)

[Create a default filter for list selector records](../../../administer/form-administration/task/t_CreateDefaultRelatedRecSecFilter.md)

