---
title: AI assets- Managed and Unmanaged
description: Learn about managing how the AI assets are Managed and Unmanaged.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/assets-list-managing-and-unmanaging-assets.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [generative AI]
breadcrumb: [AI asset inventory, AI assets, AI Control Tower dashboard, Explore, AI Control Tower, Enable AI experiences]
---

# AI assets- Managed and Unmanaged

Learn about managing how the AI assets are Managed and Unmanaged.

## AI assets list

AI assets are presented in a list format and organized by display name, provider, vendor, managed by, state, status, asset state, asset status, and risk classification.

Starting with the AI Control Tower, Australia \(March 2026\) release, you can designate assets as Managed or Unmanaged directly from the list. By default, all the assets in AI Control Tower are under Unmanaged assets.

## Unmanaged asset to Managed asset

When an Unmanaged asset is marked as Managed, it gains access to AI Control Tower capabilities such as governance, lifecycle management, value assessment, risk classification, monitoring and evaluation, security, and privacy controls.

From the AI asset inventory Unmanaged list, select an asset and click **Move to Managed**. A dialog box will open with asset state details and the information. ''Managed assets are actively monitored and governed, which improves your inventory visibility''

## Managed asset to Unmanaged asset

When an Managed asset is marked as Unmanaged, it loses access to AI Control Tower capabilities such as governance, lifecycle management, value assessment, risk classification, monitoring and evaluation, security and privacy controls.

From the AI asset inventory managed list, select an asset and click **Unmanage**. A dialog box will open with asset state details and the following information.

Once you Unmanage these AI system:

-   Any active workflows, tasks, and governance processes using them will be canceled.
-   They won't be considered for value tracking.

## Upgrade

Let's explore the upgrade in two scenarios:

1.  Managed to Unmanaged asset- When you upgrade from a pre-March release to a post-March release, AI Control Tower automatically sets the managed status of all existing active assets in the inventory to Managed for AICT Enterprise or Foundation users.
    -   This automatic status update occurs once after the upgrade and does not repeat on subsequent upgrades
    -   Now Assist only users aren't affected as their ServiceNow assets remain Unmanaged by default, and existing behavior is unchanged
    -   Assets added or discovered after the upgrade remain in Unmanaged status and this is consistent with the existing behavior
    -   The AI Control Tower continues to collect and retain usage and observability data for both Managed and Unmanaged assets
    -   Data, calculations, and evaluations for Unmanaged assets are excluded from the AI Control Tower experience across all pillars
    -   Guidance on data access and storage for Unmanaged assets is available to help prevent unauthorized use
2.  Unmanaged to Managed asset- During the first upgrade to the feature, all the active assets will be in managed, only if you're an AICT Enterprise user.

**Note:** Initiating an AI steward review for an Unmanaged AI asset triggers the lifecycle process and automatically transitions the asset to a Managed state.

Automation Rules

Automation rules automatically designate AI assets as managed based on defined criteria. For information, see [Automation rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/automation-rules.md)

