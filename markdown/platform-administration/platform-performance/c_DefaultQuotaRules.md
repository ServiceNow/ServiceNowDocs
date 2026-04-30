---
title: Default quota rules
description: Various transaction quota rules are available in the base system.
locale: en-US
release: xanadu
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Platform performance reference, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Default quota rules

Various transaction quota rules are available in the base system.

-   **Fix Script Processor**

    Allows the fix script processor to run for four hours.

-   **Presence**

    Cancels presence requests quickly when the system is busy.

-   **REST Import Set API request timeout**

    Prevents inbound REST Import Set API transactions from running for longer than 60 seconds.

-   **REST Table API request timeout**

    Prevents inbound REST Table API transactions from running for longer than 60 seconds.

-   **AMB Transactions**

    Cancels AMB transactions lasting longer than the specified maximum duration. Applies to all AMB transaction types: message send and message receive.

-   **Reference Completer**

    Stops the reference completer transaction after five seconds.

-   **REST Aggregate API request timeout**

    Prevents inbound REST Aggregate API transactions from running for longer than 60 seconds.

-   **Homepage Widgets**

    Prevents all homepage widgets from running longer than 30 seconds.

-   **REST Attachment API request timeout**

    Prevents inbound REST Import Set API transactions from running for longer than 60 seconds.

-   **UA Count Persistor Quota**

    Prevents UA count persistor scheduled jobs from running for more than one hour.

-   **UI Transactions**

    Cancels UI transactions that are two seconds away from the 5-minute server disconnect. ServiceNow datacenter load balancers display an internal server error \(HTTP Error 500\) to users after five minutes. This quota rule returns a transaction canceled page instead of an error. This rule includes an exception to prevent the cancellation of background scripts.

-   **PA Diagnostics All**

    Prevents any Diagnostics transaction that originates outside the scope of the Diagnostics application from running longer than 30 minutes. Diagnostics transactions refer to executing a diagnostic, opening a Diagnostics form, or opening a Diagnostics list.


## Normal transaction activities

Before setting transaction quotas, navigate to **User Administration** &gt; **Active Transactions** to review the normal transaction activities for your instance. You can [view and terminate long-running transactions](../task/t_ViewAndKillAnActiveTransaction.md) if necessary. Over time, you can determine the normal transaction load for your instance and set your quotas to match these norms.

**Parent Topic:**[Platform performance reference](platform-performance-references.md)

