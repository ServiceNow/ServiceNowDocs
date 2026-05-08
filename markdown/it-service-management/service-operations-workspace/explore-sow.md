---
title: Exploring Service Operations Workspace for ITSM
description: You can have a unified and seamless experience when managing the life cycle of task records such as incidents, requests, and walk-ups in IT Service Management workflows using Service Operations Workspace \(SOW\) for ITSM.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Service Operations Workspace for ITSM, IT Service Management]
---

# Exploring Service Operations Workspace for ITSM

You can have a unified and seamless experience when managing the life cycle of task records such as incidents, requests, and walk-ups in IT Service Management workflows using Service Operations Workspace \(SOW\) for ITSM.

## Service Operations Workspace for ITSM overview

Service Operations Workspace for ITSM is a configurable workspace that provides a unified experience for multiple IT Service Management and IT Operations Management workflows. Configure your agent experience using the easy-to-navigate interface of Service Operations Workspace for ITSM.

## Accessing Service Operations Workspace for ITSM

For information about accessing Service Operations Workspace for ITSM, see [Access Service Operations Workspace for ITSM](../task/access-sow-itsm.md).

## Service Operations Workspace for ITSM users

<table id="table_jrc_mdf_ccc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tier 1 agent

</td><td>

User who has the itil or sn\_sow.sow\_home role and belongs to a service desk group.Primarily focused on the life cycle of the following records:

-   Interaction
-   Incident
-   Request

</td></tr><tr><td>

Tier 2 agent

</td><td>

User with the itil role.Primarily focused on the life cycle of the following records:

-   Incident
-   Request
-   Change
-   Problem
-   Major incident

</td></tr><tr><td>

Administrator

</td><td>

User who implements and sets up Service Operations Workspace for ITSM.

</td></tr></tbody>
</table>## Service Operations Workspace for ITSM benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Tailored landing page for tier 1 and tier 2 agents. It provides an overview of outages, service announcements, and assignments to efficiently prioritize the work. Tier 1 agents can view and manage their performance and learning tasks assigned by their manager. |[Service Operations Workspace for ITSM landing page](sow-ui-landing-page.md)|Tier 1 and Tier 2 agents|
|Agents can manage incidents effectively with contextual information and targeted actions. Streamline investigations and accelerate incident resolution with the metrics data collected from Agent Client Collector \(ACC\).|[Incident Management in Service Operations Workspace](incident-sow.md)|Tier 1 and Tier 2 agents|
|Agents can use information from similar incidents and knowledge articles to accelerate incident resolution.|[Recommended Actions for ITSM in Service Operations Workspace](recommended-actions-for-itsm-in-service-operations-workspace.md)|Tier 1 and Tier 2 agents|
|Agents can reach out to experts on-call for high-priority tasks. |[On-Call Scheduling in Service Operations Workspace](on-call-scheduling-in-sow.md)|Tier 1 and Tier 2 agents|
|Agents can collaborate with the requester and peers from the task using Microsoft Teams chat. |[ServiceNow integrations with Microsoft Teams in Service Operations Workspace](msteams-sow.md)|Tier 1 and Tier 2 agents|
| Agents can create requests from incidents and interactions. Agents can also manage the entire life cycle of requests. |[Request Management in Service Operations Workspace](request-sow.md)|Tier 1 and Tier 2 agents|
|Agents and administrators can review and manage walk-up interactions, appointments, stockrooms, and kiosks at the walk-up service location.  |[Walk-up Experience management in Service Operations Workspace](walkup-sow.md)|Tier 1 and Tier 2 agents|
|All logged-in users can view key features to get started with Service Operations Workspace for ITSM.|[Service Operations Workspace for ITSM landing page](sow-ui-landing-page.md)|Tier 1 and Tier 2 agents|
|Administrators can have a guided experience for initial configuration of Service Operations Workspace for ITSM.|Using guided setup|Administrator|
|Agents can have a unified experience for services and operations on a single platform by integrating with Service Operations Workspace for ITOM.|Automating and optimizing your services and operations using Service Operations Workspace|Tier 1 agent, Tier 2 agent, and IT operator|

