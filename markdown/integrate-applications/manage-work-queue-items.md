---
title: Manage your work items in RPA Hub
description: Manage your work items more efficiently in RPA Hub. You can view your work items, mark them as complete, and reassign a work item.Use the Work item form to view more details of the executed work items.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [mark as sensitive data rpa hub]
breadcrumb: [Work items, Use, RPA Hub, Workflow Data Fabric]
---

# Manage your work items in RPA Hub

Manage your work items more efficiently in RPA Hub. You can view your work items, mark them as complete, and reassign a work item.

## Before you begin

Create a queue. For more information, see [Create a queue in RPA Hub](create-queue.md).

Role required: sn\_rpa\_fdn.rpa\_developer, sn\_rpa\_fdn.rpa\_business\_user, sn\_rpa\_fdn.rpa\_support\_user, or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Queues**.

4.  Open the queue to view your work items.

5.  To mark a work item as complete or reassign a work item, select the appropriate action on the **Work Items** tab.

<table id="choicetable_lz1_3dx_2rb"><thead><tr><th align="left" id="choptionhd_xxv_hdx_2rb">

Option

</th><th align="left" id="d474012e137">

Action

</th></tr></thead><tbody><tr><td id="choption_yxv_hdx_2rb">

**To mark a work item as complete**

</td><td>

1.  From the list, select one or more work items.
2.  In the form header, select **Mark as Complete**.
3.  Enter a comment for marking the work item as complete.
4.  Select **Mark as Complete**.
The status of the work item changes to `Success`.

</td></tr><tr><td id="choption_zxv_hdx_2rb">

**To reassign a work item**

</td><td>

1.  From the list, select one or more work items.
2.  In the form header, select **Reassign**.
3.  Enter a comment for reassigning the work item.
4.  Select **Reassign**.
 The status of the work item changes to `Pending`.You can reassign a work item that is in In Progress, Pending, Failed, or Success state. Upon reassigning, the values of the following fields on the Work Item form are reset to:

-   **Started On**- &lt;empty&gt;
-   **Completed On**- &lt;empty&gt;
-   **Robot**- &lt;empty&gt;
-   **Last Started Time**- &lt;empty&gt;
-   **Attempts Count**- 0
-   **Exception Type**- &lt;empty&gt;
-   **Status**- Pending
-   **Remarks**- &lt;from the modal&gt;
Roles required to reassign a failed or a success work item: RPA developer, RPA release manager, and RPA admin.

</td></tr></tbody>
</table>6.  On the **Work Items** tab, open a work item to view the details on the form.

7.  In the **Activity** and **Compose** fields, view the activity of the form, work notes, and additional comments.


**Parent Topic:**[Work items in RPA Hub](../concept/work-items-rpa-hub.md)

**Related topics**  


[Queue implementation in RPA Hub](../concept/queues-implement-rpa.md)

[View Audit History](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_HistorySets.md)

## Work item form in RPA Hub

Use the Work item form to view more details of the executed work items.

<table id="table_g5y_gbx_2rb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the work item.

</td></tr><tr><td>

Work Queue

</td><td>

Name of the queue.

</td></tr><tr><td>

Status

</td><td>

Status of the work item.

</td></tr><tr><td>

Exception Type

</td><td>

Type of the exception:-   **Application** - For example, if an issue persists with an associated application such as SAP.
-   **Business** - For example, if an issue requires a manual intervention to fix it.

 The auto retry functionality retries the work items based on the exception type.

 If the **Exception Type** field is **Application**, then the work item is auto retried.

 Roles required to edit this field: RPA robot.

</td></tr><tr><td>

Started On

</td><td>

Start date and time of the work item.

</td></tr><tr><td>

Completed On

</td><td>

Completion date and time of the work item.

</td></tr><tr><td>

Attempts Count

</td><td>

Number of times the work item is picked for auto retry.The minimum value is 0.

</td></tr><tr><td class="sub-head" colspan="2">

Details

</td></tr><tr><td>

Priority

</td><td>

Priority of the work item:-   **Critical**
-   **High**
-   **Medium**
-   **Low**

The assigned robot executes the bot process as per the defined priority in the work queue.

</td></tr><tr><td>

Type

</td><td>

String field to define the type of work item.

</td></tr><tr><td>

Stage

</td><td>

Custom field for the robot to maintain different stages of the transaction.

</td></tr><tr><td>

SLA

</td><td>

Time and date that the SLA was started.

</td></tr><tr><td>

Robot

</td><td>

Name of the robot that is assigned to the work queue.

</td></tr><tr><td>

Created

</td><td>

Creation date and time of the work item.

</td></tr><tr><td>

Last Started Time

</td><td>

Last start time of the work item.

</td></tr><tr><td>

Deferred Till

</td><td>

Work item that is not picked until the specified date and time.

</td></tr><tr><td>

Completed By

</td><td>

Name of the robot who has completed the work item.

</td></tr><tr><td>

Remarks

</td><td>

Remarks updated by the robot runtimes.

</td></tr><tr><td class="sub-head" colspan="2">

Content

</td></tr><tr><td>

Request Content

</td><td>

Non sensitive content which is displayed in plain text in the Work Item form and can be used for work item processing.

</td></tr><tr><td>

Sensitive Request Content

</td><td>

Sensitive request content which is encrypted and masked in the Work Item form and can be used for work item processing.When the work item is picked, the sensitive data is decrypted and passed to the RPA Desktop Design Studio or robots.

With this option, you can pass sensitive information through queues. For example, credit card details are encrypted.

</td></tr><tr><td>

Response Content

</td><td>

Content that is added or updated when a work item is picked after the transaction.

</td></tr><tr><td class="sub-head" colspan="2">

Transaction Activity

</td></tr><tr><td>

Work notes

</td><td>

Work notes for the work item.

</td></tr><tr><td>

Additional Comments

</td><td>

Comments for updating this work item.

</td></tr><tr><td>

Activity

</td><td>

Transaction logs for the selected work item.

</td></tr></tbody>
</table>**Related topics**  


[Queue form in RPA Hub](../reference/queue-form.md)

[Using auto-retry functionality for your failed work items in RPA Hub](../concept/auto-retry-wqi-rpa.md)

[Queue implementation in RPA Hub](../concept/queues-implement-rpa.md)

