---
title: Review ACH dispute return recommendation
description: The ACH dispute return recommendation AI agent analyzes disputed transactions based on merchant analysis and Nacha eligibility. The agent recommends actions based on historical data, and applies predefined rules when data is limited.
locale: en-US
release: zurich
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: task
last_updated: "2025-10-27"
reading_time_minutes: 2
breadcrumb: [Resolve ACH disputes with AI agents, AI agents in FSO, Use agentic AI, Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Review ACH dispute return recommendation

The ACH dispute return recommendation AI agent analyzes disputed transactions based on merchant analysis and Nacha eligibility. The agent recommends actions based on historical data, and applies predefined rules when data is limited.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent\_connector, sn\_bom\_credit\_card.dispute\_agent, and now\_assist\_panel\_user.

## About this task

This agent reviews past disputes with similar transaction values to recommend an action: **Deny, File return**, or **Follow up with ODFI** along with a reason for the recommendation.

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

    **Note:** If the task is already assigned to the dispute agent, then the recommendations provided by the AI agent are automatically displayed.

8.  The AI agent prompts for one of these actions:

    -   **Deny**
    -   **File Return**
    -   **Followup ODFI**
    ![Recommendation AI agent](../image/now-assist-recommend-analysis.png)

9.  Based on the AI agent's analysis, the dispute agent can select these options on the workspace.

    -   **Apply Recommendation**: The dispute agent selects this option to accept the recommendation after reviewing the analysis.
    -   **Ask a follow up**: The dispute agent selects this option only if they aren’t sure about the analysis done and want to verify further. The analysis is then displayed in the Now Assist panel.
10. Once the dispute agent selects **Apply Recommendation** option for the selected transaction, the recommended **Outcome** and **Rationale** on the recommendation card component are copied to the **Final action** and **Resolution reason** respectively and the task is closed.

11. You can also access the recommendation for the analysis as follows.

    1.  Select the Now Assist panel icon \(![now assist panel icon](../../../common/image/icon-ai-sparkle.png)\) and open the active chat for the disputed transaction.
    2.  In the chat, the AI agent generates a recommendation for the dispute with a rationale.

        **Note:** If the dispute agent disagrees with the analysis, then a rationale is prompted by the AI agent for the disagreement. On providing a valid rationale, the task proceeds to the next task.

12. Once the dispute agent selects the appropriate action, the **ACH dispute return recommendation action** is updated with the **Final action** and **Resolution reason**.

    For information about recommendation analysis in ACH disputes, see and [Review ACH dispute return recommendation](../../fso-card-operations/task/fso-ach-review-recommendation.md).


## Result

Based on the response from the dispute agent, the **Final action** field is updated with one of the following options: **File return**, **Deny**, or **Followup ODFI** and the workflow moves to the next task or [Dispute communication AI agent](dispute-communication-ai.md).

**Parent Topic:**[Resolve ACH disputes with AI agents](resolve-ach-disputes-with-ai-agents.md)

