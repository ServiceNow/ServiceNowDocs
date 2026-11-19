---
title: AI Gateway tab in Control Tower
description: Explore the AI Gateway tab in the Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/ai-gateway-tab.html
release: brazil
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Control Tower Home, Control Tower dashboard, Exploring Control Tower \(legacy\), Control Tower \(legacy\), Establishing AI governance, Enable AI Experiences]
---

# AI Gateway tab in Control Tower

Explore the AI Gateway tab in the Control Tower.

## AI Gateway overview

**Prerequisites**

Role required: AI steward \[sn\_ai\_governance.ai\_steward\]

The AI Gateway tab shows the metrics at the MCP \(Model Context Protocol\) server level, listing all connected MCP servers along with the total number of transactions for each server and its success rate.

The AI Gateway displays a comprehensive view of all MCP servers categorized into:

-   Name
-   Total transactions
-   Success rate

Total transactions are all tool calls, calculated by MCP method equal, which is \("tools/call"\).

The success rate is the number of such transactions that have an HTTP status from 200 through 299 divided by the total.

