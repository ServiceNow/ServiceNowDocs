---
title: Enable granular integration for automations
description: Enable granular integration for automations to capture cost saved and time saved at the transaction level. This feature makes the total cost-saved and total time-saved data analysis effective.
locale: en-US
release: zurich
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with automations, Use, Automation Center, Workflow Data Fabric]
---

# Enable granular integration for automations

Enable granular integration for automations to capture cost saved and time saved at the transaction level. This feature makes the total cost-saved and total time-saved data analysis effective.

## Before you begin

Role required: sn\_ac.automation\_business\_user, sn\_ac.automation\_technical\_user, or sn\_ac.automation\_admin.

**Important:** This feature is available only for those automations that have ServiceNow® Robotic Process Automation version 10.0.0 and later.

## Procedure

1.  Navigate to **All** &gt; **Automation Center** &gt; **Automation Center Home**.

2.  Select the list icon \(![List icon.](../images/autocenter-list-icon.png)\).

3.  On the **Lists** tab, under **Administration**, select **Automation Attributes**.

4.  Select the link on the **Class** column for an automation with the source name as **ServiceNow RPA**.

    The details section is displayed.

5.  From the ellipses on the right top, select **Enable Granular Integration**.

    ![Enable granular integration](../images/granular-intg.png)

    A confirmation message is displayed.

6.  Select **Enable Granular Integration** on the confirmation window.

    You’re automatically taken to the **Granular Integration** tab.

7.  Select **Add queues**.

    A window is displayed enabling you to add queues.

    ![Add queues](../images/add-queues.png)

8.  Provide the details.

<table id="id_f43_dfr_bcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

RPA Work Queue

</td><td>

Select a queue from the list.If you don’t see any queue in the list, you must add queues to the Bot Process.

1.  Navigate to **All** &gt; **Automation center** &gt; **Monitor** &gt; **All Bot Processes**.

2.  Select the automation for which you’re enabling the granular integration.

3.  Add queues from the **Related Links** section.

</td></tr><tr><td>

Cost saved per item

</td><td>

Specify the cost that is saved per work item.

</td></tr><tr><td>

Time saved per item

</td><td>

Specify the time that is saved per work item.

</td></tr></tbody>
</table>9.  Select **Add queues** to add multiple queues.

10. Select **Map queues**.

    The queues are mapped for the automation and the granular integration is enabled. From the next execution after 24 hours, the data is displayed in the **Active automations** widget in the **Overview** dashboard. Granular data ensures that the cost-saved and time-saved data is displayed at item level making it more accurate.

    The data of the granular integration can be seen in the Automation Transaction Summary table.

11. Select – beside a row to delete the mapped queue.

    **Note:** You can’t delete the first queue that you have mapped.

12. To disable granular integration, from the ellipses on the right top, select **Disable Granular Integration**.

    The queue remains, however, granular data integration isn’t used to calculate the time and cost saved.


**Parent Topic:**[Working with automations](../concept/automations.md)

