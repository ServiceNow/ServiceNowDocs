---
title: Application quotas
description: You can set a limit on the number of events or jobs that can run in an application's scope within a specified time. Limiting the number of events or jobs running at the same time can help optimize bandwidth usage.
locale: en-US
release: yokohama
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring the ServiceNow AI Platform to optimize performance, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Application quotas

You can set a limit on the number of events or jobs that can run in an application's scope within a specified time. Limiting the number of events or jobs running at the same time can help optimize bandwidth usage.

Application quota rules limit the number of events or jobs that can run within an application's scope during a specified amount of time. Each scoped application can have one application quota rule. When an application exceeds the quota limit, all transactions running in the application scope are canceled. Until the next update period, new transactions within the application scope are cancelled as soon as they're initiated. These actions effectively block transactions from an application scope from running for the update period.

An application quota rule applies to transactions created by all instances of an application and all transactions created by methods of the application called by other applications. If two users are running the same application, the application quota rule does not distinguish between transactions for each instance of the application. If, together, they violate the quota, all transactions in the application's scope are canceled.

If you check the **Log Only** option, transactions are not canceled by a quota violation. Instead, entries are added to the local host log that indicate the transactions are running under violation.

Transaction and application quota rules are evaluated separately. By defining an application quota rule, you simply introduce another restriction. A transaction is canceled if it violates a transaction quota rule, or if collectively with other application transactions, it violates its application quota rule.

You cannot define an application quota rule for the global application.

