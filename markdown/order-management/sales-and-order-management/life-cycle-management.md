---
title: Service contract life cycle
description: A service contract goes through the various states in each phase of its life cycle.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Customer Contracts and Entitlements reference, Configure, price, quote, Reference, Sales Customer Relationship Management]
---

# Service contract life cycle

A service contract goes through the various states in each phase of its life cycle.

In each state, a service contract is enabled to perform certain actions as mentioned in the following table.

<table id="table_p1t_b12_nzb"><thead><tr><th>

Life-cycle

</th><th>

State

</th><th>

Action

</th></tr></thead><tbody><tr><td>

A service contract is generated.

</td><td>

Draft

</td><td>

-   The start and end dates of the service contract can be modified such that the child records' dates are within the date range.
-   The related contract lines and entitlements can be added, removed, or modified.
-   The sold product/install base item covered can be added or removed.

</td></tr><tr><td>

Service contract gets activated on the date of activation.

</td><td>

Active

</td><td>

-   Modifications to the service contract can be done manually, via integration and via Sales Customer Relationship Management workflow.
-   The start date can't be modified.
-   The end date can be extended and should be greater than the current date.
-   Service contract line items can be added.
-   The sold product/install base item covered can be modified.

</td></tr><tr><td>

Service contract is deactivated on the date of expiration.

</td><td>

Expired

</td><td>

No action.

</td></tr><tr><td>

Service contract is canceled.

</td><td>

Canceled

</td><td>

No action.

</td></tr></tbody>
</table>The service contract line items and entitlements also perform similar actions in the respective states.

When a parent entity moves to the Expired state, the child entities inherit the same state. For example, when a service contract expires, the related contract lines and entitlements also expire.

However, the state change of a child entity doesn't affect it parent entity.

The sold product or install base item referenced either in the contract line or an entitlement must be in the same state as the entity where it's referenced.

## Suspended state

When a sold product is suspended, the related service contract lines and entitlements, in the Draft or Active states, move to the Suspended state as well.

A suspended service contract line or entitlement is paused for any activity, except the following:

-   Editing the field values.
-   Creating records in the corresponding related lists.

On resuming the sold product, the related service contract line item or entitlement acquires the state depending on its start and end dates. For example, a resumed entitlement that has its start date in the past and its end date in the future, acquires the Active state.

Exceptionally, when a contract line or entitlement in the Suspended state has reached its end date, it moves to the Expired state automatically.

## Date validations

A service contract line associated with a service contract must be created within the service contract's start and end dates. Any modification to the dates of service contract lines must comply with the date range of the parent service contract.

**Parent Topic:**[Customer Contracts and Entitlements reference](pss-reference.md)

