---
title: Transaction call chains
description: Identify and debug the root causes for a problematic transaction by recording, and then reviewing, its call chain. A call chain consists shows the ordered series of scripts executed during the life cycle of a transaction.
locale: en-US
release: xanadu
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Monitoring platform performance, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Transaction call chains

Identify and debug the root causes for a problematic transaction by recording, and then reviewing, its call chain. A call chain consists shows the ordered series of scripts executed during the life cycle of a transaction.

With Transaction Call Chain tracking, an administrator can register the URL of a problematic transaction. The call chain is then recorded during the next occurrence of the registered URL. Transaction call chains can help diagnose transaction performance issues.

The following shows the workflow for enabling and using transaction call chain tracking.

![An infographic showing the workflow for adding a transaction call chain register. For more details, refer to the following description.](../image/add-transaction-call-chain-register.png)

1.  When you find a problematic transaction on the Transaction Log or Slow Transaction list that requires debugging, select it to view its detail record. To aid in debugging, filter and group these lists by application scope, limiting transactions that appear to only those transactions originating in specific scopes.

    **Note:** To learn more about these lists, see [Transaction logs](https://www.servicenow.com/docs/access?context=r_TransactionLogs&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) and [Slow transactions log record detail](../reference/slow-transactions-log-record-detail.md).

2.  In the record detail form, select **Record call chain of next occurrence**. Doing this designates that the next occurrence of the transaction URL should be persisted with all of its call chain information.

    Optionally, you can designate a user ID so call chain recording only takes place during the next transaction occurrence for a specific user.

3.  The next time a user accesses the URL, the Transaction Call Chain Register record is updated to contain a list of the script resources executed to service the request. This list of resources is available for administrators to view by navigating to the Transaction Call Chain Record and selecting the Transaction Call Chain Related List.

    ![A transaction is executed and logged in the Transaction Call Chain Register, then accessed by the admin through the Transaction Call Chain Related List on the Transaction Call Chain Record.](../image/url-transaction-logged.png)

4.  In Transaction Call Chains, review the recorded call chain for the transaction, and then take the needed actions required to debug it.

-   **[Create a transaction call chain register](../task/create-transaction-call-chain-register.md)**  
Create a call chain register to record call chain information for a problematic \(or slow\) transaction during the next occurrence of that URL. You specify that the next occurrence of the transaction URL should be persisted with all of its call chain information.
-   **[Review a transaction call chain](../task/review-transaction-call-chain.md)**  
Use Transaction Call Chains to review the resulting call chain for a selected transaction. You can use the information in Transaction Call Chains can help debug performance issues.

**Parent Topic:**[Monitoring platform performance](monitoring-platform-performance.md)

