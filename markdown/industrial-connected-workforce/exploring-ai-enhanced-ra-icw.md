---
title: AI Enhanced recommended actions for Industrial Connected Workforce \( ICW\)
description: The AI Enhanced recommended actions for Industrial Connected Workforce feature accesses external sources related to a deviation, and contextualizes how the document is relevant to the deviation.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [explore]
breadcrumb: [AI Enhanced recommended actions for ICW, Industrial Connected Workforce]
---

# AI Enhanced recommended actions for Industrial Connected Workforce \( ICW\)

The AI Enhanced recommended actions for Industrial Connected Workforce feature accesses external sources related to a deviation, and contextualizes how the document is relevant to the deviation.

## AI Enhanced recommended actions for ICW overview

AI Enhanced recommended actions for ICW leverages the external content connector to collect data from an external source. This feature currently supports using Microsoft SharePoint Online as the external source.

**Note:** The external content connector is part of the existing ServiceNow AI Platform capabilities. For more information about the external content connector, see External Content Connectors.

## Using the AI Enhanced recommended actions for ICW for your recommended actions

AI Search fetches the data from the external source. Then AI Enhanced recommended actions for ICW displays the fetched data as search results in the **Suggested Actions** tab of the Recommendations panel. You can use the **Contextualize document** UI action in the **Suggested Actions** tab to summarize why a fetched document is relevant to your search prompt.

By default, AI Search uses the short description, description, site, ICW device, and equipment model entity field values to display the most relevant external sources for your deviation. The following image shows an example of what the **Contextualize document** UI action looks like in an existing deviation record in the Digital Factory Workspace.

Image/screenshot: Contextualize document UI action under an external document in the Digital Factory Workspace.

## What to explore next

To learn more about configuring and using AI Enhanced recommended actions for ICW, see:

-   [Configure AI Enhanced recommended actions for Industrial Connected Workforce](configure-ai-enhanced-ra-icw.md)
-   [Contextualize an external document for a Deviation in the Digital Factory Workspace](../task/use-ai-enhanced-ra-icw.md)

**Parent Topic:**[AI Enhanced recommended actions for Industrial Connected Workforce](../reference/ai-enhanced-ra-icw-landing.md)

