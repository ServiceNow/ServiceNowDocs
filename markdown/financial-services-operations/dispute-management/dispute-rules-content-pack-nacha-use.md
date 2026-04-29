---
title: Using Dispute Rules Content Pack for Nacha
description: By using the Dispute Rules Content Pack for Nacha, your agents can help customers to determine the correct reason code for automated clearing house \(ACH\) transaction disputes based on Nacha operating guidelines. Agents use the predefined logic in the content pack, as well as a knowledge base article outlining the eligibility rules, required documentation, and timelines for each return code.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [use]
breadcrumb: [Dispute Rules Content Pack for Nacha, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Using Dispute Rules Content Pack for Nacha

By using the Dispute Rules Content Pack for Nacha, your agents can help customers to determine the correct reason code for automated clearing house \(ACH\) transaction disputes based on Nacha operating guidelines. Agents use the predefined logic in the content pack, as well as a knowledge base article outlining the eligibility rules, required documentation, and timelines for each return code.

## Overview of using Dispute Rules Content Pack for Nacha

When an agent disputes a transaction on behalf of a customer, a dispute service case begins and the dispute transaction flow is triggered. This flow includes the various tasks that are specific to the case details. As a task in the case is closed, the next task is created.

1.  [Create a dispute service case.](../../fso-card-operations/task/create-case-with-intake-workspace.md#)

    A new dispute case is raised by:

    -   The agent initiating the dispute service process by entering the initial case information and creating a dispute case on behalf of a customer.

    -   A customer raising a new case from the customer portal.

2.  [Initiate and submit a dispute.](../../fso-card-operations/task/create-case-with-intake-workspace.md#)

    The agent or the customer enters the dispute details, including the financial account, the disputed transactions, and answers to the dispute questionnaire. For an ACH dispute, the customer will also provide documented proof, including the Written Statement of Unauthorized Debit \(WSUD\). The case is then submitted for investigation.

3.  [Investigate the case.](../../fso-card-operations/concept/work-dispute-ach.md)

    The investigation agent follows the dispute investigation playbook and completes the activities, including issuing provisional credit, and reviewing Nacha operating guidelines.

    If [Now Assist for Financial Services Operations \(FSO\)](../../fso-common/concept/now-assist-for-financial-services-operations.md) is integrated in the workflow, AI agents will provide additional guidance, such as merchant analysis, insights into Nacha guidelines, and ACH dispute return recommendations.

    The agent will then file the return, deny the dispute, or follow up with the Originating Depository Financial Institution \(ODFI\).


## ACH chargeback eligibility rules Knowledge Base article

Dispute Rules Content Pack for Nacha includes a Knowledge Base article that contains a table of reason codes and the corresponding eligibility rules.

To access the knowledge base article:

1.  Navigate to **All** &gt; **Knowledge Center**
2.  Navigate to the knowledge base **Dispute Compliance Documents**.
3.  Open the knowledge base article **NACHA Operating Guidelines for Return Codes**.

Dispute agents may use the KB article to manually evaluate whether an ACH transaction is eligible for chargeback.

If [Now Assist for Financial Services Operations \(FSO\)](../../fso-common/concept/now-assist-for-financial-services-operations.md) is installed, an AI agent in the ACH disputes processing agentic workflow will refer to this KB article to recommend if a transaction is eligible for chargeback.

**Related topics**  


[Dispute Reason Codes](../reference/components-installed-with-dispute-rules-content-pack-for-nacha.md#section_upm_p2c_xgc)

[Using agentic workflows in Now Assist for Financial Services Operations \(FSO\)](../../fso-now-assist/concept/using-ai-agent-use-cases-in-now-assist-for-fso.md)

