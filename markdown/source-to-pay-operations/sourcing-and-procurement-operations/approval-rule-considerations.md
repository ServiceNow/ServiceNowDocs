---
title: Approval rule considerations
description: Factors like currency, which includes foreign exchange, reference, and transactional, decide the approval rules to be triggered. Some of the other factors are purchasing limit, line amount, and received lines, among others.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create an approval rule, Sourcing and Purchasing Automation, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Approval rule considerations

Factors like currency, which includes foreign exchange, reference, and transactional, decide the approval rules to be triggered. Some of the other factors are purchasing limit, line amount, and received lines, among others.

## Foreign exchange and reference currency considerations in approval rules

If an approval rule has a defined approved purchasing limit, the foreign exchange currency is defaulted to the system reference currency.

To determine the approval rule to be triggered, compare the transactional currency on the **Total amount** field on the purchase requisition against the reference currency approval rule bucket that it belongs to.

If an approval rule has an approval trigger defined using the total line amount, it should be defined by dot-walking to the reference amount. The transactional currency on the purchase line's total line amount is compared against the reference currency, to determine the approval rule to be triggered.

## Fully received lines consideration in approval rules

For a fully received line, the line amount is taken into consideration to determine the approval rule that needs to be triggered.

**Parent Topic:**[Create an approval rule](../task/create-approval-rule.md)

