---
title: Browser extension discovery and categorization
description: Agent Client Collector for Visibility \(ACC-VC\) browser extension discovery inventories browser extensions installed on the endpoints in your environment. When an admin-defined signature matches, ACC-VC classifies each extension into a category, such as AI Tools, Productivity, or Security.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/acc-browser-extension-discovery.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-09-01"
reading_time_minutes: 1
keywords: [browser extensions, ACC-VC, extension discovery]
breadcrumb: [ACC deployment - endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Browser extension discovery and categorization

Agent Client Collector for Visibility \(ACC-VC\) browser extension discovery inventories browser extensions installed on the endpoints in your environment. When an admin-defined signature matches, ACC-VC classifies each extension into a category, such as AI Tools, Productivity, or Security.

## How browser extension discovery works

Users can install browser extensions without administrator involvement. Therefore, traditional software discovery often misses them. Browser extension discovery gives you an inventory of the extensions on your endpoints, their assigned category, and the devices where each extension is installed.

Browser extension discovery supports these browsers:

-   Chrome
-   Edge
-   Brave
-   Opera
-   Firefox
-   Safari

**Note:** On Mac machines, populating the browser extension status and extended metadata columns requires FDA.

For an extension to appear in the inventory, create a signature and specify the extension ID or name to match. Assign a category, such as AI Tools, to classify the matching extensions in the inventory. ACC-VC matches each discovered extension against the active signatures, and writes the result to the Browser Extension Catalogs table.

A signature takes effect on a device the next time that the 24-hour discovery check runs on that device. The daily configuration refresh picks up signatures that are new or newly activated. If an extension matches more than one signature, ACC-VC applies only the first match, in this fixed order:

1.  Extension ID signatures
2.  Exact-name signatures
3.  Other name-condition signatures, such as contains, starts with, and ends with.

Browser extensions are categorized or re-categorized automatically, without creating a new signature, in the following cases:

-   An inactive signature is reactivated.
-   New browser extensions are discovered that match an existing active signature.

-   **[Browser extension metadata fetching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-browser-extension-metadata-fetching.md)**  
Assess shadow IT and shadow AI risk in your organization by using browser extension metadata fetching in Agent Client Collector for Visibility \(ACC-VC\). This capability is an optional layer on top of browser extension discovery that collects each extension's metadata.
-   **[Categorize discovered browser extensions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-categorize-browser-extensions.md)**  
Group discovered browser extensions in your environment by business relevance.

**Parent Topic:**[Deploying Agent Client Collector on endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-endpoint-deployment.md)

