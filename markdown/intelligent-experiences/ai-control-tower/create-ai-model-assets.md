---
title: Create AI model assets
description: Create AI assets to track and manage the life cycles of your AI models.
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

# Create AI model assets

Create AI assets to track and manage the life cycles of your AI models.

## Before you begin

Role required: AI steward \[sn\_ai\_governance\_ai\_steward\] or Asset Owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]

## About this task

An AI model is a program that is trained to process data and generate outputs, such as predictions, content, recommendations, and decisions, without human intervention. You can use an AI model to perform a specific task, such as image recognition, data classification, or price prediction.

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Control Tower**.

2.  From the AI Control Tower, open the AI assets view.

3.  From the navigation menu of the AI assets view, navigate to **AI asset inventory** &gt; **AI Models**.

4.  Select **Add AI model**.

5.  In the Details section of the Add AI model form, fill in the fields.

<table id="table_osx_kg5_bfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the AI model.

</td></tr><tr><td>

Provider

</td><td>

People or organization that developed the AI model.

</td></tr><tr><td>

Version

</td><td>

Version of the AI model.

</td></tr><tr><td>

Supported languages

</td><td>

Languages that are supported by the AI model.

</td></tr><tr><td>

Deployment guidelines

</td><td>

Guidelines or instructions on how to deploy the AI model.

</td></tr><tr><td>

Training procedure

</td><td>

Method that you’re using to train the AI model.

</td></tr><tr><td>

Context window

</td><td>

Maximum number of tokens that the AI model can process and recall when generating outputs.

</td></tr><tr><td>

Model size in MB

</td><td>

Size of the AI model in megabytes \(MB\).

</td></tr><tr><td>

Model parameters info

</td><td>

Internal variables that the AI model learns during training to process data and generate outputs.

</td></tr><tr><td>

Description

</td><td>

Brief description of the AI model.

</td></tr><tr><td>

Managed by

</td><td>

User who is assigned to manage the AI model. This field is automatically set to the user who creates the AI model asset.**Note:** This field is editable only if you have the AI steward \[sn\_ai\_governance\_ai\_steward\] role. If you have the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role, this field is read-only.

</td></tr><tr><td>

State

</td><td>

State of the AI model. The options are **Draft** and **Deployed**.

</td></tr><tr><td>

License details

</td><td>

License that you are using for the AI model.

</td></tr><tr><td>

Base model

</td><td>

Base model, also known as a foundation model or pre-trained model, that the AI model was built from.

</td></tr><tr><td>

Department

</td><td>

Department that the AI model belongs to.

</td></tr><tr><td>

Supported locations

</td><td>

Locations in which the AI model is supported.

</td></tr><tr><td>

Model card

</td><td>

Brief document that describes important information about the AI model, including the context, intended use, training data, and limitations of the model.

</td></tr><tr><td>

Model weights info

</td><td>

Numerical parameters that define how the AI model learns during training so that it can generate more desired outputs.

</td></tr><tr><td>

Required infrastructure

</td><td>

Integrated software and hardware components that are required for developing, deploying, and managing the AI model.

</td></tr><tr><td>

Evaluation metrics report

</td><td>

Report that provides data for the metrics that you’re using to evaluate the effectiveness of the AI model.

</td></tr></tbody>
</table>6.  Select **Next**.

7.  In the Related assets section of the Add AI model form, specify the datasets and prompts that are associated with the model.

    -   To specify a dataset that is associated with the AI model, search for and select the dataset from the **Evaluation datasets** field. You can specify more than one dataset.

    -   To specify a prompt that is associated with the AI model, search for and select the prompt from the **AI prompts** field. You can specify more than one prompt.

        **Note:** If an associated dataset or prompt isn’t available, you can add it by selecting **Add new** and then following the proceeding steps in [Create dataset assets](create-dataset-assets.md) or [Create prompt assets](create-prompt-assets.md).

8.  Select **Submit for review**.

    **Note:** If you aren’t ready to submit the AI model for review, select **Save** instead. You can then edit it and submit it for review later by navigating to **AI assets** &gt; **Lifecycle** &gt; **Onboard** and then selecting the AI model from the list. When the AI asset record opens, select **Edit** to continue editing the AI model details.


## Result

The AI model is added to your AI asset inventory. It automatically enters the onboard stage of the AI asset life cycle and is updated with a Lifecycle status of AI steward review.

## What to do next

Users who are assigned the AI steward \(sn\_ai\_governance.ai\_steward\) role can start the review process to begin tracking and managing the life cycle of the AI model. For detailed instructions, see [Complete AI asset lifecycle](complete-ai-asset-lifecycle.md).

**Parent Topic:**[Creating AI assets](../concept/creating-ai-assets.md)

