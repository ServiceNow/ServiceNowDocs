---
title: Generate, accept, and reject risks
description: Use generative AI to identify, generate, and manage potential risks in your project based on insights, resources, financials, milestones, and work notes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-workspace/generate-risks-using-ai-pw.html
release: australia
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2026-04-20"
reading_time_minutes: 2
breadcrumb: [Manage RIDAC, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Generate, accept, and reject risks

Use generative AI to identify, generate, and manage potential risks in your project based on insights, resources, financials, milestones, and work notes.

\[Omitted video\] Description: AI identified risks in Project Workspace.

## Before you begin

Role required: it\_project\_manager

-   Install ServiceNow Otto for Strategic Portfolio Management plugin.
-   Verify risk generation skill is active.
-   The risk generation skill is activated by default. For more information on how to activate the skill if it isn't automatically activated or if you want to change the skill configuration, see [Configure AI Admin Hub]().

## About this task

AI analyzes project data to identify potential risks and presents them for project manager review. AI-suggested risks are generated as part of the project insights cadence and appear in the AI Risks menu for project managers to accept or reject. AI generates risks by analyzing data from project insights, resources, financials, and milestones.

The AI Identified Risks menu is visible only to project managers when the risk generation skill is active. If no risks are identified during generation or regeneration, the AI Identified Risks page displays an empty state where you can generate risks again.

## Procedure

1.  Navigate to **Workspaces** &gt; **Project Workspace**.

2.  From Project Workspace, [Create a project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/create-project-from-project-workspace.md) or open an existing project.

3.  Select **AI Identified Risks** from the navigation menu.

4.  Review the AI-suggested risks in the list and perform one of these actions:

    -   Regenerate: When you select regenerate option, the risk is generated again and added to the AI identified risks list. AI-generated risks appear in AI draft state.
    -   Accept: When you accept a risk, the approved risk appear in the RIDAC list and its state moves from AI Draft to Pending.
    -   Reject: When you reject a risk, the rejected risk is removed or hided from the AI identified risks list and its state moves to Closed skipped. The rejected risks are retained so that AI does not generate the same risk again.
    If no risks are identified during generation or regeneration, the AI identified risks page displays an empty state. In this case, you can't regenerate risks immediately and are advised to revisit the page later as the project evolves.

5.  Select **Generate AI Risks** if no risks are identified for the project.

    \[Omitted image "ai-generated-risks.png"\] Alt text: AI-generated risks for a project.

    You can select any task ID, resource ID, or other reference in the AI Rationale column of AI project risks. This navigates directly to the related record without searching for the ID manually.


**Parent Topic:**[Manage Risk, Issue, Decision, Action, or Request Change \(RIDAC\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/manage-ridac-pw.md)

