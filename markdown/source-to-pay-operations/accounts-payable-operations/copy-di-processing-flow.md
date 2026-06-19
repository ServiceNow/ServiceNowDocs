---
title: Copy and configure the Invoice attachment DI processing flow
description: Copy and configure the Invoice attachment DI processing flow and activate this flow to use it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/copy-di-processing-flow.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice processing, invoice automation]
breadcrumb: [Configuring the invoice ingestion flows using Accounts Payable Operations integration with Document Intelligence, Install Accounts Payable Operations integration with Document Intelligence, Configure, Accounts Payable Operations, Finance and Supply Chain]
---

# Copy and configure the Invoice attachment DI processing flow

Copy and configure the Invoice attachment DI processing flow and activate this flow to use it.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Search for and open the **Invoice attachment DI processing** flow.

3.  Select the more actions icon \[Omitted image "more-actions-icon.png"\] Alt text: more actions\) in the top right and select **Copy flow**.

    The Create a copy of this flow dialog box is displayed.

4.  In the **New flow name** field, enter a name for the copied flow.

5.  Select the more actions icon \[Omitted image "more-actions-icon.png"\] Alt text: more actions\) in the top right and select **Copy flow**.

    The Create a copy of this flow dialog box is displayed.

6.  In the **New flow name** field, enter a name for the copied flow.

7.  In the **Application** field, select **Accounts Payable Operations integration with Document Intelligence**.

8.  Select **Copy**.

    A copy of the flow opens.

9.  Under TRIGGER, set the trigger conditions for this flow.

10. Under ACTIONS, do the following:

    -   Select **Process Attachment using DI** to expand it.
    -   In the **SYS DI Task Definition \[Use Case\]** field, select the copy of the use case that was created using the **Duplicate use case** icon \(\[Omitted image "duplicate-di-usecase.png"\] Alt text: duplicate DI use case\) in Global scope. For more information on copying use case, refer [Create a copy of the default Invoice Processing use case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-use-case-copy.md).\[Omitted image "inv-process-flow-di-skill.png"\] Alt text: Invoice processing case for invoice email flow
11. Select **Save**.

12. Select **Activate**.


