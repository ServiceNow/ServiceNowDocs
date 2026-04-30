---
title: Using the Dispute Rules Content Pack for Mastercard
description: By using the Dispute Rules Content Pack for Mastercard's questionnaire, your agents can help customers complete the reason code mapping for their disputes. This mapping enables the agents to categorize the dispute and determine the chargeback eligibility according to the Mastercard Chargeback Guide.
locale: en-US
release: xanadu
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Dispute Rules Content Pack for Mastercard, Managing Mastercard disputes, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Using the Dispute Rules Content Pack for Mastercard

By using the Dispute Rules Content Pack for Mastercard's questionnaire, your agents can help customers complete the reason code mapping for their disputes. This mapping enables the agents to categorize the dispute and determine the chargeback eligibility according to the Mastercard Chargeback Guide.

## Dispute Rules Content Pack for Mastercard workflows

In the  Dispute Rules Content Pack for Mastercard, a dispute agent handles the following basic tasks:

-   Completes the intake of questionnaires based on dispute category
-   Uses the questionnaire to map the dispute reason code
-   Determines chargeback eligibility by completing the questionnaire and mapping the reason code

When an agent disputes a transaction on behalf of a customer, a dispute service case begins and the dispute card transaction flow is triggered. This flow includes the various tasks that are specific to the case details. Each task is created when an agent closes the previous task.

1.  Create a dispute service case.

    The agent initiates the dispute service process by entering the initial case information and creating a dispute case on behalf of a customer. For more information, see [Create a card dispute service case](../../fso-card-operations/task/create-dispute-service-case.md).

2.  Initiate a dispute.

    The agent enters the dispute details, including the account being referenced, the dispute amount, and the type of dispute. The agent provides the necessary information for the available options in the type of dispute \(Authorization, Point of Interaction Error, Fraud, Cardholder Disputes, Installment Billing Dispute, Cardholder Dispute Not Classified Elsewhere\). For more information, see [Initiate a dispute](../../fso-card-operations/task/initiating-dispute.md).

3.  Submit the case for investigation.

    The agent submits the case for investigation by reviewing the dispute amount, the dispute reason code, and the associated dispute reason code message.

    After submission, the agent can review the chargeback eligibility status and reason in the State of transactions panel or the **Card disputes transactions** tab.

    The following example shows the State of transactions panel.

    ![State of transactions panel that displays the disputed and resolved transactions for a card dispute.](../image/state-of-transactions-panel.png "State of transactions panel")


For more information, see [Submit for investigation](../../fso-card-operations/task/initiating-dispute.md).

**Parent Topic:**[Dispute Rules Content Pack for Mastercard](dispute-rules-content-pack-for-mastercard-landing-page.md)

