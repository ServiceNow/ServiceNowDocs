---
title: Configure project insights generation skill in the AI Admin Hub console
description: Define the triggers, inputs, and display location for project insights generation skill.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/project-workspace/configure-project-insights-generation-skill.html
release: zurich
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2026-04-15"
reading_time_minutes: 1
breadcrumb: [Activate a AI skill, Use AI Admin Hub, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Configure project insights generation skill in the AI Admin Hub console

Define the triggers, inputs, and display location for project insights generation skill.

## Before you begin

Role required: admin

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

## Procedure

1.  Navigate to **Admin** &gt; **AI Admin Hub**.

    If you’re already in the AI Admin Hub console, select the **AI Skills** tab.

2.  On the navigation panel, select **Technology** and select **SPM**.

    Each workflow contains feature sets.

3.  On the Project insights generation feature card, select **Turn on**.

    \[Omitted image "edit-access-project-insights-generation.png"\] Alt text: Edit access screen for Project insights generation skill.

4.  In Add users access section, specify the user or roles.

5.  Review the role restrictions to skill and select **Turn on** to activate the skill.

    New topics in project insights framework to support reuse across portfolio insights, project insights, and status report contextual data:

    -   Project delays: Identifies delay patterns across your project timeline and reports them in project insights.
    -   Task dependency: Evaluates task relationships to highlight dependency risks and impacts.
    -   Budget fluctuations: Monitors budget changes and highlights significant variances for review.
    -   Scope creep: Detects insights of unplanned growth in a project by comparing the current project state against its first baseline. The insight flags deviations in task count, budget, and the existence of open change requests to help project managers identify potential scope expansion early.

## Result

The skill is active on the instance.

## What to do next

Analyze your skill performance and usage on the AI Admin Hub console to help determine the success of the skill. Learn more about tracking your AI usage at [Monitor AI usage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md).

**Parent Topic:**[Activate a AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-workspace/configure-now-assist-skill-spm.md)

