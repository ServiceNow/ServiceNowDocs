---
title: Azure DevOps integration with DevOps Change Velocity
description: Connect to your Azure DevOps instance to discover boards, repositories, and pipelines to enable change automation and traceability.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integrate, DevOps Change Velocity, IT Service Management]
---

# Azure DevOps integration with DevOps Change Velocity

Connect to your Azure DevOps instance to discover boards, repositories, and pipelines to enable change automation and traceability.

## Azure DevOps integration overview

The following Azure DevOps tools are supported:

-   Azure Boards \(planning\)
-   Azure Repositories \(coding\)
-   Azure Pipelines \(orchestration\)
    -   Build \(CI\) pipelines — agent and agentless \(server\) jobs
    -   Release \(CD\) pipelines

Capture tags from Azure DevOps coding tool commits.

Jenkins also supports testing capabilities with JUnit. [Test tool integration](dev-ops-test-tool-integration.md) lets you view test results in DevOps Change Velocity for Azure DevOps unit, functional, and performance tests.

## Azure DevOps extension

You can use the **ServiceNow DevOps** extension for Azure DevOps on [Visual Studio Marketplace](https://marketplace.visualstudio.com/) to integrate your Azure pipeline with DevOps Change Velocity.

The [**ServiceNow DevOps** extension](../task/config-dev-ops-extensions-azure.md#) includes:

-   ServiceNow DevOps service connection
-   ServiceNow DevOps Release Gate
-   Azure build \(CI\) pipeline agent and server job custom tasks
-   ServiceNow DevOps Build Sonar Registration \(for Build pipelines\)
-   ServiceNow DevOps Release Sonar Registration task \(for Release pipelines\)

## Bulk commits in Azure DevOps

Large commits are supported with Azure DevOps.

To support large commits, perform these actions:

-   Install the ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\) plugin.
-   For optimal performance, disable flow logging by setting the Workflow Studio **com.snc.process\_flow.reporting.level** property to **Off**.
-   For MID Server settings, view the [MID Server support for Data Stream actions](https://www.servicenow.com/docs/access?context=dsa-on-mid&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US) section.

The Azure DevOps data stream can currently process up to 8000-9000 commits per code push. The number of run commits listed for a task execution are limited to 200.

## Get started

You can connect to Azure DevOps at the organization level or at individual project levels.

Connecting at an organization level is recommended as it is enables discovery of multiple projects at once using one set of credentials. This makes it easier to discover multiple projects at a time and for updating credentials.

Connecting at a project level if you want to restrict access to the project to a certain group of users. Since DevOps group access controls are at the tool level, to restrict access to a project, you must create an Azure DevOps tool connection for that project.

Use one of the following options to onboard Azure DevOps. For a guided experience, use the workspace to onboard a tool. Alternatively, you can use the Service Catalog or Classic experience.

-   **[Onboard Azure DevOps to DevOps Change Velocity — Workspace](devops-wkspc-azuredevops-tool-conn.md#)**  
Connect to your Azure DevOps instance using the DevOps Change Workspace playbook to collect data for planning, coding, orchestration, artifact, and software quality functions.
-   **[Onboard Azure DevOps to DevOps Change Velocity — Service Catalog](../task/onboard-azure-devops-service-catalog.md)**  
Create, connect, discover, and configure your Azure DevOps instance using the ServiceNow Service Catalog.
-   **[Onboard Azure DevOps to DevOps Change Velocity — Classic](../task/create-azure-tool-dev-ops.md)**  
Create an Azure DevOps tool record in DevOps Change Velocity to connect, discover, and import Azure DevOps tool data.

**Parent Topic:**[Integrating DevOps Change Velocity with third party tools](integrating-devops-change-with-third-party-tools.md)

