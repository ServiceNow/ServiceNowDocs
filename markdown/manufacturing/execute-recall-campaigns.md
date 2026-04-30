---
title: Execute recall campaigns faster Agentic Workflow
description: Use MCO AI agents agentic workflow to generate the corrective actions and charges for the required repair documents quickly and efficiently.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-11-04"
reading_time_minutes: 1
breadcrumb: [Use agentic workflows, Now Assist for MCO, Manufacturing Commercial Operations]
---

# Execute recall campaigns faster Agentic Workflow

Use MCO AI agents agentic workflow to generate the corrective actions and charges for the required repair documents quickly and efficiently.

## Before you begin

Role required: sn\_rcl\_claim\_mgmt.recall\_manager

## About this task

The Execute recall campaigns faster workflow uses the Create Recall Corrective Actions AI agent to streamline recalls by automatically extracting information from uploaded repair documents. This agent systematically identifies and gathers all relevant data from the repair instructions, reducing the need for manual input. As a result, corrective actions are created efficiently, and related charges are calculated accurately. This automation speeds up the process and helps minimize human error.

The recall manager can initiate a recall campaign and associate repair instruction documents with the campaign record. When prompted to add documents, the AI agent requests you to select from the available attachments. You can select the relevant documents. Also, you can upload the additional documentation necessary for implementing corrective actions.

The asset applicability criteria specify which corrective actions apply to a specific subset of the affected asset.

## Procedure

1.  Navigate to **All****Workspaces** &gt; **CSM/FSM Configurable Workspace** &gt; **Lists** &gt; **Recall Management**.

2.  Create a recall campaign record.

3.  Select the Now Assist icon ![](../../../common/image/icon-ai-sparkle.png) to launch the Now Assist panel.

4.  Submit a request to initiate a corrective action.

    The orchestrator activates the Create Recall Corrective Actions AI Agent, prompting you to proceed with the creation of the corrective action.

5.  The agent prompts the user to upload the repair documents required for generating the corrective actions.

6.  The agent reviews the uploaded documents.

    **Note:** If information is missing, the agent displays an error message and provides clear instructions for resolution.

    This process is repeated until all the required information is provided.

7.  The agent generates the corrective action and associated charges.

    All the corrective actions are generated along with the different charges \(labor, part, miscellaneous, and external services\).


**Related topics**  


[Create a campaign](../../mftg-manufacturing/concept/mco-rc-my-campaigns.md)

[Activate an agentic workflow template](https://www.servicenow.com/docs/access?context=activate-aia-use-case&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

[Duplicate an agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

[Modify an agentic workflow](https://www.servicenow.com/docs/access?context=modify-aia-use-case&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

