---
title: Define event mappings for Work scheduler
description: Add event mappings required for card interactions and for the card properties transformation to the page configurations in Work scheduler.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/work-sched-event-mapping-wfo-cs.html
release: zurich
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a Work scheduler card using the Next Experience UI Builder, Setting up Work scheduler, Optimize workforce operations, Extend capabilities, Configure, Customer Service Management]
---

# Define event mappings for Work scheduler

Add event mappings required for card interactions and for the card properties transformation to the page configurations in Work scheduler.

## Before you begin

Role required: admin, workspace\_admin, or ui\_builder\_admin​

## Procedure

1.  In the **Page configuration** section, select the **Events** tab.

2.  Attach the **Transform workItem to cardProps** to the **Page ready** event.

    1.  In the **Page ready** menu, select **+Add a new event handler**.

    2.  In the pop-up screen, go the Scripts section and select **Transform workItem to cardProps**.

    3.  Select **Add**.

3.  Attach the **Transform workItem to cardProps** to the **Page ready** event.

    1.  In the **Page ready** menu, select **+Add a new event handler**.

    2.  In the pop-up screen, go the Scripts section and select **Transform workItem to cardProps**.

    3.  Select **Add**.

4.  Attach the **Transform workItem to cardProps** to the **Page property changed** event.

    1.  In the **Page property changed** menu, select **+Add a new event handler**.

    2.  In the pop-up screen, go the Scripts section and select **Transform workItem to cardProps**.

    3.  Select **Add**.

5.  Attach the **CARD\_CLICKED** and **CARD\_CLICKED \(Work item cards\)** events.

    The **Create an event** popup screen displays.

<table id="choicetable_c2r_hgm_ntb"><thead><tr><th align="left" id="d237991e216">

To Attach

</th><th align="left" id="d237991e219">

Do this

</th></tr></thead><tbody><tr><td id="d237991e225">

**The __CARD\_CLICKED__ event**

</td><td>

1.  In the **Dispatched events** section, select **+Add**.
2.  In the **Event label** field, enter **CARD\_CLICKED**.
3.  From the **Target parent event handler** menu, select **CARD\_CLICKED \(Work item cards\)**
4.  Click **Add**.


</td></tr><tr><td id="d237991e272">

**The __CARD\_ACTION\_CLICKED \(Work item cards\)__ event**

</td><td>

1.  In the **Dispatched events** section, select **+Add**.
2.  In the **Event label** field, enter **CARD\_ACTION\_CLICKED**.
3.  From the **Target parent event handler** menu, select **CARD\_ACTION\_CLICKED \(Work item cards\)**
4.  Click **Add**.


</td></tr></tbody>
</table>    Here's a demo on how to define event mappings for the Work scheduler.


## What to do next

[Configure container components for Work scheduler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/workforce-optimization-for-it-service-management/work-sched-card-based-container.md)

**Parent Topic:**[Create a Work scheduler card using the Next Experience UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/create-workscheduler-card-wfo-cs.md)

**Related topics**  


[Events in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/ui-builder/work-events.md)

