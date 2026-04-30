---
title: Copy and configure the Invoice processing case for Invoice email flow
description: Copy and configure the Invoice processing case for Invoice email flow and add a trigger condition to specify when to create an invoice processing case.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring the invoice ingestion flows using Accounts Payable Operations integration with Document Intelligence, Install Accounts Payable Operations integration with Document Intelligence, Configuring Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Copy and configure the Invoice processing case for Invoice email flow

Copy and configure the Invoice processing case for Invoice email flow and add a trigger condition to specify when to create an invoice processing case.

## Before you begin

Role required: admin

## About this task

When activated, this flow automatically creates an invoice processing case for an inbound email.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Search for and open the **Invoice processing case for Invoice email** flow.

3.  Select the more actions icon \(![more actions](../../supplier-lifecycle-operations/image/more-actions-icon.png)\) in the top right and select **Copy flow**.

    The Create a copy of this flow dialog box is displayed.

4.  In the **New flow name** field, enter a name for the copied flow.

5.  In the **Application** field, select **Accounts Payable Operations integration with Document Intelligence**.

6.  Select **Copy**.

    A copy of the flow opens.

7.  Under TRIGGER, select **Inbound Email**.

8.  In the **Trigger** field, leave the trigger as **Inbound Email**.

9.  Update the email conditions according to your business requirements.

    **Note:** Don't activate this flow without configuring email conditions to specify when to create an invoice processing case. Otherwise, an invoice processing case is created for any email that you receive.

10. Select **Save**.

11. Select **Activate**.


