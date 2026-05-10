---
title: AI Enhanced Recommended Actions for Operational Technology Service Management \(OTSM\)
description: The AI Enhanced Recommended Actions for Operational Technology Service Management \(OTSM\) feature accesses external sources related to an Operational Technology \(OT\) incident, and contextualizes how the document is relevant to the incident.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [explore]
breadcrumb: [AI Enhanced Recommended Actions for OTSM, Operational Technology]
---

# AI Enhanced Recommended Actions for Operational Technology Service Management \(OTSM\)

The AI Enhanced Recommended Actions for Operational Technology Service Management \(OTSM\) feature accesses external sources related to an Operational Technology \(OT\) incident, and contextualizes how the document is relevant to the incident.

## AI Enhanced Recommended Actions for OTSM overview

AI Enhanced Recommended Actions for OTSM leverages the external content connector to collect data from an external source. This feature currently supports using Microsoft SharePoint Online as the external source.

**Note:** The external content connector is part of the existing ServiceNow AI Platform capabilities. For more information about the external content connector, see [External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/ext-cont-connectors-landing-page.md).

## Using the AI Enhanced Recommended Actions for OTSM for your recommended actions

**Contextualize document feature**

AI Search fetches the data from the external source. Then AI Enhanced Recommended Actions for OTSM displays the fetched data as search results in the **Suggested Actions** tab of the Recommendations panel. You can use the **Contextualize document** UI action in the **Suggested Actions** tab to summarize why a fetched document is relevant to your search prompt.

By default, AI Search uses the short description, description, site, OT device, and equipment model entity field values to display the most relevant external sources for your OT incident. The following image shows an example of what the **Contextualize document** UI action looks like in an existing OT incident record in the Industrial Workspace.

![Contextualize document UI action under an external document in the Industrial Workspace](../image/conextualize-doc-example.png)

## What to explore next

To learn more about configuring and using , see:

-   [Configure AI Enhanced Recommended Actions for Operational Technology Service Management \(OTSM\)](configure-ai-enhanced-ra-otsm.md)
-   [Contextualize an external document](../task/use-ai-enhanced-ra-otsm.md)

