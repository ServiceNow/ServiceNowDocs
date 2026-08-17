---
title: Managed and unmanaged AI assets
description: Control whether an AI asset participates in governance workflows by changing the status in AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/disc-ai-managed-unmanaged.html
release: zurich
topic_type: concept
last_updated: "2026-05-18"
reading_time_minutes: 1
breadcrumb: [Managing your AI asset inventory, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Managed and unmanaged AI assets

Control whether an AI asset participates in governance workflows by changing the status in AI Control Tower.

You can set or change the management status of any asset directly from the inventory list. Use these guidelines to decide when to move assets between states:

-   Assets discovered automatically or imported through connectors enter the inventory as unmanaged by default. Move assets to managed when you're ready to bring them into your governance program. You can move one asset or multiple assets at the same time.
-   Move assets to unmanaged when they no longer need to participate in governance workflows. For example, you might move an asset to unmanaged when an asset has been superseded, is under evaluation for retirement, or was discovered but doesn't yet require governance oversight. Unmanaged assets remain in the inventory but are excluded from active workflows and lifecycle reviews.

Initiating a steward review for an unmanaged asset transitions it to managed status automatically. Automation rules can also set or change management status based on conditions you define. See [Managing AI assets in bulk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-ai-bulk-managing-assets.md).

**Note:** The **Move to Managed** and **Move to Unmanaged** actions are now restricted to the AI Steward role. A Product Owner can't perform these actions on any asset, whether owned or not.

