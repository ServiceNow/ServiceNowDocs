---
title: Approve or reject a service order for fulfillment
description: Select a service order and review the account, contact, and date details to verify that the order is correct and complete. If you're a service order manager, you can approve or reject a service order with a New state for fulfillment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/telecommunications-media-and-technology-core/approve-reject-service-order-fulfillment.html
release: australia
product: Telecommunications, Media and Technology Core
classification: telecommunications-media-and-technology-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Approve and fulfill service orders, Use, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Approve or reject a service order for fulfillment

Select a service order and review the account, contact, and date details to verify that the order is correct and complete. If you're a service order manager, you can approve or reject a service order with a New state for fulfillment.

## Before you begin

Role required: sn\_ind\_tmt\_orm.service\_order\_manager

## About this task

**Note:** If the following error message appears in the San Diego release or above after approving an order, it indicates that a required upgrade script was not run.

```
Some of the OMT tables need reparenting. Please contact administrator to execute the reparenting script.
```

The Post Upgrade Script performs required order management table reparenting and column promotion. If the script hasn't been run, the order decomposition and order fulfillment functions won't function as designed until your system administrator runs it. To learn more, see [Restructured Order Management tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecommunications-media-and-technology-core/restructured-order-mgt-tables-san-diego.md).

## Procedure

1.  Navigate to **All** &gt; **Service Order Management** &gt; **Workspace** &gt; **Configurable Workspace Home**.

    **Note:** If you aren't using configurable workspaces, navigate by using the following path:

    **Workspace Experience** &gt; **Workspaces** &gt; **Agent Workspace Home**.

    To learn more about migrating to configurable workspaces, see [Migrate to Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/migrate-to-configurable-workspace.md).

    If you have an assigned Service Order Manager or Service Order Agent role, the Service Order Management workspace appears. If the Service Order Management workspace doesn't appear, do the following actions:

    1.  From the Configuration Workspace Lists icon \[Omitted image "list-outline-24.svg"\] Alt text:, click **Service Orders**.
    2.  Do one of the following:

        -   To view all service orders, click **All**.
        -   To view only open, unfulfilled service orders, click **Open**.
        **Note:** To learn more about creating or updating service order details, see [Creating orders in Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/creating-orders-som.md).

    3.  Select the service order that you want to review, verify, and approve:
        -   To refresh the form, click the refresh icon \[Omitted image "form-refresh.png"\] Alt text:.
        -   To filter existing service orders, click the filter icon \[Omitted image "form-filter.png"\] Alt text:.
2.  Select the service order to review by clicking the appropriate tile.

3.  On the Customer Order form, review the order number, account, and contact information for the selected service order.

4.  To approve or reject fulfillment of a service order in a New state, perform one of the following actions.

<table id="choicetable_hrn_21f_5rb"><thead><tr><th align="left" id="d38764e207">

Action

</th><th align="left" id="d38764e210">

Description

</th></tr></thead><tbody><tr><td id="d38764e216">

**Approve a customer or service order for fulfillment**

</td><td>

In the Customer Order form, do the following actions:1.  Click **Approve**.
2.  Click **Save**.
When you approve an order for fulfillment, the following actions take place:

-   The **State** field changes to In Progress.
-   The **Revision Operation** field is set to None.
**Note:** You must have an sn\_ind\_tmt\_orm.order\_fulfillment\_manager role.

</td></tr><tr><td id="d38764e259">

**Reject a customer or service order for fulfillment**

</td><td>

In the Customer Order form, do the following actions:1.  Click **Reject**.
2.  Click **Save**.
When you reject an order for fulfillment, the following actions take place:

-   The **State** field changes to In Rejected.
-   The **Revision Operation** field is set to None.
**Note:** You must have an sn\_ind\_tmt\_orm.order\_fulfillment\_manager role. You can approve an order that you previously rejected.

</td></tr></tbody>
</table>
