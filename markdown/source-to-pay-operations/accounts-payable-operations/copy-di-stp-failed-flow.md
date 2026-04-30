---
title: Copy and configure the DI STP Failed flow
description: Copy and configure the DI STP Failed flow and activate this flow to use it.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring the invoice ingestion flows using Accounts Payable Operations integration with Document Intelligence, Install Accounts Payable Operations integration with Document Intelligence, Configuring Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Copy and configure the DI STP Failed flow

Copy and configure the DI STP Failed flow and activate this flow to use it.

Copy and configure the DI STP failed flow 

## Before you begin

Role required: admin

Scope: sn\_ap\_ic scope.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Search for and open the **DI STP Failed** flow.

3.  Select the more actions icon \(![more actions icon](../../supplier-lifecycle-operations/image/more-actions-icon.png)\) in the top right and select **Copy flow**.

    The Create a copy of this flow dialog box is displayed.

4.  In the **New flow name** field, enter a name for the copied flow.

5.  In the **Application** field, select **Accounts Payable Operations integration with Document Intelligence**.

6.  Select **Copy**.

    A copy of the flow opens. Under **TRIGGER**, in the **Condition** field, copy "DI STP Failed" flow and update trigger condition to reference the use case created by the customer. Use the AND operator and select **Use case** is **copied Gen AI use case** and **Done**. Use the AND operator and, select **Use case** is **copied Gen AI use case** and **Done**. ![DI STP Failed trigger condition](../image/di-stp-failed-genai.png). For more information on copying use case, refer [Create a copy of the default Invoice Processing use case](create-use-case-copy.md) and [Copy and activate the generative AI DocIntel flow](configure-gen-ai-di-flow.md).

7.  Select **Save**.

8.  Select **Activate**.


