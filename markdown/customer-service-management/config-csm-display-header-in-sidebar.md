---
title: Display the form ribbon and form header secondary values in the Contextual side panel
description: Configure the form ribbon and the secondary values that appear in a form header to display in the Contextual side panel in CSM Configurable Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-18"
reading_time_minutes: 2
breadcrumb: [Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Display the form ribbon and form header secondary values in the Contextual side panel

Configure the form ribbon and the secondary values that appear in a form header to display in the Contextual side panel in CSM Configurable Workspace.

## Before you begin

Role required: workspace\_admin, ui\_builder\_admin, admin

## About this task

**Note:** This task applies to CSM Configurable Workspace.

The form ribbon includes components that provide agents with an overview of case details, such as a customer summary and a case timeline.

The form header for the Case form can display two levels of field values from the Case table. The primary value is the case short description. The secondary values include the account and contact or consumer, the case priority, and the case state.

You can use properties to determine where the form ribbon and secondary values are displayed: at the top of the record or in the Contextual side panel. Two properties are available for the standard record page and two are available for the interaction record.

These properties can operate independently. For example, you can display the form ribbon in the Contextual side panel and the secondary values in the form header.

**Note:** The form ribbon properties apply to pages that have active ribbon configurations. If a page does not have a ribbon configuration, or has an inactive ribbon configuration, there is no information for the system to display in either location.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Experiences** &gt; **CSM/FSM Configurable Workspace**.

2.  In the UX Page Properties list, select the desired property.

    |Property|Description|
    |--------|-----------|
    |**ribbonLocation**|Controls where to display the form ribbon on a standard record page: header or sidebar. For example, the Case record page. Default is sidebar.|
    |**record\_secondary\_values\_location**|Controls where to display the form header secondary field values on a standard record page: header or sidebar. For example, the Case record page. Default is sidebar.|
    |**ribbonLocation\_interaction**|Controls where to display the form ribbon on an interaction record: header or sidebar. Default is sidebar.|
    |**interaction\_secondary\_values\_location**|Controls where to display the form header secondary field values on an interaction record: header or sidebar. Default is sidebar.|

3.  In the **Value** field for the selected property, enter one of the following values.

<table id="choicetable_rz1_21k_npb"><thead><tr><th align="left" id="d55497e168">

Value

</th><th align="left" id="d55497e171">

Description

</th></tr></thead><tbody><tr><td id="d55497e177">

**header**

</td><td>

Displays the selected component in the following location: -   Ribbon: at the top of the record.
-   Secondary values: at the top of the record, in the form header below the primary value.


</td></tr><tr><td id="d55497e194">

**sidebar**

</td><td>

Displays the selected component in the Contextual side panel.

</td></tr></tbody>
</table>4.  Select **Update**.


