---
title: Generate, accept, and reject risks using risk generation skill
description: Use generative AI to identify, generate, and manage potential risks in your project based on insights, resources, financials, and milestones.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-workspace/generate-risks-using-ai-pw.html
release: australia
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2026-04-20"
reading_time_minutes: 1
breadcrumb: [Managing projects with Project Workspace, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Generate, accept, and reject risks using risk generation skill

Use generative AI to identify, generate, and manage potential risks in your project based on insights, resources, financials, and milestones.

AI identified risks in Project Workspace. 

## Before you begin

Role required: it\_project\_manager

-   Install Now Assist for Strategic Portfolio Management \(SPM\) plugin.
-   Verify risk generation skill is active.
-   The risk generation skill is activated by default. For more information on how to activate the skill if it isn't automatically activated or if you want to change the skill configuration, see [Configure Now Assist Admin features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/configuring-na-spm.md).

## About this task

AI analyzes project data to identify potential risks and presents them for project manager review. AI-suggested risks are generated as part of the project insights cadence and appear in the AI Identified Risks menu for project managers to accept or reject. AI generates risks by analyzing data from project insights, resources, financials, and milestones.

If no risks are identified during generation or regeneration, the AI Identified Risks page displays an empty state where you can generate risks again as project evolves.

## Procedure

1.  Navigate to **Workspaces** &gt; **Project Workspace**.

2.  From Project Workspace, [Create a project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/create-project-from-project-workspace.md) or open an existing project.

3.  Select **AI Identified Risks** from the navigation menu.

4.  Review the AI-suggested risks in the list and perform one of these actions:

    -   Regenerate: When you select regenerate option, the risk is generated again and added to the AI identified risks list. AI-generated risks appear in AI draft state.
    -   Accept: When you accept a risk, the approved risk appear in the RIDAC list and its state moves from AI Draft to Pending.
    -   Reject: When you reject a risk, the rejected risk is removed or hided from the AI identified risks list and its state moves to Closed skipped.
5.  Select **Generate AI Risks** if no risks are identified for the project.

    \[Omitted image "ai-generated-risks.png"\] Alt text: AI-generated risks for a project.

    You can select any task ID, resource ID, or other reference in the AI Rationale column of AI project risks to navigate directly to the related record.


**Parent Topic:**[Managing projects with Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/use-projects-pw.md)

