---
title: Edit a value template
description: Edit a value template to update how value is calculated for AI assets.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using value templates, Use, AI Control Tower, Enable AI experiences]
---

# Edit a value template

Edit a value template to update how value is calculated for AI assets.

## Before you begin

Role required: \[sn\_ai\_governance\_ai\_steward\]

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Control Tower**.

2.  Select the **AI asset inventory** tab and navigate to the asset that you want to edit the value template for.

3.  In the **Value template** tab, select **Duplicate**.

    A new tab with the same details as the original template opens for you to edit.

4.  Edit the value template according to your requirements.

5.  Select **Save as draft**.

6.  Validate and test the formula against the available dataset by selecting **Validate and calculate output**.

    You can preview calculations from the past 30 days using the new template before publishing. This functionality enables you to evaluate the impact of the new template while preserving the historical data associated with the previous version.

7.  If you’re satisfied with the output, publish the template by selecting **Publish**.

    When a value template is published, it’s modified across all instances and subsequent calculations are based on the new template.


