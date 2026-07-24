---
title: Create Return Merchandise Authorization case lines
description: Create return merchandise authorization case lines directly from install base items or sold product entities to manage the full post-sale life cycle of products sold to customers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/create-return-merchandise-authorization-case-lines.html
release: australia
topic_type: task
last_updated: "2026-07-09"
reading_time_minutes: 1
breadcrumb: [Order operations apps, Configure, Sales Customer Relationship Management]
---

# Create Return Merchandise Authorization case lines

Create return merchandise authorization case lines directly from install base items or sold product entities to manage the full post-sale life cycle of products sold to customers.

## Before you begin

Role required: sn\_csm\_rma\_case.csm\_rma\_case\_agent

## Procedure

1.  Navigate to the CSM/FSM Configurable Workspace.

2.  From the list, navigate to **RMA cases** and select **All** to open the list of cases.

3.  Open an RMA case.

4.  On the form, fill in the fields.

    To learn more about the fields on the form, see [RMA case line form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/rma-case-line-form.md).

5.  Select **Save and Continue**.

6.  In the **Add and edit items** window, select **Add** to add an install base item or a sold product as a line item.

7.  Select **Add**, exit the pop-up and select **Save and submit**.

8.  In the **Review entitlements** window, add any entitlements and select **Verify and continue**.

9.  In the **Propose issue solution** screen, select the case line that you're working on and select **Edit**.

    -   Based on the requirement, select **Refund**, **Replacement**, **Reject**, or **Repair** as a proposed resolution.
    -   Update the state of the case to **Draft**, **New**, **Work in progress**, **Awaiting info**, **Awaiting shipment**, **Resolved-Accepted**, **Resolved- Denied**, **Closed**, or **Canceled**. At this stage, you can move forward only if the case is set to work in progress.
10. In the **Resolve issues** window, edit the proposed resolution and state of the case and select **Save and continue**.

    **Note:** The resolution code for all case lines must be in either the **Resolved - Accepted**, **Resolved - Denied**, or the **Canceled** state.

11. In the **Propose case solution** window, add the resolution code and the resolution notes.

12. Select **Save and continue**.


**Related topics**  


[RMA case line form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/rma-case-line-form.md)

