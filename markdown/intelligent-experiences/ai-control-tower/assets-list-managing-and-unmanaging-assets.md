---
title: AI assets- Managed and Unmanaged
description: Learn about managing how the AI assets are managed and unmanaged.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/assets-list-managing-and-unmanaging-assets.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [generative AI]
breadcrumb: [AI asset inventory, AI assets, AI Control Tower dashboard, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# AI assets- Managed and Unmanaged

Learn about managing how the AI assets are managed and unmanaged.

## AI assets list

AI assets are presented in a list format and organized by display name, provider, vendor, managed by, state, status, asset state, asset status, and risk classification.

Starting with the AI Control Tower AI Control Tower Australia release, you can designate assets as managed or unmanaged directly from the inventory list. By default, all assets in AI Control Tower are Unmanaged.

## Unmanaged asset to Managed asset

When an unmanaged asset is marked as managed, it gains access to AI Control Tower capabilities such as governance, lifecycle, value assessment, risk classification, monitoring and evaluation, security, and privacy controls.

From the AI asset inventory, select an asset and click **Move to Managed**. A dialog box will open with asset state details and the information. ''Managed assets are actively monitored and governed, which improves your inventory visibility''

## Managed asset to Unmanaged asset

When a managed asset is marked as unmanaged, it loses access to AI Control Tower capabilities such as governance, lifecycle, value assessment, risk classification, monitoring and evaluation, security and privacy controls.

From the AI asset inventory managed list, select an asset and click **Unmanage**. A dialog box will open with asset state details and the following information.

Once you Unmanage these AI system:

-   Any active workflows, tasks, and governance processes using them will be canceled
-   They won't be considered for value tracking

## Upgrade

When you upgrade from a pre-March release to a post-March release, AI Control Tower automatically updates the managed status of all existing active assets to managed.

-   This automatic status update occurs once after the upgrade and does not repeat on subsequent upgrades.
-   Now Assist only users aren't affected as their ServiceNow assets remain unmanaged by default, which is consistent with existing behavior.
-   Assets added or discovered after the upgrade remain in unmanaged status and this is consistent with the existing behavior.
-   AI Control Tower continues to collect and retain usage and observability data for both managed and unmanaged assets.
-   Data, calculations, and evaluations for unmanaged assets are excluded from the AI Control Tower experience across all pillars.
-   Guidance on data access and storage for unmanaged assets is available to help prevent unauthorized use.

**Note:** Initiating an AI steward review for an unmanaged AI asset triggers the lifecycle process and automatically transitions the asset to a managed state.

Automation Rules

Automation rules automatically designate AI assets as managed based on defined criteria. For information, see [Automation rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/automation-rules.md)

