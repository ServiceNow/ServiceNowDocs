---
title: Evaluate Nacha operating guidelines with AI agent
description: The Nacha operating guidelines check AI agent verifies if a disputed ACH transaction qualifies for return under Nacha rules by checking required documents such as a valid Written Statement of Unauthorized Debit \(WSUD\) and ensuring actions occur within allowed time frames.
locale: en-US
release: australia
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Resolve ACH disputes with AI agents, ACH dispute AI agents overview, AI agents in FSO, Use agentic AI, Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Evaluate Nacha operating guidelines with AI agent

The Nacha operating guidelines check AI agent verifies if a disputed ACH transaction qualifies for return under Nacha rules by checking required documents such as a valid Written Statement of Unauthorized Debit \(WSUD\) and ensuring actions occur within allowed time frames.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent\_connector, sn\_bom\_credit\_card.dispute\_agent, and now\_assist\_panel\_user.

## About this task

This agent verifies if a disputed transaction meets established Nacha standardized rules and timelines from a knowledge article, then provides an eligibility recommendation for the dispute.

**Note:** This agent uses the knowledge article to evaluate the Nacha operating guidelines. The knowledge article is installed as part of the Nacha dispute content pack. For more information, see [Using Dispute Rules Content Pack for Nacha](../../dispute-content-pack-for-nacha/task/dispute-rules-content-pack-nacha-use.md). To enable this capability, make sure that the AI Search option is turned on.

## Procedure

1.  Navigate to **Workspaces** &gt; **Financial Services Workspace** and open a card dispute.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select the case you want to work on.

5.  Select the **Playbook** tab.

6.  In the **Processing** tab, select the transaction ID.

7.  If the task isn’t assigned to an agent and once the dispute agent selects **Assign to me** the AI agent is invoked.

    If the task is already assigned to the dispute agent, then the recommendations provided by the AI agent are automatically displayed.

8.  Based on the AI agent's analysis, the dispute agent can select these options on the workspace.

    -   **Apply Recommendation**: The dispute agent selects this option to accept the recommendation after reviewing the Nacha operating guidelines analysis.
    -   **Ask a follow up**: The dispute agent selects this option only if they aren’t sure about the analysis done and want to verify further. The analysis is then displayed in the Now Assist panel. ![Nacha eligibility](../image/now-assist-nacha-analysis.png)
9.  Once the dispute agent selects **Apply Recommendation** option for the selected transaction, the recommended **Outcome** and **Rationale** on the recommendation card component are copied to the **Final action** and **Resolution reason** respectively and the task is closed.

    **Note:** If the dispute agent disagrees with the analysis, then a rationale is prompted by the AI agent for the disagreement. On providing a valid rationale, the task proceeds to the next task.

    For information about Nacha operating guidelines in ACH disputes, see [Evaluate Nacha operating guidelines](../../fso-card-operations/task/fso-ach-evaluate-nacha.md)

    **Note:** You can also access the recommendation for the Nacha operating guidelines as follows.

    1.  Once the dispute agent selects **Assign to me**, a notification appears for that agent in the Now Assist panel.
    2.  Select the Now Assist panel icon \(![now assist panel icon](../../../common/image/icon-ai-sparkle.png)\) and open the active chat for the disputed transaction.

## Result

Based on the response from the dispute agent, the **Final action** field is updated as **Eligible** or **Ineligible**. The task navigates to the next task [Review ACH dispute return recommendation](recommendation-ai.md).

**Parent Topic:**[Resolve ACH disputes with AI agents](resolve-ach-disputes-with-ai-agents.md)

