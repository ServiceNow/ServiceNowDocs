---
title: Configure the newly created DocIntel Extract Values Flow
description: Configure the newly created DocIntel Extract Values Flow - copied use case - Invoice Processing v7 flow to add the missing information by referring to the default DocIntel Extract Values Flow - Invoice Processing v7 flow.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a copy of the default Invoice Processing use case, Configuring the invoice ingestion flows using Accounts Payable Operations integration with Document Intelligence, Install Accounts Payable Operations integration with Document Intelligence, Configuring Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Configure the newly created DocIntel Extract Values Flow

Configure the newly created **DocIntel Extract Values Flow - copied use case - Invoice Processing v7** flow to add the missing information by referring to the default **DocIntel Extract Values Flow - Invoice Processing v7** flow.

Configure the newly created DocIntel Extract Values flow. 

## Before you begin

Role required: admin

## About this task

In the **DocIntel Extract Values Flow - copied use case - Invoice Processing v7** flow, perform the following steps.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Search for and open the **DocIntel Extract Values Flow - Invoice Processing v7** flow.

3.  In the **DocIntel Extract Values Flow - copied use case - Invoice Processing v7** flow, under TRIGGER, do the following:

    Configure the condition by appending **AND** condition with existing condition where the new condition is **Use case** which is equal to copied use case. Example: Use case=&lt;&lt;**copied use case**&gt;&gt;.![Copied GenAI use case](../image/add-genai-usecase.png)

4.  In the **DocIntel Extract Values Flow - copied use case - Invoice Processing v7** flow: under **Actions**, configure new actions similar to **Look up Invoice Stage Record** \(action 3\), **Look up Invoice Case Record** \(action 4\), **Condition label : Check if invoice on invoice case is not empty** \(action 5, 6, 7\) and **Update stage record** \(action 8\) from flow mentioned in step 2.![Trigger condition](../image/trigger-condition-usecase.png)

5.  Select **Save**.

6.  Select **Activate**.


