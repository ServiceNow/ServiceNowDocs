---
title: Configuring Azure DevOps projects for SAFe
description: Set up SAFe related configuration in Azure DevOps projects and understand the workflow of SAFe PI and Sprint integration with Azure DevOps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/microsoft-azure-devops-integrations-comm/configuring-azure-devops-projects-for-safe.html
release: zurich
product: Microsoft Azure DevOps Integrations Comm
classification: microsoft-azure-devops-integrations-comm
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Azure DevOps integration with SAFe, Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0, Microsoft Azure DevOps Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Configuring Azure DevOps projects for SAFe

Set up SAFe related configuration in Azure DevOps projects and understand the workflow of SAFe PI and Sprint integration with Azure DevOps.

After creating map configuration for SAFe entities, [import areas, teams, and iterations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/microsoft-azure-devops-integrations-comm/import-areas-teams-azure-agile.md) for your Azure DevOps projects and update the following fields. These fields are mandatory if **Sync Sprints** is set to **true**.

-   **ART**: Select an agile release train \(ART\).
-   **ART Iteration Path**: Select an iteration that is an equivalent to the parent of PI.

    **Note:** If the ART Iteration Path lookup \(\[Omitted image "lookup\_icon.png"\] Alt text: Lookup icon\) does not return any records, [import areas, teams, and iterations from Azure DevOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/microsoft-azure-devops-integrations-comm/import-areas-teams-azure-agile.md) and try again.

    For the example shown in the following screenshot, **Fabrikam** must be selected as the ART Iteration path.


The application will then automatically identify PI 1 as the program increment and Sprint 1, Sprint 2, and so on, as the corresponding SAFe sprints in the ServiceNow instance.

\[Omitted image "safe-pi-sprint.png"\] Alt text: Azure DevOps SAFe project example.

**Important:**

-   To create [team integration settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/microsoft-azure-devops-integrations-comm/set-up-import-export-azure-agile.md) for a project, the SAFe teams must be a part of the project's ART.
-   All teams of an ART must share the same sprint cycle.

## SAFe sprint and PI integration workflow

\[Omitted image "SAFe-Sprint-ADO-Import-Sprints.jpg"\] Alt text: Import Sprints workflow between SAFe and Azure DevOps.

