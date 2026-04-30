---
title: Copy and configure the Invoice attachment DI processing flow
description: Copy and configure the Invoice attachment DI processing flow and activate this flow to use it.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring the invoice ingestion flows using Accounts Payable Operations integration with Document Intelligence, Install Accounts Payable Operations integration with Document Intelligence, Configuring Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Copy and configure the Invoice attachment DI processing flow

Copy and configure the Invoice attachment DI processing flow and activate this flow to use it.

## Before you begin

Role required: admin

Scope: sn\_ap\_ic scope.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Search for and open the **Invoice attachment DI processing** flow.

3.  Select the more actions icon ![more actions](../../supplier-lifecycle-operations/image/more-actions-icon.png)\) in the top right and select **Copy flow**.

    The Create a copy of this flow dialog box is displayed.

4.  In the **New flow name** field, enter a name for the copied flow.

5.  In the **Application** field, select **Accounts Payable Operations integration with Document Intelligence**.

6.  Select **Copy**.

    A copy of the flow Invoice Attachment DI Processing flow opens.

7.  Under **Trigger**, select **Use case** is **copied Doc Intel use case** and **Done**.

8.  Under ACTIONS, do the following:

    -   Select **Process Attachment using DI** to reference the use case created by the customer.
    -   In the **DI Task Definition \[Use Case\]** field, select the copy of the use case that was created using the **Duplicate use case** icon \(![duplicate DI use case](../image/duplicate-di-usecase.png)\) in sn\_ap\_ic scope. For more information on copying use case, refer [Create a copy of the default Invoice Processing use case](create-use-case-copy.md).
9.  Select **Save**.

10. Select **Activate**.


