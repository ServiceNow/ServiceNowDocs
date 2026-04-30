---
title: Resolve ACH disputes with AI agents
description: Use AI agents to streamline ACH dispute resolution in Now Assist for FSO.
locale: en-US
release: zurich
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: task
last_updated: "2025-10-29"
reading_time_minutes: 3
breadcrumb: [AI agents in FSO, Use agentic AI, Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Resolve ACH disputes with AI agents

Use AI agents to streamline ACH dispute resolution in Now Assist for FSO.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent\_connector and sn\_bom\_credit\_card.dispute\_agent.

## About this task

In the ACH dispute resolution workflow, once a dispute agent is assigned to a case and its related transactions, all tasks under that transaction are automatically assigned to that dispute agent, through an out-of-the-box assignment configuration. The corresponding AI agents are invoked automatically.

**Note:** Ensure that your assignment logic such as Advanced Work Assignment \(AWA\) is configured so that when a dispute case is assigned to an agent, all associated transactions are automatically assigned to the same agent. This alignment helps maintain consistency and speeds up case resolution.

If this configuration isn’t enabled, the dispute agent must manually assign each task to themselves by selecting **Assigned to Me** on a specific task, to activate the AI agent.

-   **Tools**: The agent has access to various tools, including:
    -   Knowledge base \(KB\) articles
    -   ACH disputes task details
    -   Previous cases of disputes
-   **Decision Making**: The human agent can follow a generated recommendation of the AI agent or make a different decision. If the human agent decides to deviate from the generated suggestion, they must provide a reason for their decision. The process includes declining recommendations, issuing credits, and communication templates for customer interaction.

## Procedure

1.  Navigate to **Workspaces** &gt; **Financial Services Workspace** and open a card dispute.

    The AI agents are invoked in the **Processing** stage based on the assignment of a task to the dispute agent.

2.  Based on the analysis done, these options are displayed on the workspace.

    -   **Apply Recommendation**: The dispute agent selects this option to agree with the recommended analysis of the AI agent. The task closes and navigates to the next task.
    -   **Ask a follow up**: The dispute agent selects this option only if they aren’t sure about the analysis done and want to verify further. The analysis is then displayed in the Now Assist panel.

        Select the Now Assist panel icon \(![now assist panel icon](../../../common/image/icon-ai-sparkle.png)\) and open the active chat for the disputed transaction.

        **Note:** If the dispute agent disagrees with the analysis, then a rationale is prompted by the AI agent for the disagreement. On providing a valid rationale, the task proceeds to the next task.

3.  Interact with the AI agent to continue resolving the case.

    You can continue working on the tasks as you interact with the AI agent.

    For information about how to resolve ACH disputes, see [Resolving ACH disputes](../../fso-card-operations/concept/work-dispute-ach.md).


## Result

Based on the resolution steps that the dispute agent selects, the dispute is either resolved or navigates to the next step of the dispute resolution.

-   **[Merchant analysis with AI agent](merchant-analysis-ai.md)**  
The Merchant analysis for disputes AI agent checks the credibility of the merchant in the context of the dispute, based on ratings and reviews from web search. If a web search returns no results for a merchant, then the merchant is classified as not credible.
-   **[Evaluate Nacha operating guidelines with AI agent](nacha-guidelines-ai.md)**  
The Nacha operating guidelines check AI agent verifies if a disputed ACH transaction qualifies for return under Nacha rules by checking required documents such as a valid Written Statement of Unauthorized Debit \(WSUD\) and ensuring actions occur within allowed time frames.
-   **[Review ACH dispute return recommendation](recommendation-ai.md)**  
The ACH dispute return recommendation AI agent analyzes disputed transactions based on merchant analysis and Nacha eligibility. The agent recommends actions based on historical data, and applies predefined rules when data is limited.
-   **[Dispute communication AI agent](dispute-communication-ai.md)**  
The Dispute communication AI agent automatically picks the appropriate email template for customer communication, including outcomes, denials, and follow-ups based on the transaction details.

**Parent Topic:**[Standalone AI agents in FSO](../concept/ai-agents-fso.md)

