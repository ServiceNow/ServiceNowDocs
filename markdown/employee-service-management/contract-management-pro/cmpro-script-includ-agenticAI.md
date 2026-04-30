---
title: Update the contracts AI agents handler script include
description: Update the ContractsAIAgentsHelper script include to add the sys\_id of a customized Manage contract repository agentic workflow to run the agentic workflow autonomously.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure agentic workflows, Configure, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Update the contracts AI agents handler script include

Update the ContractsAIAgentsHelper script include to add the sys\_id of a customized Manage contract repository agentic workflow to run the agentic workflow autonomously.

## Before you begin

Role required: admin

## About this task

When you duplicate the Manage contract repository agentic workflow and create a customized agentic workflow, you must add the sys\_id of the new agentic workflow in the ContractsAIAgentsHelper script include to run the agentic workflow autonomously.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

    The Script Includes table appears.

2.  In the Name column, search for `ContractsAIAgentsHelperSNC`.

3.  Open **ContractsAIAgentsHelperSNC**.

4.  In the **Script** box, copy the `startAiAgentConversation()` method.

    ![Script include for agentic workflow in CM Pro.](../image/cmpro-script-agentic-ai.png "Script include for agentic workflow")

5.  Navigate back to the Script Include table.

6.  In the Name column, search for `ContractsAIAgentsHelper`.

7.  Open **ContractsAIAgentsHelper**.

8.  In the **Script** box, paste the `startAiAgentConversation()` method.

9.  In usecaseId, add the sys\_id of the new agentic workflow.

    You can copy the sys\_id of the new agentic workflow from the Use case \[sn\_aia\_usecase\] table.

10. Select **Update**.


## Result

The customized Manage contract repository agentic workflow runs autonomously when all the trigger conditions are met.

For more information, see [Manage contract repository agentic workflow](../concept/cmpro-na-reminder-agentic-wf.md).

**Parent Topic:**[Configuring agentic workflows in Now Assist in Contract Management](../concept/cmpro-conf-agentic-workflow.md)

**Related topics**  


[Activate business rules for the Manage contract repository agentic workflow](conf-repository-agentic-ai.md)

[Set the default notice period for the Manage contract repository agentic workflow](conf-sys-prop-default-np.md)

[Enable notifications for AI extracted metadata and obligations](cmpro-na-me-agentic-ntf.md)

