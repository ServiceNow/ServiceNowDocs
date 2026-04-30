---
title: Public Sector Digital Services AI agent collection Help manage public information requests workflow
description: Use the Help manage public information requests agentic workflow to generate an estimated fee breakdown for an information request case, or to determine whether a fee waiver should be granted.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Understanding Fee Estimation and Waiver Review workflow, Review Fee Estimation and Waiver, Fee Estimation and Waiver]
breadcrumb: [Using agentic workflows, Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Public Sector Digital Services AI agent collection Help manage public information requests workflow

Use the **Help manage public information requests** agentic workflow to generate an estimated fee breakdown for an information request case, or to determine whether a fee waiver should be granted.

You can use the **Help manage public information requests** agentic workflow to:

-   Estimate fees for information request case records by analyzing past cases and user input.
-   Analyze requests to waive the fees associated with an information request case.

This feature will estimate fees for information request cases by comparing similar case records and creating the estimate on those records, and calculating an estimate based on labor variables entered by the user. It then compares the requester's fee waiver justification against predefined criteria to recommend whether a fee waiver applies to the case.

## AI agents used in the Help manage public information requests workflow

The AI agents used for the **Help manage public information requests** agentic workflow are as follows:

|AI Agent name|Description|
|-------------|-----------|
|Information Request Fee Estimation AI Agent|Estimates and communicates the fee breakdown for an information request case record using similar request queries and details input by the user.|
|Information Request Fee Waiver Review AI Agent|Analyze and validate the fee waiver justification for an information request case record against a set of predefined rules from an external source and explain whether the request should be approved or rejected.|

To use the **Help manage public information requests** agentic workflow, you must confirm or perform the following:

1.  The Now Assist for Public Sector Digital Services \(PSDS\) plugin \(sn\_psds\_gen\_ai\) plugin is installed and configured.
2.  Navigate to **All** &gt; **Now Assist admin** &gt; **Skills** &gt; **PSDS**. On the Now Assist Experience tab, verify the Now Assist panel for users is turned on.

For more information, see [Install and configure Now Assist for Public Sector Digital Services \(PSDS\)](now-assist-psds-configuring.md).

To access the **Help manage public information requests** agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.
2.  Select **Help manage public information requests**.

To modify the agentic workflow, [duplicate it](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) by selecting the duplicate \(![](../image/duplicate_ai_agent_button_psds.png)\) icon, and adjust the settings according to your requirements. You can activate the duplicated agentic workflow template by making triggers active and setting the display settings to include the Now Assist panel.

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

## Roles required to activate and access the workflow

The roles required to activate and access the workflow are as follows:

<table id="table_cnc_nyr_dfc"><thead><tr><th>

Roles

</th><th>

Responsibilities

</th></tr></thead><tbody><tr><td>

PSDS AI admin \[sn\_gsm\_ai\_agents.admin\]

</td><td>

-   Configure the agentic workflow.
-   Change AI settings.
-   Create and manage new workflows and AI agents.
-   Access and update Autonomous AI Assistant tables.

</td></tr><tr><td>

PSDS AI agent \[sn\_aia\_agent\]

</td><td>

Read, create, update, and delete records in the AI agent table.

</td></tr><tr><td>

PSDS Information Request Manager \[sn\_gsm\_info\_req.manager\]

</td><td>

Receive output from the AI agents.

</td></tr></tbody>
</table>## Activating the agentic workflow

To activate the agentic workflow, perform the following steps:

1.  Navigate to agentic workflow **Help manage public information requests** and duplicate it. It duplicates any triggers associated with that agentic workflow.
2.  Navigate to the duplicated workflow and activate the trigger **Information Request Fee Estimation and Review is created or updated**.