For information about key features in Service Operations Workspace for ITOM, see Exploring Service Operations Workspace for ITOM.

## Service Operations Workspace for ITSM workflow for an agent

![SOW workflow](../image/final-sow-workflow.png)

-   An agent can start the day by looking at an overview of assignments, outages, service announcements, and assignments in Service Operations Workspace to prioritize work based on service level agreements \(SLAs\), priority level, and urgency​.
-   The agent can create an incident based on the issue reported. Since the agent has access to related incidents and recent interactions, better and faster support can be provided. Agent also has access to all related information from the incident record page.
-   The agent can resolve the incident faster by using tailored recommendations.
-   The agent can reach out to experts on-call for high-priority tasks.​
-   The agent can collaborate easily with the requester and peers right from the task.
-   The agent can create a change request to fix the issue.

## Using guided tours to learn about Service Operations Workspace for ITSM

Use a guided tour that is sequence of interactive steps to guide an agent through a specific process or task within Service Operations Workspace for ITSM. To access guided tours, select the Show help icon in the navigation bar and scroll down to find the **Take a Tour** or **Select a Tour** option. For more information about playing a guided tour, see [Play a guided tour in Service Operations Workspace](../task/play-guided-tour-sow.md).

**Important:**

-   A guided tour might break if you customize any of its associated UI elements in your instance, so ensure that you update your guided tours as well accordingly. For information on how to update guided tours, see Edit Guided Tours.
-   The **Take a Tour** or **Select a Tour** option is available only when a guided tour is available for that UI page.

## Using guided setup to implement Service Operations Workspace for ITSM

Service Operations Workspace for ITSM guided setup provides a sequence of tasks that help an administrator configure Service Operations Workspace for ITSM on your ServiceNow instance. To open Service Operations Workspace for ITSM guided setup, navigate to **All** &gt; **Adoption Services** &gt; **Guided Setup**. For more information about using the guided setup interface, see Using guided setup.

## What to explore next

To learn more about configuring and using Service Operations Workspace for ITSM, see:

-   [Configuring Service Operations Workspace for ITSM](configure-sow.md)
-   [Operating IT services in your organization](enhancing-services-operations-in-organization.md)
-   [Managing IT services in your organization](managing-services-operations-in-organization.md)
-   [Optimizing IT services in your organization](optimizing-services-operations-in-organization.md)

-   **[Access Service Operations Workspace for ITSM](../task/access-sow-itsm.md)**  
Experience a unified and seamless experience when managing the life cycle of task records such as incidents and requests.
-   **[Service Operations Workspace for ITSM user interface](service-operations-workspace-ui.md)**  
You can navigate through the Service Operations Workspace to get an overview of how an agent can prioritize tasks and provide resolution.
-   **[Service Operations Workspace for ITSM landing page](sow-ui-landing-page.md)**  
An agent can get quick visibility into the work assigned, view announcements, and view upcoming tasks.
-   **[Exploring Recommended Actions for ITSM in Service Operations Workspace](exploring-recommended-actions-for-itsm-in-service-operations-workspace.md)**  
Recommended Actions for ITSM lets you set up and apply real-time actionable recommendations for speeding up the triaging process. You can resolve issues quickly across various records in the Service Operations Workspace, including Incident, Incident task, Problem, Problem task, Change request, Change task, Interaction, and Request.
-   **[Exploring On-call Scheduling in Service Operations Workspace](../task/on-call-scheduling-in-service-operations-workspace.md)**  
On-Call Scheduling ensures that dedicated support team members are always available to resolve issues as they arise. You can set up on-call schedules, roster rotations, and escalation policies, escalate notifications for a group, and determine the current contact for an escalation.

**Parent Topic:**[Service Operations Workspace for ITSM](sow-landing-page.md)

**Related topics**  


[bundle-platux.list-of-workspaces]

