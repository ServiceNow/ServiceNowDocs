---
title: Transaction quotas
description: Transaction quotas allow you to define a quota policy for different types of transactions. A transaction quota cancels any transaction in violation of the policy and notifies the user of the cancellation.
locale: en-US
release: yokohama
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2025-05-08"
reading_time_minutes: 2
breadcrumb: [Configuring the ServiceNow AI Platform to optimize performance, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Transaction quotas

Transaction quotas allow you to define a quota policy for different types of transactions. A transaction quota cancels any transaction in violation of the policy and notifies the user of the cancellation.

Administrators can set transaction quotas to prevent poorly performing queries and scripts from consuming system resources. This ensures that no transaction consumes enough resources to prevent other transactions from running. Administrators can also view cancellation log messages to identify transactions that might consume excessive resources.

The Transaction Quotas plugin is active by default on all new and upgraded instances.

## How transaction quotas work

Transactions use the Quota Manager, which is a background thread that cancels transactions according to transaction quota rules. The Quota Manager performs the following actions.

1.  Obtains a list of active transactions, similar to the list under **User Administration** &gt; **Active Transactions**.
2.  Cycles through each transaction and checks all quota rules with conditions matching the transaction. The first occurrence that exceeds any of the quota limitations triggers a transaction cancellation. If a transaction changes or there is a new quota rule, the Quota Manager re-evaluates the transaction.

    **Note:** The **Order** field on a quota rule affects the order in which the quota rules are checked. The Quota Manager checks lower-order rules first \(for example, order 80 before order 90\), but ultimately checks all rules. This might have marginal performance implications, depending on the conditions of the rules involved.

3.  Cancels the transaction if it has been running longer than the specified quota maximum.
4.  Logs the running transactions.
5.  Sleeps until the next heartbeat, which is controlled by the **glide.quota.manager.heartbeat** [system property](../reference/r_ConfigureTransactionQuotaProps.md).

## Transaction cancellation from exceeded quotas

When a transaction runs longer than the maximum duration specified by a quota rule, the user is notified of the cancellation and the reason.

Additionally, a warning is logged in the Transaction Cancellation Log whenever a transaction is cancelled due to exceeded quotas. To view the Transaction Cancellation Log, navigate to **All** &gt; **System Logs** &gt; **System Log** &gt; **Transaction Cancellation Log**.

## Transaction cancellation examples

Transactions can be canceled for more than one reason. Look for the following indicators.

-   **maximum execution time exceeded**: This message appears when the glide.quota.manager threads cancels the transaction.
-   **canceled by other transaction**: This message appears when the transaction was canceled by the session thread that initially issued it, and not by the glide.quota.manager thread.
-   **canceled by user request**: This message appears when the user selected the red X button to cancel the running transaction.

If you are looking for transactions that were canceled by glide.quota.manager, search for the **\[Message\] \[Contains\] \[maximum execution time exceeded\]** combination. For example:

```
Cancelling transaction /home.do - Default-thread-11.0 (maximum execution time exceeded): Thread Default-thread-11.0 (Default-thread-11.0, F530DD111B11111111FC031767DA158E), after 30000ms
```

.

