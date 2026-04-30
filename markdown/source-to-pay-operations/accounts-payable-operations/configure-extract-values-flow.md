---
title: Configure the newly created DocIntel Extract Values Flow
description: Configure the newly created DocIntel Extract Values Flow - copied use case - Invoice Processing v3 flow to add the missing information by referring to the default DocIntel Extract Values Flow - Invoice Processing v3 flow.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a copy of the default Invoice Processing use case, Configuring the invoice ingestion flows using Accounts Payable Operations integration with Document Intelligence, Install Accounts Payable Operations integration with Document Intelligence, Configuring Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Configure the newly created DocIntel Extract Values Flow

Configure the newly created **DocIntel Extract Values Flow - copied use case - Invoice Processing v3** flow to add the missing information by referring to the default **DocIntel Extract Values Flow - Invoice Processing v3** flow.

## Before you begin

Role required: admin

## About this task

In the **DocIntel Extract Values Flow - copied use case - Invoice Processing v3** flow, perform the following steps.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Search for and open the **DocIntel Extract Values Flow - Invoice Processing v3** flow.

3.  In the **DocIntel Extract Values Flow - copied use case - Invoice Processing v3** flow, under **Actions**, configure two new actions similar to **Look up Invoice Stage Record** \(action 3\) and **Update Invoice Stage Record** \(action 4\) from flow mentioned in step 2.

4.  In the **DocIntel Extract Values Flow - copied use case - Invoice Processing v3** flow, under TRIGGER, do the following:

    Configure the condition by appending **AND** condition with existing condition where the new condition is **Use case** which is equal to copied use case. Example: Use case=&lt;&lt;**copied use case**&gt;&gt;.

5.  Select **Save**.

6.  Select **Activate**.


