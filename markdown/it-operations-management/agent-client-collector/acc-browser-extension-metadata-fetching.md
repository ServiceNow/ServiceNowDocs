---
title: Browser extension metadata fetching
description: Assess shadow IT and shadow AI risk in your organization by using browser extension metadata fetching in Agent Client Collector for Visibility \(ACC-VC\). This capability is an optional layer on top of browser extension discovery that collects each extension's metadata.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/acc-browser-extension-metadata-fetching.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-08-27"
reading_time_minutes: 1
keywords: [browser extension metadata, browser extension discovery, ACC-VC]
breadcrumb: [Browser extension discovery and categorization, ACC deployment - endpoints, Agent Client Collector, IT Operations Management]
---

# Browser extension metadata fetching

Assess shadow IT and shadow AI risk in your organization by using browser extension metadata fetching in Agent Client Collector for Visibility \(ACC-VC\). This capability is an optional layer on top of browser extension discovery that collects each extension's metadata.

## Browser extension metadata fetching overview

ACC-VC browser extension discovery identifies extensions installed across the endpoints in your environment. Browser extension metadata fetching goes a step further: it reads each extension's manifest and preference data to collect declared and runtime-granted permissions, host access, install source, and install and update timestamps. The system collects this metadata for extensions on Windows, Mac, and Linux endpoints. This feature provides security and IT teams the detail needed to assess shadow IT and shadow AI risk, rather than just the extension name and version.

**Note:** On Mac machines, populating the extended metadata column requires FDA.

## Data collected

The type of data browser extension metadata fetching collects depends on the browser family, as shown in the table.

|Field group|Chrome, Edge, Brave, and Opera|Firefox|
|-----------|------------------------------|-------|
|Permissions|Runtime-granted permissions, falling back to permissions declared in the extension manifest|Permissions declared by the extension|
|Host access|Granted explicit hosts, falling back to manifest host permissions|Declared origins|
|Install source|Web store or side-loaded, classified from browser-reported signals|Web store or side-loaded, classified from browser-reported signals|
|Install and update time|Extension install and update timestamps reported by the browser|Extension install and update timestamps reported by the browser|

## Performance impact

Turning on browser extension metadata fetching increases the amount of data the agent reads and sends for each extension. Turn it on deliberately instead of leaving it on by default.

**Note:** If you turn off browser extension metadata fetching after previously turning it on, existing metadata records aren't deleted, but they stop being refreshed.

