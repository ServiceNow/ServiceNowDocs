---
title: Configure the Accounts Payable Operations queues
description: Configure Advanced Work Assignment queues to automatically route supplier communications, including email and chat to the appropriate accounts payable agents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/configure-the-account-payable-operation-queues.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, supplier, email ingestion, Advanced Work Assignment, AWA]
breadcrumb: [Configure Advanced Work Assignment for Accounts Payable Operations, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Configure the Accounts Payable Operations queues

Configure Advanced Work Assignment queues to automatically route supplier communications, including email and chat to the appropriate accounts payable agents.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Source to Pay Workspace** &gt; **All** &gt; **Advanced Work Assignment** &gt; **&gt;Queues**.

2.  Select one of the following mentioned queues for Account Payable Operations.

    -   Invoice Inquiry case
    -   Chat
3.  In the **Assignment Eligibility related** list, select **New**.

    1.  In the **Agent assignment rule** field, select **Chat - Most Capacity**.
    2.  Select the lock icon \(\[Omitted image "lock-icon.png"\] Alt text: Lock icon\) next to the **Groups** field.
    3.  Select the look-up icon \(\[Omitted image "look-up-icon.png"\] Alt text: Look-up icon\) to view the list of groups.
    4.  Select **New**.
    5.  In the **Name** field, enter a name for the group.
    6.  Fill in the remaining fields, as appropriate.
    7.  Select **Submit**.
    8.  Select the lock icon \(\[Omitted image "lock-icon.png"\] Alt text: Lock icon\) to lock the **Groups** field.
    9.  Right-select and select **Save**.
4.  Next to the **Groups** field, select the link to the group, which opens the group record.

    1.  In the Group Members related list, select **Edit** to add members to the group.
    2.  Select one or more users in the Collection list and move them to the Group Members List.
    3.  Select **Save**.

        **Note:** The users that you add to this assignment group are automatically granted the awa\_agent role.


**Parent Topic:**[Configure Advanced Work Assignment for Accounts Payable Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/configure-advanced-work-assignment-for-apo.md)

