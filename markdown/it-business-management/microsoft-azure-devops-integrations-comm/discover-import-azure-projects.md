---
title: Discover and import Azure DevOps projects
description: Discover and import all available Azure DevOps projects into Agile Development 2.0 to start using the integration between the two applications.
locale: en-US
release: australia
product: Microsoft Azure DevOps Integrations Comm
classification: microsoft-azure-devops-integrations-comm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0, Microsoft Azure DevOps Integration for Agile Development, Strategic Portfolio Management]
---

# Discover and import Azure DevOps projects

Discover and import all available Azure DevOps projects into Agile Development 2.0 to start using the integration between the two applications.

## Before you begin

-   Complete [connecting Agile Development and Azure DevOps](../reference/connect-sn-agile-with-azure.md#).
-   Role required: sn\_ado\_int.user

## Procedure

1.  Navigate to **All** &gt; **Agile Azure DevOps Integration** &gt; **Azure DevOps Instances**.

2.  Open your Azure DevOps instance record.

3.  Click **Discover Projects**.

    This action creates requests to import Azure DevOps projects and process map configuration for all these projects. You can view all import requests in the Azure DevOps Import Requests related list. The initial state of these requests is **Requested**.


## Result

Once the status of each import request changes to **Complete**, you can see that the related lists of this Azure DevOps instance are populated as follows:

-   Azure DevOps Projects: All available projects from Azure DevOps
-   Process Mappings: Map configuration for all the imported Azure DevOps projects according to the process type.

    For example, default process types such as Agile, Basic, and CMMI or any custom process types that you defined for your Azure DevOps projects.

    For more information on the default map configuration of work items, see [Default map configuration for Azure DevOps integration with Agile Development 2.0](../reference/default-agile-azure-mapping.md).


## What to do next

[Import areas, teams, and iterations from Azure DevOps](import-areas-teams-azure-agile.md)

.

-   **[Default map configuration for Azure DevOps integration with Agile Development 2.0](../reference/default-agile-azure-mapping.md)**  
Understand the default field map configuration, of different process types, between Azure DevOps and Agile Development 2.0.

**Parent Topic:**[Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0](../concept/setting-up-agile-azure-integration.md)

