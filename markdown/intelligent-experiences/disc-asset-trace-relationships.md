---
title: Trace the relationships between AI assets
description: Identify the AI assets that depend on or feed into a specific AI asset to assess the impact of a planned change, investigate an unexpected evaluation score, or respond to an audit question about how data and models flow through your AI inventory.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/disc-asset-trace-relationships.html
release: zurich
topic_type: task
last_updated: "2026-05-05"
reading_time_minutes: 1
keywords: [asset relationship map, asset map, dependencies, related AI assets, change impact]
breadcrumb: [Managing AI asset details, Working with AI asset records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Trace the relationships between AI assets

Identify the AI assets that depend on or feed into a specific AI asset to assess the impact of a planned change, investigate an unexpected evaluation score, or respond to an audit question about how data and models flow through your AI inventory.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward or sn\_ai\_asset\_mgmt.ai\_asset\_owner

**Note:** Users with the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role can view relationships for any asset but can only update assets that they own.

## About this task

The asset relationship map shows the current AI asset at the center, with connected AI assets arranged around it. Connected assets are grouped by node type, such as AI models, AI prompts, and AI datasets.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Inventory**.

2.  Open the AI asset with connections that you want to trace.

3.  Select the **Details** tab and locate the **Asset relationship map** section.

4.  To narrow the map to a specific category of related asset, such as AI models or AI datasets, select a value from the **Node type** list.

    The map updates to show only nodes of the type you selected.

5.  To find a specific related asset by name, enter the name in the search field.

6.  To open a related asset's record, select its node on the map.

    The selected asset's record opens.


## What to do next

Depending on the relationships identified, take one of the following actions:

-   Add a relationship to another asset.
-   If a related asset will be affected by an upcoming change, create a change request for that asset. See [Create change requests for AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-ai-asset-change-request-newexperience.md)
-   If you're investigating evaluation scores for an AI system, review the **Evaluation** tab on a connected AI model's record to see how that model performs in isolation. See [Monitoring an AI system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-asset-monitor.md).

**Parent Topic:**[Managing AI asset details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-ai-asset-details.md)

