---
title: Onboard the AIOps specialist
description: Add the AIOps specialist to your team so it can start receiving and acting on alerts by assigning it a name, a role, and one or more teams.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/onboard-ai-specialist.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [onboard, AI specialist, AIOps, NOC]
breadcrumb: [AIOps AI Specialist, ITOM AIOps specialists, AI in ITOM AIOps, ITOM AIOps, IT Operations Management]
---

# Onboard the AIOps specialist

Add the AIOps specialist to your team so it can start receiving and acting on alerts by assigning it a name, a role, and one or more teams.

## Before you begin

Very you have the following setting

-   Platform version Brazil Patch 2 or later.
-   ServiceNow Otto for IT Operations Management \(ITOM\) application, version 2.10.0 or later.
-   AIOps Experience application, version 27.2.68 or later.
-   AIOps AI Specialist \(sn\_ai\_aiops\_force\) plugin, version 3.0.0 or later.

-   Create a team in your instance to which you want to add the AIOps specialist.

**Important:** AIOps AI Specialist isn't supported on domain-separated instances. For more information, see [Domain separation support for AIOps AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/ai-specialist-aiops-overview.md).

Role required: evt\_mgmt\_admin or evt\_aiops\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  On your homepage, select **Onboard a new team member**.

3.  In the AIOps AI Specialist tile, select **Add to team**.

    You're now on the AIOps AI Specialist page.

    \[Omitted image "ai-specialist-profile.png"\] Alt text: AIOps AI Specialist profile page.

4.  Enter a name for the AI specialist by clicking the edit icon \(\[Omitted image "icon-edit.png"\] Alt text: Edit icon\).

    **Tip:** Use a name that helps your team identify it at a glance. For example, "NOC AI specialist" or "AIOps Tier-1 Worker". Choose a name that reflects what the AI specialist handles, not just that it is an AI. For example, "Network AI specialist" or "DB Alert AI specialist" makes it easier to distinguish multiple AI specialists in the team view.

5.  In the Assignment groups section, select one of the following options:

    -   **Add specialist to specific group\(s\)**: Select this to limit the AI specialist to handling alerts from only the assignment groups you choose.
    -   **All groups**: Select this to let the AI specialist handle alerts from all assignment groups.
6.  Review the role assignment.

    The AI specialist is assigned the Operator role \(evt\_mgmt\_operator\) by default.

7.  Clear the **Handle unassigned alerts** check box if you don't want the AI specialist to handle alerts that aren't assigned to any assignment group.

8.  Select **Save**.

    **Note:** If you have been using the Manage Alerts Autonomously agentic workflow, activating the AI specialist disables the workflow and the AI specialist takes over the work.


## What to do next

Configure the AI specialist's alert scope and task modules before activating it. See [Configure alert scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/configure-alert-scope-ai-specialist.md) and [Configure task modules for the AIOps AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/configure-task-modules-ai-specialist.md).

-   **[Configure alert scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/configure-alert-scope-ai-specialist.md)**  
Define which alerts your AI specialist receives by setting filter conditions—the AI specialist is only assigned alerts that match all active conditions.
-   **[AIOps AI Specialist's task modules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/task-modules.md)**  
Task modules are the AI Specialist's built-in capabilities. Each module handles a distinct part of the alert lifecycle, and you control which modules are active and how they behave.
-   **[Configure task modules for the AIOps AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/configure-task-modules-ai-specialist.md)**  
Enable and configure the AI Specialist's capabilities by activating the Deflect, Investigate, and Remediate modules that control what the AI Specialist does when it receives an alert.
-   **[Test and activate the AIOps AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/test-activate-ai-specialist.md)**  
Run the AI Specialist with a real alert to preview its output before it goes live as an active member of your NOC team.

**Parent Topic:**[AIOps AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/ai-specialist-aiops-overview.md)

