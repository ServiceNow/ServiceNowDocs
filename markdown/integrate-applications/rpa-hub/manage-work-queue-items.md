---
title: Manage your work items
description: Manage your work items more efficiently in RPA Hub. You can view your work items, mark them as complete, and reassign a work item.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Managing RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Manage your work items

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

</th><th align="left" id="d221398e125">

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


**Parent Topic:**[Managing RPA Hub](../concept/managing-rpa-hub.md)

**Related topics**  


[Work item form in RPA Hub](../reference/work-queue-form.md)

[Queue implementation in RPA Hub](../concept/queues-implement-rpa.md)

[View Audit History](https://www.servicenow.com/docs/access?context=c_HistorySets&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

