---
title: Create AI system assets
description: Create AI assets to track and manage the lifecycle of your AI systems.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Now Assist, generative AI]
breadcrumb: [Creating AI assets, Using AI Control Tower, AI Control Tower, Enable AI experiences]
---

# Create AI system assets

Create AI assets to track and manage the lifecycle of your AI systems.

## Before you begin

Role required: AI steward \[sn\_ai\_governance\_ai\_steward\] or sn\_ai\_asset\_mgmt.ai\_asset\_owner

## About this task

An AI system is a software artifact that provides AI and machine learning \(ML\) capabilities to generate outputs, such as predictions, content, recommendations, and decisions, with varying levels of autonomy. Each AI system can be associated with one or more AI models, which may also be associated with one or more prompts and datasets. These AI models, prompts, and datasets enable the AI system to process data and solve complex problems with little to no human intervention.

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Control Tower**.

2.  From the AI Control Tower, open the AI assets view.

3.  From the navigation menu of the AI assets view, navigate to **AI asset inventory** &gt; **AI Systems**.

4.  Select **Add AI system**.

5.  In the Details section of the Add AI system form, fill in the fields.

<table id="table_xhd_l25_bfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the AI system.

</td></tr><tr><td>

Provider

</td><td>

People or organization that developed the AI system.

</td></tr><tr><td>

Version

</td><td>

Version of the AI system.

</td></tr><tr><td>

Description

</td><td>

Brief description of the AI system.

</td></tr><tr><td>

Documentation

</td><td>

Additional information about the AI system, such as the method used to evaluate the efficacy of the AI system.

</td></tr><tr><td>

Managed by

</td><td>

User who is assigned to manage the AI system. This field is automatically set to the user who creates the AI system asset.**Note:** This field is editable only if you have the AI steward \[sn\_ai\_governance\_ai\_steward\] role. If you have the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role, this field is read-only.

</td></tr><tr><td>

State

</td><td>

State of the AI system. The options are **Draft** and **Deployed**.

</td></tr><tr><td>

License details

</td><td>

License that you are using for the AI system.

</td></tr><tr><td>

Asset type

</td><td>

Type of AI that your AI system is. The options are **Generative AI** and **Classic AI**.

</td></tr><tr><td>

Department

</td><td>

Department that the AI system belongs to.

</td></tr><tr><td>

Supported locations

</td><td>

Locations in which the AI system is supported.

</td></tr></tbody>
</table>6.  Select **Next**.

7.  In the Related assets section of the Add AI system form, specify the AI models, datasets, and prompts that are associated with the AI system.

    -   To specify an AI model that is associated with the AI system, search for and select the model from the **AI models** field. You can specify more than one model.
    -   To specify a dataset that is associated with the AI system, search for and select the dataset from the **Evaluation datasets** field. You can specify more than one dataset.
    -   To specify a prompt that is associated with the AI system, search for and select the prompt from the **AI prompts** field. You can specify more than one prompt.

        **Note:** If an associated AI model, dataset, or prompt isn’t available, you can add it by selecting **Add new** and then following the proceeding steps in [Create AI model assets](create-ai-model-assets.md), [Create dataset assets](create-dataset-assets.md), or [Create prompt assets](create-prompt-assets.md).

8.  Select **Submit for review**.

    **Note:** If you aren’t ready to submit the AI system for review, select **Save** instead. You can then edit it and submit it for review later by navigating to **AI assets** &gt; **Lifecycle** &gt; **Onboard** and then selecting the AI system from the list. When the AI asset record opens, select **Edit** to continue editing the AI system details.


## Result

The AI system is added to your AI asset inventory. It automatically enters the onboard stage of the AI asset life cycle and is updated with a Lifecycle status of AI steward review.

## What to do next

Users who are assigned the AI steward \(sn\_ai\_governance.ai\_steward\) role can start the review process to begin tracking and managing the life cycle of the AI system. For detailed instructions, see [Complete AI asset lifecycle](complete-ai-asset-lifecycle.md).

**Parent Topic:**[Creating AI assets](../concept/creating-ai-assets.md)

