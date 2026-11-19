---
title: Approval rule considerations
description: Factors like currency, which includes foreign exchange, reference, and transactional, decide the approval rules to be triggered. Some of the other factors are purchasing limit, line amount, and received lines, among others.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/source-to-pay-operations/sourcing-and-procurement-operations/approval-rule-considerations.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-10-28"
reading_time_minutes: 3
breadcrumb: [Create an approval rule, Sourcing and Purchasing Automation, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Approval rule considerations

Factors like currency, which includes foreign exchange, reference, and transactional, decide the approval rules to be triggered. Some of the other factors are purchasing limit, line amount, and received lines, among others.

## Foreign exchange and reference currency considerations in approval rules

If an approval rule has a defined approved purchasing limit, the foreign exchange currency is defaulted to the system reference currency.

To determine the approval rule to be triggered, compare the transactional currency on the **Total amount** field on the purchase requisition against the reference currency approval rule bucket that it belongs to.

If an approval rule has an approval trigger defined using the total line amount, it should be defined by dot-walking to the reference amount. The transactional currency on the purchase line's total line amount is compared against the reference currency, to determine the approval rule to be triggered.

**Note:** Do not define the approval trigger on the currency field of the total line amount. Approval rules that use the currency field instead of the reference amount might trigger inconsistently.

## Fully received lines consideration in approval rules

For a fully received line, the line amount is taken into consideration to determine the approval rule that needs to be triggered.

## Manager hierarchy considerations in approval rules

Approval rules that send requests to the requester's managers follow the **Manager** field on each user record, starting with the business owner of the purchase requisition. Make sure that the manager chain is valid:

-   The chain must not loop back on itself, for example, user A reports to user B and user B reports to user A. A loop prevents the approver list from being resolved, so no approval plan is created and the approval stays at **Not Requested**.
-   For the rule options that send the request up to a job level, the chain must reach a manager with the job code that matches the rule's job level. If the top of the chain is reached first, all managers found up to that point are used as approvers.
-   A user without a manager has no approver to receive the request when the rule is set to send the request to the direct manager.

## When no approval plan is generated

An approval plan is created for a rule only when both of the following are true:

-   At least one line of the approving object that has not yet been decided meets the rule's approval trigger conditions and is not already covered by another rule in the same approval group.
-   The rule resolves to at least one approving user. For example, a group with no members, a user without a manager, or an empty dynamic attribute results in no approver. Cost center manager rules are the exception to this check.

If no rule produces a plan, the purchase requisition does not wait for approval and moves to the next stage. If requisitions skip approval unexpectedly, review the active approval rules, their trigger conditions, and the approvers that each rule resolves to.

## Approving objects for approval rules

The **Approving object** field lists only the tables that are registered for approvals. Out of the box, approval plans are generated for purchase requisitions and the other registered objects, such as sourcing requests and invoices. Purchase orders are not registered, so approval rules cannot be defined for them without customization.

To make another table available as an approving object, register it through the `sn_shop.ApprovalObjectMappingsProvider` extension point. The mappings define the header-to-line relationship, state field, approved and rejected states, requester field, and states in which approval is no longer required.

**Parent Topic:**[Create an approval rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/sourcing-and-procurement-operations/create-approval-rule.md)

