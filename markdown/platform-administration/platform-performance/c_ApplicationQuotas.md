---
title: Application quotas
description: You can set a limit on the number of events or jobs that can run in an application's scope within a specified time. Limiting the number of events or jobs running at the same time can help optimize bandwidth usage.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/platform-performance/c\_ApplicationQuotas.html
release: australia
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Application quotas

You can set a limit on the number of events or jobs that can run in an application's scope within a specified time. Limiting the number of events or jobs running at the same time can help optimize bandwidth usage.

Application quota rules limit the number of events or jobs that can run within an application's scope during a specified amount of time. Each scoped application can have one application quota rule. When an application exceeds the quota limit, scheduled jobs and events that are already running complete. New scheduled jobs and events in the application scope are deferred until the next update period.

An application quota rule applies to transactions created by all instances of an application and all transactions created by methods of the application called by other applications. If two users are running the same application, the application quota rule does not distinguish between transactions for each instance of the application. If, together, they violate the quota, new scheduled jobs and events in the application's scope are deferred.

If you select the **Log Only** check box, scheduled jobs and events aren't deferred by a quota violation. Instead, entries are added to the local host log that indicate the transactions are running under violation.

Transaction and application quota rules are evaluated separately. By defining an application quota rule, you introduce another restriction. A transaction is canceled if it violates a transaction quota rule. Scheduled jobs and events are deferred if, collectively with other application transactions, they violate the application quota rule.

You can't define an application quota rule for the global application.

