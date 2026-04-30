---
title: Transaction cancellation
description: You can cancel transactions that take longer than expected to load. Canceling long-running transactions can help prevent excessive resource consumption.
locale: en-US
release: yokohama
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2025-05-13"
reading_time_minutes: 2
breadcrumb: [Resolving platform performance issues, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Transaction cancellation

You can cancel transactions that take longer than expected to load. Canceling long-running transactions can help prevent excessive resource consumption.

Causes of slow-loading transactions include the following scenarios.

-   Sorting a large number of records by an unindexed string field.
-   Grouping a large table on a field that has predominantly distinct values.
-   Exporting all rows from a large table.
-   Testing a poorly scripted business rule that has an infinite JavaScript loop.

## Transaction cancel timer

**Note:** You can’t cancel an import with these controls.

During a long-running transaction, a timer and a cancellation option appear in an alert banner.

![An example running transaction alert banner, with the text "Running transaction: 6 seconds" and aCancel button.](../image/CancelRequest.png "Cancel request")

To cancel the transaction, select the **Cancel** button. The alert message displays when a transaction cancellation is in progress and when the cancellation is completed.

If a slow transaction completes successfully, the timer indicates how long it took for the transaction to complete.

![A slow transaction completion alert banner, with text "Transaction completed: 4 seconds."](../image/TransactionCompleted.png "Transaction completed")

## Canceled transaction logs

Canceled transactions appear in the transaction log with **CANCELLED** appended to the URL. Transactions canceled by a user are logged differently from transactions canceled by transaction quotas. For more information about canceled transaction logging, see [Canceled-transaction logging to a table](c_CanTranLogTbl.md). For more information about transaction quotas, see [Transaction quotas](c_TransactionQuotas.md).

## Properties for transaction cancellation

Administrators can configure the behavior of the transaction cancellation capability using the following properties.

|Property|Definition|Location|
|--------|----------|--------|
|com.glide.request\_manager.active|Let users cancel long-running transactions \(enabled by default\).|Open the sys\_properties table by navigating to **All** and entering `sys_properties.list`.|
|glide.ui.transaction.long\_response.time|Delay in seconds before the cancel transaction button appears for a long-running transaction.|Navigate to **All** &gt; **System Properties** &gt; **UI Properties** and locate the field labeled **Delay in seconds before the Transaction Cancel button is displayed for a long-running transaction**.|

-   **[View and kill active transaction](../task/t_ViewAndKillAnActiveTransaction.md)**  
Administrators can view active transactions and kill long-running transactions.
-   **[Canceled-transaction logging to a table](c_CanTranLogTbl.md)**  
The system logs canceled transactions to a table in addition to the transaction log.

**Parent Topic:**[Resolving platform performance issues](resolving-plat-performance-issues.md)

