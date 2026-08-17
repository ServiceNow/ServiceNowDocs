---
title: Update the use and purpose of an AI asset
description: Update the use and purpose values for an AI asset when its operating characteristics or business outcome change so that risk classifications and governance controls continue to reflect how the asset behaves.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/disc-asset-update-use-purpose.html
release: australia
topic_type: task
last_updated: "2026-05-05"
reading_time_minutes: 2
keywords: [AI asset, use and purpose, system autonomy, human involvement, interaction type, intended outcome]
breadcrumb: [Managing AI asset details, Working with AI asset records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Update the use and purpose of an AI asset

Update the use and purpose values for an AI asset when its operating characteristics or business outcome change so that risk classifications and governance controls continue to reflect how the asset behaves.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward or sn\_ai\_asset\_mgmt.ai\_asset\_owner

**Note:** Users with the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role can view details for any asset but can only update assets that they own.

## About this task

Use and purpose values describe how an AI system operates and what outcome it produces. These values are first captured during asset onboarding, but they can change over time. For example, an AI system that originally proposed actions for a user to approve might later be reconfigured to act on its own. When that happens, the asset's **System autonomy level** and **Level of human involvement** values no longer reflect how the asset actually behaves, and any risk classification or control assignment based on those values is out of date.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Inventory**.

2.  Open the asset record for the AI asset that you want to update.

3.  Select the **Details** tab and locate the **Use and purpose** section.

4.  In the **Use and purpose** section, update the relevant fields.

    For example, an AI system that previously required user approval before acting has been reconfigured to act on its own. In this case, change **System autonomy level** from **Semi-Automated \(acts with confirmation\)** to **Fully Automated Execution**, and change **Level of human involvement** from **AI-Initiated with User Approval** to **Fully Automated Workflow**.

    For a description of the fields and their values, see [Use and purpose fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/disc-asset-use-purpose-fields.md).

5.  Select the check icon to save your changes.


## Result

The updated values appear in the **Use and purpose** section and are referenced in subsequent reviews, risk classifications, and audit responses.

## What to do next

If the change affects how the asset operates, review the controls and governance assignments that depend on these values to confirm they still apply.

**Parent Topic:**[Managing AI asset details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/disc-ai-asset-details.md)

