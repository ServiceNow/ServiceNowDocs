---
title: Continual Improvement Management overview
description: Continual Improvement Management enables you to initiate improvement opportunities within your organization by providing a centralized framework for planning, implementing, and monitoring improvement initiatives.
locale: en-US
release: xanadu
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Continual Improvement Management, IT Service Management]
---

# Continual Improvement Management overview

Continual Improvement Management enables you to initiate improvement opportunities within your organization by providing a centralized framework for planning, implementing, and monitoring improvement initiatives.

The following video gives you an overview of Continual Improvement Management application.Continual Improvement Management Overview

Use Continual Improvement Management to implement service, process, and function improvements. An improvement initiative contains goals to measure success, and phases that contain tasks with specific actions to complete the improvement.

![Continual Improvement Management Workflow](../image/cim-workflow.png)

## Initial CIM setup

Install the CIM plugin. For more information, see [Install CIM](../task/request-cim.md).

To use guided setup to configure CIM, navigate to **Continual Improvement** &gt; **Administration** &gt; **Guided Setup** and select **Configure** in the Request CIM section.

Once CIM is activated, assign user roles and groups.

-   Improvement Manager
-   Improvement Coordinator
-   Approver group membership \(CIM Approvers, default is empty\)

For more information, see [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Use the [Continual Improvement Workbench](../task/plan-cim-initiatives.md) to plan and manage improvements. Both tile and list views are supported.

## Workflow of CIM roles

The workflow of improvements from an improvement request to final approval Continual Improvement Management involves various responsibilities.

1.  An **Improvement Requester**, such as a help desk manager, process owner, or ITIL user, recognizes the need for an improvement with the organization and submits an improvement request.
2.  The **Improvement Manager** reviews the improvement, accepts it, and assigns it to an Improvement Coordinator for implementation. The Improvement Manager also runs prioritization meetings with Improvement Coordinators and uses the Continual Improvement workbench to monitor, manage, and plan overall progress of improvements. When all tasks are complete, the Improvement Manager reviews improvements for closure.
3.  After the improvement request is assigned, the **Improvement Coordinator** along with the Improvement manager creates phases and tasks to complete the improvement. The Improvement Coordinator also meets with task owners to track progress and timely completion.

For more information about CIM roles, see [CIM roles](../reference/cim-roles.md).

## Integration with other applications

CIM is integrated with other ServiceNow® applications to enable you to create improvements across various processes and services within the company. These integrations provide you a centralized framework to implement, manage, and monitor the progress and impact of improvements. You can create improvement initiatives from integrated applications and conversely, create records for integrated applications from improvement initiatives.

For more information about the applications integrated with CIM, see [Improvement integration with other applications](../reference/cim-integration.md).

## Domain separation

[Domain separation](cim-domain-separation.md) capability is supported in Continual Improvement Management with no setup or configuration required.

You can create improvements separately in a specific domain, or in the global domain.

-   **[Install CIM](../task/request-cim.md)**  
Install the Continual Improvement Management plugin from ServiceNow Application Manager after purchasing a subscription.
-   **[Improvement integration with other applications](../reference/cim-integration.md)**  
You can create an improvement request from within multiple integrated applications. You can also create many application tasks from within an improvement initiative. Set the Continual Improvement Management attributes property to determine which field values get copied to integrated application tasks.
-   **[Integrate Continual Improvement Management using extension point](../task/integrate-extension-api.md)**  
Integrate CIM with other applications by using the CIMIntegrationAPI extension point. It defines the inbound and outbound extension points for integrating CIM with other applications.
-   **[Domain separation and Continual Improvement Management](cim-domain-separation.md)**  
Domain separation in Continual Improvement Management is configured to apply to all features of the application. Separation of data is configured along with separation of logic and process. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

**Parent Topic:**[Continual Improvement Management](cim-landing-page.md)

