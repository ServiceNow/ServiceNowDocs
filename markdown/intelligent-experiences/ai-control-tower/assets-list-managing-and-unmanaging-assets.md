---
title: Managing AI assets
description: Learn about managing AI assets as Managed and Unmanaged assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/assets-list-managing-and-unmanaging-assets.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-01-28"
reading_time_minutes: 1
breadcrumb: [AI asset inventory, AI assets, AI Control Tower dashboard, Explore, AI Control Tower, Enable AI experiences]
---

# Managing AI assets

Learn about managing AI assets as Managed and Unmanaged assets.

## Assets list

AI assets are presented in a list format and organized by display name, provider, vendor, managed by, lifecycle phase, state, status, and risk classification.

## Managed and Unmanaged assets

Starting with the AI Control Tower, Australia \(March 2026\) release, you can designate assets as managed or unmanaged directly from the list. By default, all the assets in AI Control Tower are under unmanaged assets.

When an unmanaged asset is marked as managed, it gains access to AI Control Tower capabilities such as governance, lifecycle management, value assessment, risk classification, security, and privacy. If a managed asset is switched back to an unmanaged asset, it loses all the previously mentioned AI Control Tower capabilities.

**Note:** When an upgrade happens all the existing assets are unmanaged except those which have open approval requests and AI Control Tower capabilities like Lifecycle, Risk Assessments, Value, Monitoring and Evaluation, Security aren't available and the managed assets are accounted for licensing cost.

Using Automation rules, AI assets are set as managed. For information on the Automation rules page, see [Automation rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/ai-control-tower/automation-rules.md).

\[Omitted image "unamanged-managed-asset.png"\] Alt text: AI asset inventory - Managed - AI systems screen.

**Note:** Initiating a steward review for an unmanaged asset triggers the lifecycle process and automatically transitions the asset to a managed state.

