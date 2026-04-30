---
title: Create prompt assets
description: Create AI assets to track and manage the life cycles of your prompts.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Now Assist, generative AI]
breadcrumb: [Creating AI assets, Using AI Control Tower, AI Control Tower, Enable AI experiences]
---

# Create prompt assets

Create AI assets to track and manage the life cycles of your prompts.

## Before you begin

Role required: AI steward \[sn\_ai\_governance\_ai\_steward\] or Asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]

## About this task

A prompt is the input that you provide to AI models to elicit specific responses or outputs. The more detailed and descriptive a prompt is, the higher the quality of the response or output. Examples of prompts include instructions, questions, and commands.

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Control Tower**.

2.  From the AI Control Tower, open the AI assets view.

3.  From the navigation menu of the AI assets view, navigate to **AI asset inventory** &gt; **Prompts**.

4.  Select **Add prompt**.

5.  In the Details section of the Add prompt form, fill in the fields.

<table id="table_xhd_l25_bfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the prompt.

</td></tr><tr><td>

Provider

</td><td>

People or organization that developed the prompt.

</td></tr><tr><td>

Version

</td><td>

Version of the prompt.

</td></tr><tr><td>

Description

</td><td>

Brief description of the prompt.

</td></tr><tr><td>

Documentation

</td><td>

Additional information about the prompt, such as the method used to evaluate the accuracy and quality of AI model responses based on the given input.

</td></tr><tr><td>

Managed by

</td><td>

User who is assigned to manage the prompt. This field is automatically set to the user who creates the prompt asset.**Note:** This field is editable only if you have the AI steward \[sn\_ai\_governance\_ai\_steward\] role. If you have the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role, this field is read-only.

</td></tr><tr><td>

State

</td><td>

State of the prompt. The options are **Draft** and **Deployed**.

</td></tr><tr><td>

Prompt information

</td><td>

Input that you want to provide to AI models.

</td></tr></tbody>
</table>6.  Select **Next**.

7.  In the Related assets section of the Add prompt form, specify the AI models that are associated with the prompt by searching for and selecting each model from the **AI model** field.

    You can specify more than one model.

    **Note:** If an associated AI model isn’t available, you can add it by selecting **Add new** and then following the proceeding steps in [Create AI model assets](create-ai-model-assets.md).

8.  Select **Submit for review**.

    **Note:** If you aren’t ready to submit the prompt for review, select **Save** instead. You can then edit it and submit it for review later by navigating to **AI assets** &gt; **Lifecycle** &gt; **Onboard** and then selecting the prompt from the list. When the AI asset record opens, select **Edit** to continue editing the prompt details.


## Result

The prompt is added to your AI asset inventory. It automatically enters the onboard stage of the AI asset life cycle and is updated with a Lifecycle status of AI steward review.

## What to do next

Users who are assigned the AI steward \(sn\_ai\_governance.ai\_steward\) role can start the review process to begin tracking and managing the life cycle of the prompt. For detailed instructions, see [Complete AI asset lifecycle](complete-ai-asset-lifecycle.md).

**Parent Topic:**[Creating AI assets](../concept/creating-ai-assets.md)

