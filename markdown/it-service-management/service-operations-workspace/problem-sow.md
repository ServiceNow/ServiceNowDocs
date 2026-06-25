---
title: Problem Management in Service Operations Workspace
description: When you have recurring incidents or a major incident, you can create a problem to identify the root cause of the incidents and help prevent them from happening again. Use Service Operations Workspace to manage problems through their life cycle, share workarounds or fixes with related incidents, and create known error articles to help deflect incidents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-operations-workspace/problem-sow.html
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

\[Omitted image "problem-sow.png"\] Alt text: Problem record in Service Operations Workspace

## Overview tab

This tab displays the following information about a problem:

-   Summary
-   Analysis information
-   Resolution information
-   Problem tasks and fix tasks
-   Impact
-   Work notes

You can configure the problem record overview tab and its UI elements in the Service Operations Workspace Admin Center. For more information, see [Manage configurations in Service Operations Workspace for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/manage-admin-console-sow-itsm.md).

You can optionally enable the following shortcuts, accessible from both the header and **Tasks \(problem and fix\)** drop-down menus:

-   **Create defect** \(for more information and requirements, see [Agile Development 2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/agile-landing-page.md)\)
-   **Create enhancement** \(for more information and requirements, see [Agile Development 2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/agile-landing-page.md)\)
-   **Create improvement initiative** \(for more information and requirements, see [Continual Improvement Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/continual-improvement-management/cim-landing-page.md)\)

For all other configuration options, see [Configuring Problem Management in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/configuring-problem-management-sow.md).

## Details tab

This section displays the detailed information of a problem. For information about fields in this section, see [Create a problem in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/create-problem-sow.md).

From the **Compose** section, you can add work notes for the problem.

All fields that are available on the Problem form in ServiceNow AI Platform are available in Service Operations Workspace. However, on the problem form in Service Operations Workspace, the **State** field is read-only. For information about state transitions of a problem, see [Life cycle of a problem](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/problem-management/understanding-state-mgmt-transitions.md).

For information on how you can configure fields in this tab, see [Configuring Problem Management in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/configuring-problem-management-sow.md).

## Problem Tasks tab

This section displays problems tasks associated with this problem. Problem tasks are created when you need help from other teams to identify a fix for the problem. For information about creating a problem task, see [Create a problem task in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/create-problem-task-sow.md).

## Fix Tasks tab

This section displays fix tasks associated with the problem. In Service Operations Workspace, only change requests are configured as fix tasks. For information about the **List of related task records \(comma-separated\) to track as fixes for this Problem** property where the fix tasks are configured, see [Configure properties for Problem Management in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/configure-problem-properties-sow.md).

## Related records tab

This section displays the following records related to the problem. You can add a record, create a record, or remove it from the problem.

-   Incidents
-   Affected CIs
-   Outages
-   Knowledge attached from Agent Assist

## Contextual side panel

From this section, you can access Agent assist and search for relevant records and perform the required actions.

For more information about Problem Management, see [Problem Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/problem-management/c_ProblemManagement.md).

-   **[Create a problem in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/create-problem-sow.md)**  
Investigate the root cause of recurring incidents or a major incident. Provide a permanent fix to help prevent them from happening again.
-   **[Work on a problem in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/work-on-problem-sow.md)**  
Manage problems and problem tasks through their life cycle, share workarounds or fixes with related incidents, and create known error articles to help deflect incidents.
-   **[Problem Management models in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/problem-mgmt-models-sow.md)**  
You can use Problem Management models to tailor processes for specific use cases.
-   **[Create a problem task in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/create-problem-task-sow.md)**  
When you need to engage another team or agent for help, create and assign a problem task.
-   **[Work on a problem task in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/work-on-problem-task-sow.md)**  
Manage problems and problem tasks through their life cycle, share workarounds or fixes with related incidents, and create known error articles to help deflect incidents.
-   **[Problem Management in Service Operations Workspace reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/reference-problem-management-sow.md)**  
Reference topics provide additional information about Problem Management in Service Operations Workspace.

**Parent Topic:**[Managing IT services in your organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/managing-services-operations-in-organization.md)

**Related topics**  


[Knowledge Management in Service Operations Workspace]()

[Major Incident Management in Service Operations Workspace]()

[On-Call Scheduling in Service Operations Workspace]()

[Recommendation Framework in Service Operations Workspace]()

[Recommended Actions for ITSM in Service Operations Workspace]()

[ServiceNow integrations with Microsoft Teams in Service Operations Workspace]()

[Service Level Management in Service Operations Workspace]()

[Walk-up Experience management in Service Operations Workspace]()

[Collaboration in Service Operations Workspace]()

[Computer Telephony Integration in Service Operations Workspace]()

[Universal Request in Service Operations Workspace]()

[Universal Task in Service Operations Workspace]()

[Resetting password using Service-desk assisted Password Reset in Service Operations Workspace]()

