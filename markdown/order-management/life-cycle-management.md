---
title: Customer contract life cycle
description: A customer contract goes through the various states in each phase of its life cycle.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customer Contracts and Entitlements reference, Configure, price, quote, Reference, Sales Customer Relationship Management]
---

# Customer contract life cycle

A customer contract goes through the various states in each phase of its life cycle.

In each state, a customer contract is enabled to perform certain actions as mentioned in the following table.

<table id="table_p1t_b12_nzb"><thead><tr><th>

Life-cycle

</th><th>

State

</th><th>

Action

</th></tr></thead><tbody><tr><td>

A customer contract is generated.

</td><td>

Draft

</td><td>

-   The start and end dates of the customer contract can be modified such that the child records' dates are within the date range.
-   The related contract lines and entitlements can be added, removed, or modified.
-   The sold product/install base item covered can be added or removed.

</td></tr><tr><td>

Customer contract gets activated on the date of activation.

</td><td>

Active

</td><td>

-   Modifications to the customer contract can be done manually, via integration and via Sales Customer Relationship Management workflow.
-   The start date can't be modified.
-   The end date can be extended and should be greater than the current date.
-   customer contract line items can be added.
-   The sold product/install base item covered can be modified.

</td></tr><tr><td>

Customer contract is deactivated on the date of expiration.

</td><td>

Expired

</td><td>

No action.

</td></tr><tr><td>

Customer contract is canceled.

</td><td>

Canceled

</td><td>

No action.

</td></tr></tbody>
</table>The customer contract line items and entitlements also perform similar actions in the respective states.

When a parent entity moves to the Expired state, the child entities inherit the same state. For example, when a customer contract expires, the related contract lines and entitlements also expire.

However, the state change of a child entity doesn't affect it parent entity.

The sold product or install base item referenced either in the contract line or an entitlement must be in the same state as the entity where it's referenced.

## Suspended state

When a sold product is suspended, the related customer contract lines and entitlements, in the Draft or Active states, move to the Suspended state as well.

A suspended customer contract line or entitlement is paused for any activity, except the following:

-   Editing the field values.
-   Creating records in the corresponding related lists.

On resuming the sold product, the related customer contract line item or entitlement acquires the state depending on its start and end dates. For example, a resumed entitlement that has its start date in the past and its end date in the future, acquires the Active state.

Exceptionally, when a contract line or entitlement in the Suspended state has reached its end date, it moves to the Expired state automatically.

## Date validations

A customer contract line associated with a customer contract must be created within the customer contract's start and end dates. Any modification to the dates of customer contract lines must comply with the date range of the parent service contract.

**Parent Topic:**[Customer Contracts and Entitlements reference](pss-reference.md)

