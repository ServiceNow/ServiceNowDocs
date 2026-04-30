---
title: Create an AI Control Tower Playbook Workflow
description: Create an AI Control Tower Approval Playbook for Now Assist approvals to approve or reject an asset.
locale: en-US
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Now Assist, Gen AI, Generative AI, AI Governance, Now LLM, large language model]
breadcrumb: [Use, AI Control Tower, Enable AI experiences]
---

# Create an AI Control Tower Playbook Workflow

Create an AI Control Tower Approval Playbook for Now Assist approvals to approve or reject an asset.

## Before you begin

**Important:**

The AI Control Tower Approval Playbook for the Now Assist approval isn’t created manually. They’re automatically triggered when an approval request is created while the approval mandate is enabled. To automatically trigger, activate the Automatically trigger playbooks feature under configuration.

Role required: sn\_ai\_governance\_ai\_steward \(Authorized to create approval request\)

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Control Tower**.

2.  From the AI Control Tower, open the **AI assets** view.

3.  From the navigation menu of the AI assets view, navigate to Now Assist **Approvals** and open an Approval request record.

4.  Under the **Playbook** tab, you can see the Now Assist **Approvals** workflow.

    You can save the **Playbook** record using the **Save** option or select **Cancel approval request** to cancel the workflow during any step.

5.  **Review asset**- You can view all the details of an asset in review.

6.  Select **Next**.

    The approval status changes when the Review asset step is marked as complete.

7.  **Evaluate asset**- AI stewards can create and assign the approval tasks to other individual AI stewards to evaluate the assets.

    For information on creating a Now Assist approval task for evaluating assets, see .

    **Note:** You can **Copy** or **Delete** the tasks and create a task using the **New** option in the Approval tasks list.

8.  **Approval/Reject**- AI stewards can select the Risk score from the drop-down menu and enter the Close notes, while approving or rejecting an asset based on the evaluation of the tasks.

9.  Select **Reject** or **Approve asset** to complete the workflow.

    The **Risk score** and **Close notes** can't be modified after the **Approve/Reject** step is marked as complete.

    ![Approval Playbook](../image/ai-governance-playbook.png "Approval Playbook") ![]( "Approval Playbook")


## What to do next

If you need to activate any skill from Now Assist Admin, an approval request is now required. The AI Control Tower approvals are integrated with both the builder team on the Skill Kit and Now Assist Admin. You may only use models, skills, or AI systems that have been approved. Approval is granted when the "AI steward approval required" option is enabled.

**Parent Topic:**[Using AI Control Tower](../concept/using-ai-control-tower.md)

