---
title: View and kill active transaction
description: Administrators can view active transactions and kill long-running transactions.
locale: en-US
release: yokohama
product: Platform Performance
classification: platform-performance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Transaction cancellation, Resolving platform performance issues, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# View and kill active transaction

Administrators can view active transactions and kill long-running transactions.

## Before you begin

Role required: admin

## About this task

This action is intended to stop background processes, such as scheduled jobs, and not user-initiated transactions.

## Procedure

1.  If [High Security Settings](https://www.servicenow.com/docs/access?context=c_HighSecuritySettings&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) are enabled, elevate privileges to security\_admin.

2.  Navigate to the appropriate **Active Transactions** module.

    -   To view and kill transactions on the current node for your instance, navigate to **User Administration** &gt; **Active Transactions**.
    -   To view and kill transactions on all nodes for your instance, navigate to **System Diagnostics** &gt; **Active Transactions \(All Nodes\)**.
3.  Find the transaction that you want to stop.

    The process to display the transactions is included in the list. Don’t kill that process.

4.  Kill the transaction in one of the following ways:

    -   Select and hold \(or right-click\) the record and select **Kill** from the available options.
    -   Select the check box next to one or more records and select **Kill** from the **Actions on selected rows** drop-down menu.

**Parent Topic:**[Transaction cancellation](../concept/transaction-cancellation.md)

