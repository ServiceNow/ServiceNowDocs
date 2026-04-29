---
title: Migrate to service level management
description: Migrate SLA processing from the escalations engine to use the service level management functionality.
locale: en-US
release: australia
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Level Management reference, Service Level Management, IT Service Management]
---

# Migrate to service level management

Migrate SLA processing from the escalations engine to use the service level management functionality.

The two core differences between the old SLA engine and the new service level management plugin are that tasks can now run multiple SLAs simultaneously, and the escalation concept has been replaced with the more robust Workflow Editor. This allows administrators greater control on what actions, notifications, and events are triggered by tasks, to take into account more mature Service Level processes.

If an instance has been using the original SLA engine and has just activated the Service Level Agreements \(SLA\) Plugin, the old SLAs will not work. For the old SLAs to work, they must be converted to the new SLA Definition records, which will attach the appropriate Task SLA records to the matching Task records. This is done manually by creating new SLA Definition records that reflect the definition of the old SLA. Old SLAs will continue to function, but any time a task is updated, the appropriate new Task SLAs will attach.

Once new Task SLAs are implemented, they will attach themselves to any new or updated incident, including ones which already have old SLAs attached. If the new Task SLA is set to retroactively start, it will automatically calculate the duration from that point in the past, which means that the duration will still be accurate.

When enabled, the property **Compute prior SLA pause time for new, retroactive SLAs \(2011 SLA engine only\)** calculates the pause time when a retroactive SLA is attached.

For example: if a retroactive SLA attaches to an incident one hour after its creation, and meets the pause conditions for half an hour, then the elapsed time is half an hour rather than the full hour.

**Note:** This property is only used with audited tables. Tables which are not audited ignore the pause time before the creation of the record.

**Parent Topic:**[Service Level Management reference](service-level-management-reference.md)

