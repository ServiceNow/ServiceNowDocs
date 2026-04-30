---
title: Setting up a new credit card account
description: As a credit card agent, you can work on a credit card case to validate the customer information and set up a new credit card account for the customer.
locale: en-US
release: xanadu
product: Financial Services Card Operations
classification: financial-services-card-operations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing credit card service requests, Financial Services Card Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Setting up a new credit card account

As a credit card agent, you can work on a credit card case to validate the customer information and set up a new credit card account for the customer.

When a customer requests a new credit card, a credit card service case is created and the New Credit Card flow is triggered. This flow triggers the following tasks from the credit card service case. A new task is created when an agent closes the previous task.

1.  [Evaluate the product eligibility for a customer](../task/evaluate-product-eligibility.md).
2.  [Retrieve a credit assessment and evaluate the risks for a customer](../task/retrieve-credit-assessment-evaluate-risk.md).

    **Note:** If the credit assessment agent rejects the credit request, the stage of the associated credit card service case changes to Closed – Rejected. The case is automatically closed and the flow doesn't trigger steps 3–6.

3.  [Check the completeness of the supporting documents for a customer](../task/check-completeness-supporting-documents.md).
4.  [Determine a card's Terms and Conditions and Disclosures for a customer](../task/determine-card-terms-conditions-disclosures.md).
5.  [File a customer agreement for a customer](../task/file-customer-agreement.md).
6.  [Set up a credit card account for a customer and close the case](../task/set-up-credit-card-account.md).

For more information on the flows that are installed with the Financial Services Card Operations application, see [Designer flows for Financial Services Operations applications](../../fso-common/reference/flow-designer-flows-fso-apps.md).

