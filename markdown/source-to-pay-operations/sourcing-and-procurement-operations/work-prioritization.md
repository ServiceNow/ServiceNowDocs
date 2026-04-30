---
title: Work prioritization
description: Work prioritization automatically assigns a priority level to purchase requisitions, sourcing requests, and procurement cases so that procurement specialists can work the most urgent items first.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-04-01"
reading_time_minutes: 4
keywords: [work prioritization, priority levels, decision table, procurement specialist, work queue, automatic priority assignment, priority scale, line item evaluation, Planning priority, purchase requisition, sourcing request, procurement case, sourcing and procurement operations, SPO]
breadcrumb: [Procurement Case Management, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Work prioritization

Work prioritization automatically assigns a priority level to purchase requisitions, sourcing requests, and procurement cases so that procurement specialists can work the most urgent items first.

When procurement records arrive in a specialist's queue, they have no automatic signal indicating which items are most urgent. Without prioritization, a minor catalog update and a high-value supplier renegotiation appear identical. Work prioritization solves this by evaluating each record against a set of administrator-defined rules and stamping it with a priority level before a specialist opens it. The result is a work queue that specialists can sort and filter by priority, with the most business-critical records surfaced at the top.

Priority is assigned automatically. Specialists and requesters do not set it manually. Administrators control the rules that determine how priority is calculated, through decision tables they configure for each record type. For more information about configuring decision table rules to automatically assign priority to purchase requisitions, sourcing requests, and procurement cases, see [Configuring work prioritization](../concept/configuring-work-prioritization.md).

## Priority levels

Work prioritization uses a five-level priority scale.

|Priority|Value|Description|
|--------|-----|-----------|
|Critical|1|Highest urgency. Requires immediate attention.|
|High|2|Significant urgency. Work ahead of routine items.|
|Moderate|3|Standard urgency. Normal processing timeline.|
|Low|4|Lower urgency. Can be deferred when higher-priority items are waiting.|
|Planning|5|System default. Assigned when no configured rule matches the record.|

The Planning priority is not a value that administrators configure. It is the fallback assigned to any record that no rule matches. Administrators can roll out work prioritization incrementally — records for which no rules have been written yet receive Planning priority and appear at the bottom of the queue.

## Decision table mechanism

Priority rules are defined in decision tables — structured sets of if-then rules where each row specifies one or more conditions and the priority level to assign when those conditions are met. Administrators configure the rules. The system evaluates them automatically whenever a relevant record is created or updated.

There is one decision table per record type.

|Decision table|Record type|Default evaluation basis|
|--------------|-----------|------------------------|
|Priority defaulting for purchase requisitions|Purchase requisitions|Line total amount \(financial threshold\)|
|Priority defaulting for sourcing requests|Sourcing requests|Business owner job code \(organizational hierarchy\)|
|Priority defaulting for procurement cases|Procurement cases|No default rules — administrators define all conditions|

The purchase requisition and sourcing request decision tables include example rules provided as demo data. These rules may not be loaded in production instances and require review before use. The procurement case decision table ships with no rules. Administrators define all conditions from scratch.

## How line items drive priority

Purchase requisitions, sourcing requests, and procurement cases can contain multiple line items. Work prioritization evaluates each line item individually and assigns the parent record the highest-urgency result found across all lines.

A single high-priority line item drives the entire parent record to that priority level. For example, if a purchase requisition contains ten lines and one line has a total amount that meets the Critical threshold, the entire requisition is assigned Critical priority, regardless of the other nine lines.

When specialists open a high-priority record, they should expect to find at least one line item that meets a high-priority condition. Other lines on the same record may be routine.

Lines in a canceled or closed state are excluded from the evaluation and do not contribute to the parent record's priority.

## Automatic priority calculation

Priority is calculated automatically in the background whenever a record is created or updated, and whenever one of its line items is created or updated. The calculation runs after the record is saved and does not affect the save operation. The priority field is updated within moments of the triggering event.

Priority is not recalculated for records in a closed or rejected state. After a record reaches a terminal state, its priority is frozen at the value it held at the time of closure.

When a line item is edited; for example, when a line amount is revised, the parent record's priority is recalculated automatically. Specialists do not need to manually refresh or recalculate priority after editing a line.

## Fallback behavior

If a record is evaluated and no configured rule matches, the record retains its current priority. For a newly created record, that means it keeps the Planning priority value that the system assigns on creation.

A record with Planning priority indicates that no rule matched — not that an administrator configured it as Planning. It is a signal that the record falls outside the currently defined rules. When the next update to the record or one of its lines triggers a recalculation, the rules are evaluated again. If a matching rule has been added since the last evaluation, the priority updates accordingly.

-   **[Work prioritization example](work-prioritization-example.md)**  
This example shows how an organization might configure work prioritization rules for all three record types, and what happens when records are evaluated against those rules.

**Parent Topic:**[Procurement Case Management](../concept/psd-overview.md)

