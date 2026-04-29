---
title: Blocking a credit card
description: Credit card agents can work on a credit card case that blocks a customer's credit card as per the service request.
locale: en-US
release: australia
product: Financial Services Card Operations
classification: financial-services-card-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Card Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Blocking a credit card

Credit card agents can work on a credit card case that blocks a customer's credit card as per the service request.

When a customer requests to block a credit card, a credit card service case is created. The Block Credit Card flow is triggered that further creates the following tasks in the credit card service case. A new task is created when the credit card agent closes the previous task.

1.  [Block a credit card for a customer](../task/block-credit-card.md).

    **Note:** If the **Duration** field in the credit card service case is set to **Indefinitely**, blocking the credit limit closes the case and step 2 is not triggered.

2.  [Unblock a credit card](../task/unblock-credit-card.md).

    If the request is for only temporarily blocking the credit card, the case remains in the Work in Progress state and in the Update Account stage until the end date that is specified in the case. The system automatically creates a new credit card service case on the specified end date to unblock the card.

    The **sn\_bom\_credit\_card.reserverd\_hours\_to\_unblock\_credit\_card** [card property](../reference/properties-installed-card-ops.md) defines the number of hours before the end date when the system creates a case to unblock the credit card.


For more information on the flows that are installed with the Financial Services Card Operations application, see [Designer flows for Financial Services Operations applications](../../fso-common/reference/flow-designer-flows-fso-apps.md).

