---
title: Edit a value template
description: Edit a value template to update how value is calculated for AI assets.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using value templates, Using AI Control Tower, AI Control Tower, Enable AI experiences]
---

# Edit a value template

Edit a value template to update how value is calculated for AI assets.

## Before you begin

Role required: AI steward \[sn\_ai\_governance\_ai\_steward\] and AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Control Tower**.

2.  From the AI Control Tower, open the AI assets view.

3.  From the navigation menu of the AI assets view, navigate to **Productivity** &gt; **Value templates**.

4.  Select the asset that you want to edit the value template for and click **Duplicate**.

    A new dialogue box is displayed for you to select what to duplicate and then a tab with the same details as the original template opens for you to edit.

    **Note:** Duplicating a template changes its state to Draft so that you can edit it. For a published template, you can edit only a limited number of fields in the template and save it.

5.  Edit the value template according to your requirements.

6.  Validate and test the formula against the available dataset by selecting **Validate and calculate output**.

    You can preview calculations from the past 30 days using the new template before publishing. This functionality enables you to evaluate the impact of the new template while preserving the historical data associated with the previous version.

7.  If you’re satisfied with the output, publish the template by selecting **Publish template**.

    When a value template is published, it’s modified across all instances and subsequent calculations are based on the new template.

    After a template is published, you can't edit the basic information. But you can still add more assets for mapping to it. Testing is unavailable for published templates.


**Parent Topic:**[Using value templates](../concept/using-value-templates.md)

