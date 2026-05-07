---
title: Generate, accept, and reject risks using risk generation skill
description: Use generative AI to identify, generate, and manage potential risks in your project based on insights, resources, financials, and milestones.
locale: en-US
release: australia
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: task
last_updated: "2026-04-20"
reading_time_minutes: 2
breadcrumb: [Using Now Assist for Strategic Portfolio Management \(SPM\), Now Assist for Strategic Portfolio Management \(SPM\), Strategic Portfolio Management]
---

# Generate, accept, and reject risks using risk generation skill

Use generative AI to identify, generate, and manage potential risks in your project based on insights, resources, financials, and milestones.

## Before you begin

Role required: it\_project\_manager

-   Install Now Assist for Strategic Portfolio Management \(SPM\) plugin.
-   Verify risk generation skill is active.
-   The risk generation skill is activated by default. For more information on how to activate the skill if it isn't automatically activated or if you want to change the skill configuration, see [Configure Now Assist Admin features](../concept/configuring-na-spm.md).

## About this task

AI analyzes project data to identify potential risks and presents them for project manager review. AI-suggested risks are generated as part of the project insights cadence and appear in the AI Risks menu for project managers to accept or reject. AI generates risks by analyzing data from project insights, resources, financials, and milestones.

The AI Identified Risks menu is visible only to project managers when the risk generation skill is active. If no risks are identified during generation or regeneration, the AI Identified Risks page displays an empty state where you can generate risks again.

## Procedure

1.  Navigate to **Workspaces** &gt; **Project Workspace**.

2.  From Project Workspace, [Create a project](../../project-workspace/task/create-project-from-project-workspace.md) or open an existing project.

3.  Select **AI Identified Risks** from the navigation menu.

4.  Review the AI-suggested risks in the list and perform one of these actions:

    -   Regenerate: When you select regenerate option, the risk is generated again and added to the AI identified risks list. AI-generated risks appear in AI draft state.
    -   Accept: When you accept a risk, the approved risk appear in the RIDAC list and its state moves from AI Draft to Pending.
    -   Reject: When you reject a risk, the rejected risk is removed or hided from the AI identified risks list and its state moves to Closed skipped. The rejected risks are retained so that AI does not generate the same risk again.
    If no risks are identified during generation or regeneration, the AI identified risks page displays an empty state. In this case, you cannot regenerate risks immediately and are advised to revisit the page later as the project evolves.

5.  Select **Generate AI Risks** if no risks are identified for the project.

    ![AI-generated risks for a project.](../images/ai-generated-risks.png)


**Parent Topic:**[Using Now Assist for Strategic Portfolio Management \(SPM\)](../concept/using-now-assist-for-spm.md)

