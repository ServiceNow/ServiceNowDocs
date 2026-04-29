---
title: Configure ability to copy a change request
description: You can configure the ability to copy a change request record and its details using system properties.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Change Management, IT Service Management]
---

# Configure ability to copy a change request

You can configure the ability to copy a change request record and its details using system properties.

## Before you begin

Role required: admin

## About this task

You can configure the following functionality.

-   Disable the ability to copy a change request.
-   Disable the ability to copy attachments.
-   Determine the components of the source change request that are copied.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Administration** &gt; **Change Properties**.

    Some properties are found by entering `sys_properties.list` in the application navigator, as noted.

2.  Set the following properties as desired.

<table id="choicetable_q1v_qzc_nw"><tbody><tr><td id="d71587e92">

**Disable the ability to copy a change request**

</td><td>

Set **Enable Copy Change feature** \(**com.snc.change\_request.enable\_copy**\) to `false`.

</td></tr><tr><td id="d71587e110">

**Disable the ability to copy an attachment**

</td><td>

Set **Copy attachments from originating change** \(**com.snc.change\_request.attach.enable\_copy**\) to `false`.

</td></tr><tr><td id="d71587e131">

**Disable the ability to copy the attachments from the change task**

</td><td>

This system property is located in the \[sys\_properties\] table.Set the **Enable copying of attachments from the originating change's related change tasks** \(**com.snc.change\_request.rl.change\_task.attach.enable\_copy**\) system property to `false`.

 **Note:** If the ability to copy attachments is enabled, the attachment appears on the copy of the change request only after it is saved.

</td></tr><tr><td id="d71587e155">

**Configure attributes to be copied**

</td><td>

Edit the list of values in **List of attributes \(comma-separated\) that will be copied from the originating change** \(**com.snc.change\_request.copy.attributes**\) to remove or add more attributes. For example, to prevent the **Assigned to** attribute from being copied, remove the `assigned_to` value from the list of attributes in the property text box.

</td></tr><tr><td id="d71587e179">

**Configure related lists to be copied**

</td><td>

This system property is located in the \[sys\_properties\] table. The following related lists are copied by default:-   **Affected CIs**
-   **Impacted Services/CIs**
-   **Change Tasks**
 Edit the list of values in **Related lists \(comma-separated\) that will be copied from the originating change** \(**com.snc.change\_request.copy.related\_lists**\).

 For example, if you do not want to copy the **Change Tasks** related list, remove the `change_task` value from the list of related lists in the property text box.

 **Note:** You can configure this property to control the copy functionality of the **Affected CIs**, **Impacted Services/CIs**, and **Change Tasks** related lists. You cannot add any other related list to this property.

</td></tr><tr><td id="d71587e234">

**Configure attributes of the default related lists to be copied**

</td><td>

These system properties are located in the \[sys\_properties\] table. Navigate to the appropriate system property for one of the default related lists to configure the attributes to copy. |Related list|System property|
|------------|---------------|
|Change Tasks|**com.snc.change\_request.copy.rl.change\_task.attributes**|
|Affected CIs|**com.snc.change\_request.copy.rl.task\_ci.attributes**|
|Impacted Services/CIs|**com.snc.change\_request.copy.rl.task\_cmdb\_ci\_service.attributes**|

</td></tr></tbody>
</table>3.  Complete the following steps to further customize the ability to copy a change request by modifying a script include.

    1.  Navigate to **System Definition** &gt; **Script Includes**.

    2.  Modify the ChangeUtils script include.

        For example, the ability to copy a change request is not available by default for standard changes. However, you can provide your own implementation of the isCopyRulesValid function in the ChangeUtils script include to override the default.


**Parent Topic:**[Configuring Change Management](../concept/configure-change-management.md)

**Related topics**  


[Copy a change request](copy-a-change-request.md)

