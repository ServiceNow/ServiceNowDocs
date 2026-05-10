---
title: Create recall corrective actions using Now Assist for Manufacturing Commercial Operations \(MCO\)
description: Create recall corrective actions AI agent extracts the information available in the repair documents. The AI agent identifies and collects all relevant data contained within the repair documents and generates the corrective action and the corresponding charges.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use generative AI, Now Assist for MCO, Manufacturing Commercial Operations]
---

# Create recall corrective actions using Now Assist for Manufacturing Commercial Operations \(MCO\)

Create recall corrective actions AI agent extracts the information available in the repair documents. The AI agent identifies and collects all relevant data contained within the repair documents and generates the corrective action and the corresponding charges.

## Before you begin

Role required: sn\_rcl\_claim\_mgmt.recall\_manager

## Procedure

1.  Navigate to ******Workspaces** &gt; **CSM/FSM Configurable Workspace** &gt; **Lists** &gt; **Recall Management**.

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

[Activate an agentic workflow template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-aia-use-case.md)

[Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md)

[Modify an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/modify-aia-use-case.md)

