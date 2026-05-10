---
title: Problem Management process
description: Within the platform, problems are handled using the task record system. Each problem is generated as a task record through various means, and is populated with the pertinent information. These tasks are assigned to Problem Management team members to resolve and then close.
locale: en-US
release: australia
product: Problem Management
classification: problem-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring Problem Management, Problem Management, IT Service Management]
---

# Problem Management process

Within the platform, problems are handled using the task record system. Each problem is generated as a task record through various means, and is populated with the pertinent information. These tasks are assigned to Problem Management team members to resolve and then close.

## Identify and log problems

A problem can be created in several ways. For detailed information, refer [Create a problem](../task/create-a-problem-v2.md).

Associating a problem with a configuration item using CMDB helps the Problem Management team see the affected items and its relationship to other configuration items.

A problem can be associated with one or more incidents in the **Incidents** related list. The association is automatic if the problem is generated from an incident. Associating incidents provides the Problem Management team with access to the information gathered during incident investigation.

## Investigate and update problems

If the Problem Management team has a problem model process for dealing with certain problems, they can be added to the system with [workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/legacy-workflow/c_WorkflowOverview.md) . Workflows standardize and automate a process.

As a problem is updated, [email notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_EmailNotifications.md) are sent to concerned parties. If inbound email actions are specified, the problem can be updated via email.

You can use the other active tasks icon next to **Configuration item** to look up active problem records. When you click the icon, it shows all active tasks linked to that configuration item.

The platform provides escalations rules to ensure that problems are handled promptly. Two types of escalation rules are available in the system.

-   [Service level agreements](../../service-level-management/concept/service-level-management-concepts.md): SLAs can be used to ensure that problems are highlighted. As investigating and fixing a problem could be a long-term effort, it is not recommended that you apply SLAs to an overall problem. SLAs are also used as a performance indicator for the Problem Management team.
-   [Inactivity monitors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/t_SetAnInactivityMonitor.md) : The inactivity monitors prevent problems from being overlooked by generating an event. When a problem has not been updated within a certain amount of time, the event can create an email notification or trigger a script.

## Resolve problems

If a problem needs a change request to be resolved, it is possible to request a change that goes through the change management process. After requesting a change, the problem appears on a related list on the Change Request form.

**Note:** For Madrid Best Practices: The problem coordinator, whom the Problem is assigned to, is notified when all related change requests are completed or canceled.

The following information applies for London and prior releases:

-   A business rule \(**SNC-ITIL-Close-related**\) automates the process of closing problems in **Pending Change** state when the change request is closed. If the problem is closed, another business rule \(**SNC - ITIL - Resolve Related Incidents**\) automatically sets the **State** to **Resolved** for all incidents associated with that problem whose **State** was **On Hold** and **On hold reason** was **Awaiting Problem**.
-   If the cause of a problem has been determined but there is no permanent fix, change the problem state to **Known Error** to communicate this fact. IT agents can click the Known Errors module and look for the issue they are investigating to reduce time spent on a similar issue. To communicate information related to a problem, you can open the problem and describe a workaround, create a knowledge base article, or create a news item.

-   **[Life cycle of a problem](understanding-state-mgmt-transitions.md)**  
Problem Management is responsible for managing the life cycle of underlying problems. State transition of a problem guides you through the stages of a problem life cycle, from creation to closure.
-   **[Life cycle of a problem task](understanding-state-trans-prob-task.md)**  
A problem task is the smallest unit of work that you should perform to complete a problem. State transition of a problem task guides you through the stages of a problem task life cycle, from creation to closure.

**Parent Topic:**[Exploring Problem Management](exploring-problem-management.md)

