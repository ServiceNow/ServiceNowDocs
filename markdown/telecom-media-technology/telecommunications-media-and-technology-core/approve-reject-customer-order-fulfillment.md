---
title: Approve or reject a customer order for fulfillment
description: Select a customer order, and review the account, contact, pricing, and date details to make sure that the order is correct and complete. If you're an order fulfillment manager, can approve or reject a customer order with a New state for fulfillment.OM revamp project - This topic is obsolete and has been removed from the SOM bundle on Oct 6, 2025. The content has been covered in the new approve/reject topics.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/telecommunications-media-and-technology-core/approve-reject-customer-order-fulfillment.html
release: australia
product: Telecommunications, Media and Technology Core
classification: telecommunications-media-and-technology-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customer orders, Use, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Approve or reject a customer order for fulfillment

Select a customer order, and review the account, contact, pricing, and date details to make sure that the order is correct and complete. If you're an order fulfillment manager, can approve or reject a customer order with a New state for fulfillment.

## Before you begin

Role required: sn\_ind\_tmt\_orm.order\_fulfillment\_manager

## About this task

**Note:** If the following error message appears in the San Diego release or above after approving an order, it indicates that a required upgrade script was not run.

```
Some of the OMT tables need reparenting. Please contact administrator to execute the reparenting script.
```

The Post Upgrade Script performs required order management table reparenting and column promotion. If the script hasn't been run, the order decomposition and order fulfillment functions won't function as designed until your system administrator runs it. To learn more, see [Restructured Order Management tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecommunications-media-and-technology-core/restructured-order-mgt-tables-san-diego.md).

## Procedure

1.  Navigate to **All** &gt; **Customer Order Management** &gt; **Workspace** &gt; **Configurable Workspace Home**.

    **Note:** If you aren't currently using configurable workspaces, navigate by using the following path:

    **Workspace Experience** &gt; **Workspaces** &gt; **Agent Workspace Home**.

    To learn more about migrating to configurable workspaces, see [Migrate to Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/migrate-to-configurable-workspace.md).

    If you have an assigned order fulfillment manager or order fulfillment agent role, the Customer Order Management workspace appears. If the Customer Order Management workspace doesn't appear, do the following actions:

    1.  From the Configurable Workspace Lists icon \[Omitted image "list-outline-24.svg"\] Alt text:, click **Customer Orders**.
    2.  Do one of the following actions:
        -   To view all customer orders, click **All**.
        -   To view only open, unfulfilled customer orders, click **Open**.
    3.  Select the customer order that you want to review, verify, approve, or fulfill:
        -   To refresh the form, click the refresh icon \[Omitted image "form-refresh.png"\] Alt text:.
        -   To filter existing customer orders, click the filter icon \[Omitted image "form-filter.png"\] Alt text:.
2.  To select the customer order that you want to review, click the appropriate tile in the Customer Order Management workspace.

3.  On the Customer Order form, review the order number, account, and contact information for the selected customer order.

    For information about the field descriptions, see the Customer Orders form fields section in [Customer and Service order details forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/field-descriptions-customer-orders.md).

4.  To approve or reject fulfillment of a customer order in a New state, perform one of the following actions.

<table id="choicetable_opd_p3f_5rb"><thead><tr><th align="left" id="d23973e212">

Action

</th><th align="left" id="d23973e215">

Description

</th></tr></thead><tbody><tr><td id="d23973e221">

**Approve a customer or service order for fulfillment**

</td><td>

In the Customer Order form, do the following actions:1.  Click **Approve**.
2.  Click **Save**.
When you approve an order for fulfillment, the following actions take place:

-   The **State** field changes to In Progress.
-   The **Revision Operation** field is set to None.
**Note:** You must have an sn\_ind\_tmt\_orm.order\_fulfillment\_manager role.

</td></tr><tr><td id="d23973e264">

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
