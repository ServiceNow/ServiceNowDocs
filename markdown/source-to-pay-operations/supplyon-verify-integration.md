---
title: Verify the SupplyOn integration
description: Run a purchase order end to end to confirm the SupplyOn integration is configured correctly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/source-to-pay-operations/supplyon-verify-integration.html
release: australia
topic_type: task
last_updated: "2026-10-08"
reading_time_minutes: 3
breadcrumb: [Configuring the Supplyon integration, Purchase Order Management integration with SupplyOn, Integrate with Purchase Order Management, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Verify the SupplyOn integration

Run a purchase order end to end to confirm the SupplyOn integration is configured correctly.

## Before you begin

Role required: procurement\_user or admin.

## About this task

Each step in this procedure produces a visible system response. If a step does not produce the expected response, the integration is not configured correctly at that stage.

**Note:** Creating the purchase order \(the shopping hub and requisition steps\) is standard Source-to-Pay processing and a prerequisite for the integration, not part of it.

## Procedure

1.  Create and dispatch a purchase order
2.  On the Shopping Hub page, add the item to the cart — for example, quantity 50 —, proceed to checkout, and complete the checkout.

    The order is submitted, but it is not yet a purchase order.

3.  In the Source-to-Pay workspace, open the order requisition that is created.

4.  On the purchase lines, set the CapEx account and the expense account, and set the ERP integration to the order cost center.

    Save the lines.

5.  Open the requisition case, assign it to yourself, and start work.

    Review and populate any missing GL account information, then complete the case and close it.

6.  On the order, select **Create purchase order**.

    Creating the purchase order creates the purchase order record, and a flow then processes it and writes an outbound order record. At that point the integration takes over: it maps the purchase order header and lines and posts them to SupplyOn. SupplyOn does not validate the order synchronously. It returns a transaction ID, and shortly after, it posts the processing outcome back to the instance. The outbound order stays **In process** until the outcome returns or the 24-hour timeout elapses.

    This step also applies to the ServiceNow® purchase order.

7.  Watch the outbound send and async callback
8.  Open the outbound order \(the Outbound Purchase Order \[sn\_spend\_intg\_outbound\_purchase\_order\] table\) and refresh.

    The row is **In process** and shows the transaction number.

9.  Refresh again after a moment.

    The row is **Processed**, and the processing message records that SupplyOn posted back with async status OK.

10. Confirm the outbound order in SupplyOn
11. In the SupplyOn portal, refresh the order list.

    A new purchase order appears with the same number as the ServiceNow® purchase order.

    **Note:** SupplyOn does not assign its own order identifier. It reuses the ServiceNow® purchase order number, and each line is identified by a position ID derived from the ServiceNow® purchase order line number. The POL prefix is omitted because of length limits.

12. Enter a supplier confirmation in SupplyOn
13. Open the purchase order line and confirm the quantity, date, and price.

    **Note:** On the SupplyOn side, purchase orders are confirmed line by line, not in bulk. This is why confirmations are pulled per line on the ServiceNow® side.

14. To confirm partial deliveries, select split delivery and enter each delivery schedule \(for example, 25 units on one date and the remaining 25 units on a later date\).

15. Select **Send confirmation**.

    This does not notify ServiceNow® immediately. The confirmation pull retrieves it.

16. Pull and verify the confirmation in ServiceNow
17. Go to the ERP source configuration and open the SupplyOn integration service for purchase order confirmations, which triggers the confirmation pull \(**get order confirmations import**\).

18. To run the pull immediately, select **Run job**.

    If you don't run the job manually, it runs on schedule.

19. When the run completes, review the processing message.

    It summarizes the date range used and the number of confirmations pulled, along with any failures.

20. Open the purchase order and refresh.

    A new purchase order confirmation appears.


## Result

Because SupplyOn delivery schedules can split a line across dates, the import creates one purchase order confirmation per confirmed line and one confirmation line per delivery schedule. For example, a line split into two deliveries of 25 units produces one confirmation with two confirmation lines. Each line carries its quantity, its date, and a status of **Changes requested**.

