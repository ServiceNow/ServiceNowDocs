---
title: Update the contracts AI agents handler script include
description: Update the ContractsAIAgentsHelper script include to add the sys\_id of a customized Manage contract repository agentic workflow to run the agentic workflow autonomously.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-04-18"
reading_time_minutes: 1
breadcrumb: [Configure agentic workflows, Configure, Now Assist in CM Pro, Contract Management Pro, Employee Service Management]
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

5.  Navigate back to the Script Include table.

6.  In the Name column, search for `ContractsAIAgentsHelper`.

7.  Open **ContractsAIAgentsHelper**.

8.  In the **Script** box, paste the `startAiAgentConversation()` method.

9.  In usecaseId, add the sys\_id of the new agentic workflow.

    You can copy the sys\_id of the new agentic workflow from the Use case \[sn\_aia\_usecase\] table.

10. Select **Update**.


**Parent Topic:**[Configuring agentic workflows in Now Assist in Contract Management](../concept/cmpro-conf-agentic-workflow.md)

