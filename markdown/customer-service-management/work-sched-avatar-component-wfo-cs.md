---
title: Configure an avatar component for Work scheduler
description: Use the Container component to add an avatar and the user name of the work item assignee.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/work-sched-avatar-component-wfo-cs.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a Work scheduler card using the Next Experience UI Builder, Setting up Work scheduler, Optimize workforce operations, Extend capabilities, Configure, Customer Service Management]
---

# Configure an avatar component for Work scheduler

Use the **Container** component to add an avatar and the user name of the work item assignee.

## Before you begin

Role required: admin, workspace\_admin, or ui\_builder\_admin​

## Procedure

1.  In the **Content** section, navigate to **Body\(Flex\)** &gt; **Card Base Container \(Flex\)** &gt; **Card Base Header**.

2.  Right-click **Card Base Header** and select **Add component after**.

3.  In the pop-up screen, select the **Label value stacked** component.

4.  In the left pane, right-click **Label value stacked** and select **Add component after**.

5.  Configure the component.

    1.  In the **Components** pop-up screen, select **Container**.

    2.  In the **Config** tab, do the following:

        1.  Select the Edit component visibility icon \(\[Omitted image "edit-comp-visibility-icon.png"\] Alt text: Edit component visibility icon\).
        2.  Hover over the **Hide component** field and select the Dynamic data binding icon \[Omitted image "dynamic-data-binding-icon.png"\] Alt text: Dynamic data binding icon.
        3.  In the **Hide component** field, enter `!@state.cardProps.assignedTo`
        4.  In the **Direction** menu, select **Row**.
        5.  In the **Styles** tab, in the **Align items** field, select the center icon.
        6.  Select **Save**.
6.  To add the Avatar component, select **Container\(Flex\)** &gt; **+Add component**.

7.  Select **+Add component**

    The Components pop-up screen appears.

<table id="choicetable_jbw_3mm_ntb"><thead><tr><th align="left" id="d110883e220">

To

</th><th align="left" id="d110883e223">

Do this

</th></tr></thead><tbody><tr><td id="d110883e229">

**Add the Avatar component**

</td><td>

In the configure tab, set the size, user name, and tooltip.1.  In the **Size** menu, select **Medium**.
2.  Hover over the **User name** menu, and select the Dynamic data binding icon \[Omitted image "dynamic-data-binding-icon.png"\] Alt text: Dynamic data binding icon.
3.  In the **User name** menu, type **!@state.cardProps.assignedTo**.
4.  Hover over the **Tooltip text** menu, and select the Dynamic data binding icon \[Omitted image "dynamic-data-binding-icon.png"\] Alt text: Dynamic data binding icon.
5.  In the **Tooltip text** menu, type **!@state.cardProps.assignedTo**.


</td></tr><tr><td id="d110883e292">

**Add the Label Value Tabbed component**

</td><td>

In the configure tab, set the size, and items.1.  In the **Size** menu, select **Small**.
2.  Hover over the **Items** field and select the Dynamic data binding icon \[Omitted image "dynamic-data-binding-icon.png"\] Alt text: Dynamic data binding icon.
3.  In the Items field, enter `[{value: @state.cardProps.assignedTo}`
4.  Select **Save**.


</td></tr></tbody>
</table>    Here's a demo on how to configure an avatar component for Work scheduler


**Parent Topic:**[Create a Work scheduler card using the Next Experience UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/create-workscheduler-card-wfo-cs.md)

