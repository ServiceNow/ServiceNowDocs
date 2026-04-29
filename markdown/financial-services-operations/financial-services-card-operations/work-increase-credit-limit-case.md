---
title: Increasing the credit limit of a card
description: As a credit card agent, you can work on a credit card case to increase the credit limit for a customer's credit card based on the findings from the customer's credit assessment.
locale: en-US
release: australia
product: Financial Services Card Operations
classification: financial-services-card-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Card Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Increasing the credit limit of a card

As a credit card agent, you can work on a credit card case to increase the credit limit for a customer's credit card based on the findings from the customer's credit assessment.

When a customer requests to increase a credit limit, a credit card service case is created and the Increase Credit Limit flow is triggered. This flow triggers the following tasks from the credit card service case. A new task is created when an agent closes the previous task.

1.  [Retrieve a credit assessment and evaluate the risks for a customer](../task/retrieve-credit-assessment-evaluate-risk.md).

    **Note:** If the credit assessment agent rejects the credit request, the stage of the associated credit card service case changes to Closed – Rejected. The case is automatically closed and the flow doesn't trigger the step 2.

2.  [Increase the credit limit for a customer](../task/increase-credit-limit.md).

    **Note:** If the **Duration** field in the associated case is set to **Indefinitely**, increasing the credit limit closes the case and step 3 is not triggered.

3.  [Reset the credit limit for a customer](../task/reset-credit-limit.md).

    If the request is for a temporary increase in the credit limit, the state of the case remains in the Work in Progress state and in the Update Account stage until the end date that is specified in the case. The system automatically creates a new credit card service case on the specified end date to reset the credit limit.

    The **sn\_bom\_credit\_card.reserverd\_hours\_to\_update\_credit\_limit** [card property](../reference/properties-installed-card-ops.md) defines the number of hours before the end date when the system creates a case to revert the credit limit.


For more information on the flows that are installed with the Financial Services Card Operations application, see [Designer flows for Financial Services Operations applications](../../fso-common/reference/flow-designer-flows-fso-apps.md).

