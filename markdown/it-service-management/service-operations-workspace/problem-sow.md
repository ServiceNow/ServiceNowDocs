---
title: Problem Management in Service Operations Workspace
description: When you have recurring incidents or a major incident, you can create a problem to identify the root cause of the incidents and help prevent them from happening again. Use Service Operations Workspace to manage problems through their life cycle, share workarounds or fixes with related incidents, and create known error articles to help deflect incidents.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Managing IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Problem Management in Service Operations Workspace

When you have recurring incidents or a major incident, you can create a problem to identify the root cause of the incidents and help prevent them from happening again. Use Service Operations Workspace to manage problems through their life cycle, share workarounds or fixes with related incidents, and create known error articles to help deflect incidents.

![Problem record in Service Operations Workspace](../image/problem-sow.png "Problem record in Service Operations Workspace")

## Overview tab

This tab displays the following information about a problem:

-   Summary
-   Analysis information
-   Resolution information
-   Problem tasks and fix tasks
-   Impact
-   Work notes

You can configure the problem record overview tab and its UI elements in the Service Operations Workspace Admin Center. For more information, see [Manage configurations in Service Operations Workspace for ITSM](../task/manage-admin-console-sow-itsm.md).

You can optionally enable the following shortcuts, accessible from both the header and **Tasks \(problem and fix\)** drop-down menus:

-   **Create defect** \(for more information and requirements, see [Agile Development 2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/agile-development/agile-landing-page.md)\)
-   **Create enhancement** \(for more information and requirements, see [Agile Development 2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/agile-development/agile-landing-page.md)\)
-   **Create improvement initiative** \(for more information and requirements, see [Continual Improvement Management](../../continual-improvement-management/concept/cim-landing-page.md)\)

For all other configuration options, see [Configuring Problem Management in Service Operations Workspace](configuring-problem-management-sow.md).

## Details tab

This section displays the detailed information of a problem. For information about fields in this section, see [Create a problem in Service Operations Workspace](../task/create-problem-sow.md).

From the **Compose** section, you can add work notes for the problem.

All fields that are available on the Problem form in ServiceNow AI Platform are available in Service Operations Workspace. However, on the problem form in Service Operations Workspace, the **State** field is read-only. For information about state transitions of a problem, see [Life cycle of a problem](../../problem-management/concept/understanding-state-mgmt-transitions.md).

For information on how you can configure fields in this tab, see [Configuring Problem Management in Service Operations Workspace](configuring-problem-management-sow.md).

## Problem Tasks tab

This section displays problems tasks associated with this problem. Problem tasks are created when you need help from other teams to identify a fix for the problem. For information about creating a problem task, see [Create a problem task in Service Operations Workspace](../task/create-problem-task-sow.md).

## Fix Tasks tab

This section displays fix tasks associated with the problem. In Service Operations Workspace, only change requests are configured as fix tasks. For information about the **List of related task records \(comma-separated\) to track as fixes for this Problem** property where the fix tasks are configured, see [Configure properties for Problem Management in Service Operations Workspace](../task/configure-problem-properties-sow.md).

## Related records tab

This section displays the following records related to the problem. You can add a record, create a record, or remove it from the problem.

-   Incidents
-   Affected CIs
-   Outages
-   Knowledge attached from Agent Assist

## Contextual side panel

From this section, you can access Agent assist and search for relevant records and perform the required actions.

For more information about Problem Management, see [Problem Management](../../problem-management/concept/c_ProblemManagement.md).

-   **[Create a problem in Service Operations Workspace](../task/create-problem-sow.md)**  
Investigate the root cause of recurring incidents or a major incident. Provide a permanent fix to help prevent them from happening again.
-   **[Work on a problem in Service Operations Workspace](../task/work-on-problem-sow.md)**  
Manage problems and problem tasks through their life cycle, share workarounds or fixes with related incidents, and create known error articles to help deflect incidents.
-   **[Problem Management models in Service Operations Workspace](problem-mgmt-models-sow.md)**  
You can use Problem Management models to tailor processes for specific use cases.
-   **[Create a problem task in Service Operations Workspace](../task/create-problem-task-sow.md)**  
When you need to engage another team or agent for help, create and assign a problem task.
-   **[Work on a problem task in Service Operations Workspace](../task/work-on-problem-task-sow.md)**  
Manage problems and problem tasks through their life cycle, share workarounds or fixes with related incidents, and create known error articles to help deflect incidents.
-   **[Problem Management in Service Operations Workspace reference](reference-problem-management-sow.md)**  
Reference topics provide additional information about Problem Management in Service Operations Workspace.

**Parent Topic:**[Managing IT services in your organization](managing-services-operations-in-organization.md)

**Related topics**  


[Knowledge Management in Service Operations Workspace](knowledge-articles-sow.md)

[Major Incident Management in Service Operations Workspace](mim-in-sow.md)

[On-Call Scheduling in Service Operations Workspace](on-call-scheduling-in-sow.md)

[Recommendation Framework in Service Operations Workspace](recommendation-framework-sow.md)

[Recommended Actions for ITSM in Service Operations Workspace](recommended-actions-for-itsm-in-service-operations-workspace.md)

[ServiceNow integrations with Microsoft Teams in Service Operations Workspace](msteams-sow.md)

[Service Level Management in Service Operations Workspace](slm-sow.md#)

[Walk-up Experience management in Service Operations Workspace](walkup-sow.md)

[Collaboration in Service Operations Workspace](collaboration-sow.md)

[Computer Telephony Integration in Service Operations Workspace](configure-cti-sow.md)

[Universal Request in Service Operations Workspace](using-ur-sow.md)

[Universal Task in Service Operations Workspace](using-ut-sow.md)

[Resetting password using Service-desk assisted Password Reset in Service Operations Workspace](resetting-password-pr-sow.md)

