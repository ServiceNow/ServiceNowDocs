---
title: Transaction quota rule form
description: A description of the fields on the Transaction Quota Rule form.
locale: en-US
release: xanadu
product: Platform Performance
classification: platform-performance
topic_type: reference
last_updated: "2025-05-08"
reading_time_minutes: 1
breadcrumb: [Platform performance reference, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Transaction quota rule form

A description of the fields on the Transaction Quota Rule form.

|Field|Description|
|-----|-----------|
|Name|A unique name to identify the rule.|
|Active|A check box that determines if this rule is active \(selected\).|
|Maximum Duration|The number of seconds a transaction has to complete before the quota cancels the transaction.|
|Maximum Business Rules|The number of business rules executions allowed.|
|Maximum Database Time|The total number of seconds for all SQL requests.|
|Maximum SQL Statement Time|The number of seconds a SQL statement can run.|
|Maximum Outbound Requests|The number of outbound HTTPs requests allowed.|
|Order|A number that represents the priority of the quota transaction in relation to other quotas. The transaction quota with the lowest timeout, the lowest order value, and matching conditions determines the applied quota policy.|
|Maximum Events|The number of sysevent inserts allowed.|
|Maximum Jobs|The number of sys\_trigger inserts allowed.|
|Maximum SQL Queries|The number of SQL queries allowed.|
|Maximum Outbound Request Duration|The number of seconds for an outbound HTTP request.|
|Description|A description of the transaction quota rule.|

**Parent Topic:**[Platform performance reference](../concept/platform-performance-references.md)

