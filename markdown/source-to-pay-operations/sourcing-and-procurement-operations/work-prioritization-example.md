---
title: Work prioritization example
description: This example shows how an organization might configure work prioritization rules for all three record types, and what happens when records are evaluated against those rules.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-04-01"
reading_time_minutes: 4
keywords: [work prioritization example, priority defaulting, decision table rules, purchase requisition priority, sourcing request priority, procurement case priority, line item priority, business owner job code, line total amount, modification type, Planning priority fallback, SPO configuration example]
breadcrumb: [Work prioritization, Procurement Case Management, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Work prioritization example

This example shows how an organization might configure work prioritization rules for all three record types, and what happens when records are evaluated against those rules.

A manufacturing organization has deployed the SPO application and is configuring work prioritization for the first time. Their procurement team has agreed on three different criteria, one per record type, that reflect the factors most relevant to their business.

## Example configuration

For purchase requisitions, the team prioritizes based on the total value of each line item. Larger-spend lines require faster turnaround and tighter oversight.

|Rule|Condition|Priority assigned|
|----|---------|-----------------|
|1|Purchase line total amount is $100,000 or more|Critical|
|2|Purchase line total amount is between $50,000 and $99,999|High|
|3|Purchase line total amount is between $25,000 and $49,999|Moderate|
|4|Purchase line total amount is $24,999 or less|Low|

For sourcing requests, the team prioritizes based on the organizational seniority of the business owner. Requests sponsored by senior leaders require faster response.

|Rule|Condition|Priority assigned|
|----|---------|-----------------|
|1|Business owner job code is CFO or CEO|Critical|
|2|Business owner job code is IC4 or above|High|
|3|Business owner job code is a Manager level|Moderate|
|4|Business owner job code is IC1, IC2, or IC3|Low|

For procurement cases, the team prioritizes based on the type of modification being requested. Supplier changes and contract amendments carry higher organizational risk than routine catalog updates.

|Rule|Condition|Priority assigned|
|----|---------|-----------------|
|1|Case line modification type is Supplier change or Contract amendment|High|
|2|Case line modification type is Price change|Moderate|
|3|Case line modification type is Catalog update or Description change|Low|

## Purchase requisition with mixed line values

A department manager submits a purchase requisition for three items: office furniture \($12,000\), a desktop workstation \($8,500\), and a conference room display system \($67,000\).

When the requisition is saved, the system evaluates each line against the decision table. The furniture line \($12,000\) matches Rule 4 and returns Low. The workstation line \($8,500\) also matches Rule 4 and returns Low. The display system line \($67,000\) matches Rule 2 — its amount falls between $50,000 and $99,999 — and returns High.

The system selects the most urgent result across all three lines: High. The priority field on the purchase requisition is updated to High.

When the requisition appears in the specialist's queue, it is flagged as High — driven by the single large-value line, even though the other two lines were routine in scale. The specialist knows to examine the requisition promptly and will find the $67,000 display system line when they open it.

## Sourcing request based on business owner seniority

A sourcing event is created to evaluate suppliers for a new category of raw materials. The business owner on the request holds a job code that corresponds to an IC4-level role.

When the sourcing request is saved, the system evaluates the business owner's job code against the decision table. The IC4 job code matches Rule 2 and the sourcing request receives High priority.

If the same sourcing event had been initiated by a manager-level business owner, the request would have received Moderate priority instead. The same sourcing event, sponsored by a different person, lands differently in the queue — reflecting the organizational importance of who is sponsoring the work.

## Procurement case with mixed modification types

A specialist creates a procurement case to handle updates across three items. Two of the case lines are routine description changes. The third documents a supplier change — a strategic decision with contract implications.

When the case is saved and its lines are evaluated, the two description change lines match Rule 3 and return Low. The supplier change line matches Rule 1 and returns High.

The system selects High as the priority for the parent case. When a manager reviews the team's open work queue, this case appears above the routine catalog-update cases — signaling that it contains at least one strategically significant line.

## Record with no matching rule

Before this organization finishes configuring the procurement case decision table, a procurement case is created. The table has no rules yet. The system evaluates the decision table, finds no matching rule, and the case receives Planning priority — the system default. It appears at the bottom of the work queue.

After the rules are configured in the table, the system re-evaluates the case the next time it is created or updated. If a matching rule is found, the priority updates accordingly.

This means work prioritization does not require all rules to be in place before the feature is active. Records created before rules are configured accumulate at Planning priority and are re-evaluated naturally as they are updated.

**Parent Topic:**[Work prioritization](work-prioritization.md)

