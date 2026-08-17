---
title: AI insights and dependency details
description: Analyze an individual cryptographic asset with AI insights powered by ServiceNow Otto and a dependency graph, which shows where the asset is used.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-visibility/ai-insights-and-dependency-details.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-07-25"
reading_time_minutes: 1
breadcrumb: [View cryptographic asset details, Monitor, Cryptographic Asset Compliance, ITOM Visibility, IT Operations Management]
---

# AI insights and dependency details

Analyze an individual cryptographic asset with AI insights powered by ServiceNow Otto and a dependency graph, which shows where the asset is used.

## AI Insights

The AI Insights section in the **Details** tab of an asset displays an AI-generated analysis. It includes an overview of the risk on the asset, the probable cause of each risk indicator, and recommended actions to address it. You can refresh these insights to reflect the latest state of an asset.

You can copy these insights to the clipboard for reuse.

## Dependency graph

The **Dependency graph** tab of an asset displays a graph that shows where a cryptographic asset is used. For example, the graph shows the infrastructure on which the asset is deployed on and the applications that use it. You can search the nodes in the graph by their label. The relationships displayed depend on the asset type.

For Azure Key Vault keys, the relationships displayed are:

-   Key Vault: The key vault the key is stored in.
-   Datacenter: The datacenter the key is hosted in.
-   Applications: The applications that use the key.
-   Resource Group: The resource group the key belongs to.
-   Service Account: The cloud service account the key is managed by.

For AWS KMS keys, the relationships displayed are:

-   Datacenter: The datacenter the key is hosted in.
-   Applications: The applications that use the key.
-   Cloud Service Account: The cloud service account the key is managed by.

For certificates, the relationships displayed are:

-   Infrastructure: The infrastructure that the certificate is deployed on.
-   Applications: The applications that use the certificate.
-   Other relations: Other CIs the certificate is related to, for example, a manual endpoint.

**Note:** URL-based certificates have no dependent infrastructure, so the graph does not display any infrastructure details.

