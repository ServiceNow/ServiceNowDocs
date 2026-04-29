---
title: AI Service Graph Connector for Microsoft
description: Use the  AI Service Graph Connector for Microsoft  plugin to create AI connections for Azure Foundry and Copilot to discover AI assets such as AI systems, models, prompts, and tools as well as usage data for these AI agents within your ServiceNow AI Control Tower. This usage information is consumed by the AI Control Tower value dashboard.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Graph Connectors for AI Control Tower, Enterprise AI discovery: Unlock Visibility, Governance &amp; Value, Explore, AI Control Tower, Enable AI experiences]
---

# AI Service Graph Connector for Microsoft

Use the  AI Service Graph Connector for Microsoft  plugin to create AI connections for Azure Foundry and Copilot to discover AI assets such as AI systems, models, prompts, and tools as well as usage data for these AI agents within your ServiceNow AI Control Tower. This usage information is consumed by the AI Control Tower value dashboard.

## Download apps from the store

Visit the  [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to download the AI Service Graph Connector for Microsoft app.

## Supported ServiceNow versions

-   Australia
-   Zurich patch 7
-   Yokohama patch 11

## User roles

Roles required in the ServiceNow environment:

-   sn\_ai\_disc.discovery\_admin
-   sn\_cmdb\_int\_util.sgc\_admin

## Prerequisites from Azure Foundry environment

**Setting up Azure Foundry:**

-   To get the OAuth credentials, refer to the [Azure documentation](https://learn.microsoft.com/en-us/rest/api/azure/#register-your-client-application-with-azure-ad).
-   The Azure client application needs at least 'User. Contributor' role on AI Hub \(ML services\) API. Refer [documentation for Azure Hub roles.](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/hub-rbac-foundry?view=foundry-classic#default-roles-for-the-hub) It also requires a workspace to be created.
-   The Azure client application needs at least an 'Azure AI User' role on the Azure Foundry \(Cognitive Services\) API. Refer [documentation for Azure Foundry roles.](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/rbac-foundry?view=foundry&preserve-view=true#built-in-roles) It also requires an account \(resource name\) to be created.
-   Enable both Discovery and Execution import schedules to discover agents and retrieve execution data.

## Prerequisites from Copilot environment

**Setting up Copilot**

-   Register an application in Microsoft Entra ID and [Register](https://learn.microsoft.com/en-us/entra/identity-platform/quickstart-register-app) to obtain the Client ID and Client secret.
-   Open the Power Platform Admin Center, select your Copilot environment, then go to Settings &gt; Users+permissions &gt; Application users, add a new app user using the Client ID and assign Basic user and System administrator roles.
-   Find the Organization ID, Tenant ID under Settings &gt; Session details.
-   Usage is tracked only in non-developer environments.
-   Enable both Discovery and Executions to discover agents and retrieve execution data.

**Note:** For Microsoft, OAuth authentication is supported.

