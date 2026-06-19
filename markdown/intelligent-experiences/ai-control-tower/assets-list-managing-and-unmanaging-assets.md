---
title: Managed and unmanaged AI assets
description: Learn about managing how AI assets are Managed and Unmanaged.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/assets-list-managing-and-unmanaging-assets.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [generative AI]
breadcrumb: [AI asset inventory, AI assets, AI Control Tower dashboard, Explore, AI Control Tower, Enable AI experiences]
---

# Managed and unmanaged AI assets

Learn about managing how AI assets are Managed and Unmanaged.

## Assets list

AI assets are presented in a list format and organized by display name, provider, vendor, managed by, lifecycle phase, state, status, and risk classification.

## Managed and Unmanaged assets

Starting with the AI Control Tower, Australia \(March 2026\) release, you can designate assets as managed or unmanaged directly from the list. By default, all the assets in AI Control Tower are under unmanaged assets.

When an unmanaged asset is marked as managed, it gains access to AI Control Tower capabilities such as governance, lifecycle management, value assessment, risk classification, security, and privacy. If a managed asset is switched back to an unmanaged asset, it loses access to governance, lifecycle management, value assessment, risk classification, security, and privacy controls.

**Note:**

During an upgrade

-   All existing assets revert to unmanaged, except assets with open approval requests.
-   AI Control Tower capabilities such as lifecycle, risk assessments, value, monitoring and evaluation, security are unavailable until assets are re-managed
-   Managed assets count toward your licensing usage

Automation rules automatically designate AI assets as managed based on defined criteria. For more information, see [Automation rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/automation-rules.md).

\[Omitted image "unamanged-managed-asset.png"\] Alt text: Unmanaged and managed AI assets.

**Note:** Initiating a steward review for an unmanaged AI asset triggers the lifecycle process and automatically transitions the asset to a managed state.

