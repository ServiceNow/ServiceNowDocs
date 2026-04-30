---
title: Service Level Agreement \(SLA\) breakdown definitions
description: Using SLA breakdown, the service owner or service desk manager can see detailed task ownership and SLA duration related data for any task SLA record associated with a task. This helps determine which teams and users are contributing to SLA compliance.
locale: en-US
release: zurich
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Service Level Management, IT Service Management]
---

# Service Level Agreement \(SLA\) breakdown definitions

Using SLA breakdown, the service owner or service desk manager can see detailed task ownership and SLA duration related data for any task SLA record associated with a task. This helps determine which teams and users are contributing to SLA compliance.

SLA breakdown is configurable and typically should be configured for the more significant SLAs such as P1 and P2 resolution. By default, the system deletes SLA breakdown data that is more than one year old. This is performed by a new table cleanup job **sla\_breakdown\_by\_assignment**. Table cleanup jobs are defined in the \[sys\_auto\_flush\] table.

**Parent Topic:**[Exploring Service Level Management](exploring-slm.md)

**Related topics**  


[Configure Service Level Agreement \(SLA\)](c_ConfigureSLAs.md)

