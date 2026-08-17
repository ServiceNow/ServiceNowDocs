---
title: Duplicate AI assets
description: AI asset deduplication in AI Control Tower identifies duplicate records in the AI asset inventory for AI Stewards to review and consolidate.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/review-duplicates.html
release: zurich
topic_type: concept
last_updated: "2026-06-28"
reading_time_minutes: 4
keywords: [AI asset deduplication, duplicate assets, AI Inventory, AI stewards]
breadcrumb: [Managing your AI asset inventory, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Duplicate AI assets

AI asset deduplication in AI Control Tower identifies duplicate records in the AI asset inventory for AI Stewards to review and consolidate.

## AI asset deduplication

AI asset deduplication detects AI assets in your inventory that perform the same function. AI Stewards can review and consolidate redundant entries instead of governing them independently.

Large organizations often have multiple teams building AI assets to solve the same problem. For example, an incident summarization agent might be independently developed by one team using internal resources and by another team using a cloud AI service. Since teams often work in parallel and may not know what others are working on, AI asset inventory can list the same functionality more than once under different names.

AI asset deduplication identifies these redundant entries. The feature surfaces likely duplicates for review and routes the resolution decision to AI Stewards, who confirm or dismiss each group. No automatic changes are made to asset records. Detection and flagging are informational, and all resolution actions are taken by a human reviewer.

## Key benefits

AI asset deduplication provides the following benefits:

-   Reduces governance overhead by consolidating redundant assets under a single primary record.
-   Prevents duplicate risk assessments and policy enforcement across functionally identical assets.
-   Improves accuracy of AI asset inventory reporting and audit trails.
-   Surfaces instances of uncoordinated AI development across teams and environments.

## AI asset deduplication process

Deduplication works as follows:

-   AI asset inventory scans registered assets and identifies groups of assets that appear to perform the same function. Each group is assigned a duplicate record with a unique ID in the format DUP followed by a number, for example, DUP0001028.
-   Within each group, AI asset inventory selects a main asset, the asset recommended as the primary reference going forward.
-   The duplicate group appears on the Review duplicates page in AI asset inventory, where AI Stewards can examine the group and take action.
-   The AI Steward either confirms the duplicate grouping \(**Mark as duplicates**\) or dismisses it \(**None of these are duplicates**\).

## How assets are detected as duplicates

Detection is informational only no automatic changes are made to asset records until an AI Steward confirms or dismisses a group.

The two detection methods:

1.  Predictive Intelligence \(default\): Uses machine learning clustering to identify similar assets based on shared attributes and behavior patterns. This is the original detection method and remains available.
2.  LLM-powered detection: Uses a large language model to evaluate asset similarity, producing higher-accuracy duplicate identification than predictive intelligence clustering alone.

**Note:** The system property: sn\_ai\_governance.asset\_dedup.agent.enabled acts as the primary switch controlling which detection method is active:

-   Off \(false\): The system uses Predictive Intelligence clustering only.
-   On \(true\): The LLM-powered detection is enabled for Agentic AI assets.

## Main asset selection

The system selects the main asset from the duplicate group based on the following criteria \(in order of priority\):

-   Deployment state: A deployed asset takes precedence over an asset in the draft or retired state.
-   Age: An older asset takes precedence over a newer asset with the same function.

## Effect on managed status

When an AI Steward marks a duplicate group, the following managed status changes occur:

-   Main asset: If the main asset is currently unmanaged, it is promoted to managed when the group is marked.
-   Duplicate assets: No managed status change occurs on duplicate assets. Their status remains unchanged after marking.

## Action performed on Duplicates

The following tables summarize Review duplicates page actions on the main asset and duplicates with each action's effect and resulting asset status.

|Action|Effect|Resulting asset status|
|------|------|----------------------|
|Mark assets as duplicates|Confirms the AI-identified duplicates as true duplicates. The main asset is retained as the referenced record. All other assets in the group are marked as duplicates. These duplicate assets are no longer referenced by other records or workflows.|Main asset: promoted to managed if it was previously unmanaged \(no change if already managed\). Duplicate assets: no managed status change remain as they were.|
|None of these are duplicates/This is not a duplicate \(for individual duplicate\)|Dismisses the entire duplicate group. Removes the group from the Review duplicates page and restores all assets in the group to their normal, independently referenced state. No assets are deleted.|No managed status change on any asset in the group.|
|Convert to main asset|AI Steward overrides the system-recommended main asset by selecting a different asset from the duplicates list. The previously designated main asset moves to the duplicates list; the selected asset is designated as the new main asset.|A newly designated main asset is set to the primary reference for the group. The previously designated main asset moves to the duplicates list and is treated as a duplicate going forward.|

## Notes

If the main asset is already managed when the group is marked, no status change occurs; this is the default, no-op case rather than a distinct behavior.

Convert to main asset changes in which asset is designated as main but does not, by itself, resolve the group. Confirm whether the managed status promotion described under Mark assets as duplicates applies immediately on conversion or only after a subsequent Mark assets as duplicates action.

Marking assets as duplicates can't be undone from the Review duplicates page.

