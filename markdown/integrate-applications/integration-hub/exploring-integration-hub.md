---
title: Exploring Integration Hub
description: ServiceNow Integration Hub enables you to build reusable integrations with third-party systems and call them from anywhere in the ServiceNow AI Platform. For example, you can request Integration Hub to call external systems using integration APIs from the Action Designer Script step, run the Script step on the ServiceNow MID Server, and activate protocol steps like REST, SOAP, and PowerShell.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Integration Hub, Creating integrations with applications]
---

# Exploring Integration Hub

ServiceNow® Integration Hub enables you to build reusable integrations with third-party systems and call them from anywhere in the ServiceNow AI Platform. For example, you can request Integration Hub to call external systems using integration APIs from the Action Designer Script step, run the Script step on the ServiceNow® MID Server, and activate protocol steps like REST, SOAP, and PowerShell.

## Capabilities

The Integration Hub provides both inbound and outbound integration with third-party applications.

Inbound integration occurs when a flow that you set up on Workflow Studio responds to a conditional and event-driven external webhook from a third-party system and executes. For example, when you create a P1 issue on an issue-tracking application, its external webhook triggers a flow in the ServiceNow instance and an incidence database table is updated in the ServiceNow instance. Here, the webhook is conditional and event-driven.

Outbound integration occurs when the Integration Hub enables execution of third-party APIs as a part of a flow when a specific event occurs in ServiceNow. These integrations, referred to as spokes, are easy to configure and enable you to quickly add powerful actions without the need to write a script. For example, you can post a message and incident details in a Slack channel when a high priority incident is created.

Integration Hub provides the following functionality:

-   **Create spokes**

    Build spokes using Spoke Generator to automate integration tasks by creating a sequence of reusable actions to develop custom integrations. For more information, see [Building spokes using Spoke Generator](https://www.servicenow.com/docs/access?context=spoke-builder&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

-   **Spokes for base system integrations**

    Using Integration Hub actions in Workflow Studio, you can:

    -   Post messages and ServiceNow incident, problem, and change record details to [Slack Spoke](slack-spoke.md), or [Microsoft Teams Spoke](../reference/microsoft-teams-spoke.md) communications channels.
    -   Synchronize data across multiple production instances using [Integration Hub Remote Process Sync](integrationhub-remote-process-sync.md).
-   **Create custom integrations**

    Build custom integrations with Workflow Studio using a [REST step](../../flow-designer/reference/rest-request-action-designer.md) or a [Script step](https://www.servicenow.com/docs/access?context=javascript-step-action-designer&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

-   **Automate inbound integrations with third-party applications**

    [Set up a flow with external trigger definition](../tasks/set-up-flow-ihub.md) on Workflow Studio by selecting base system external trigger definitions, and actions from the spokes or core actions. Then, [Set up external trigger endpoints](../tasks/set-up-external-webhook-endpoints.md) that the third-party application webhooks use to trigger the flow you had set up. Your ServiceNow instance authenticates the webhook before it triggers the flow.

-   **Automate the administration of servers and applications in your network**

    Use custom actions to delegate Workflow Studio processes to a [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) in your network. For example, actions that use the [PowerShell step](../../flow-designer/reference/powershell-step-action-designer.md) or [REST step](../../flow-designer/reference/rest-request-action-designer.md).


## Benefits

Integration Hub provides process owners and developers these benefits.

-   Consolidates multiple ServiceNow AI Platform automation capabilities into a single environment so process owners and developers can build and visualize business processes and integrations from a single interface.
-   Extends Workflow Studio content to integrate business processes with external systems.
-   Promotes business process automation by enabling subject matter experts to develop and share spokes with flow designers.
-   Provides natural-language-descriptions of integration logic to help non-technical users understand triggers, actions, inputs, and outputs.

## Connection and Credentials

Integration Hub takes advantage of aliases to manage connection information and credentials when integrating with external systems. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. Integration Hub only requires an alias, which then resolves to use the correct credentials and connection information during runtime. Learn more about [credentials, connections, and aliases](https://www.servicenow.com/docs/access?context=credentials-connections-alias&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## Development process

When developing a custom integration, develop all actions for the integration within a scoped application. When deployed to a target instance, these actions are grouped as a spoke in Workflow Studio. Brand the spoke by adding a custom icon to the application record. To learn more about application development, see [Build applications](https://www.servicenow.com/docs/access?context=build-applications&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

When developing spokes, flow and action designers typically perform these application development tasks.

1.  Create a scoped application on a development instance to build spokes.
2.  Publish a test version of the scoped application to the application repository.
3.  Deploy the scoped application to a test instance from the application repository.
4.  Test the scoped application on the test instance.
5.  When working as expected, publish the scoped application in one of the following ways.
    -   Publish to the application repository for deployment on production instances.
    -   Publish to the ServiceNow Store as an application that customers can request for their environments.
    -   Publish to ServiceNow Share to provide content to other customers in the ServiceNow community.

Review Workflow Studio design considerations in the [Architecture Overview](https://www.servicenow.com/docs/access?context=flow-designer-arch-overview&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

**Parent Topic:**[Integration Hub](integrationhub.md)

