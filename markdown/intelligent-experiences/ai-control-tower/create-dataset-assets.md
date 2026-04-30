---
title: Create dataset assets
description: Create AI assets to track and manage the life cycles of your datasets.
locale: en-US
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Now Assist, generative AI]
breadcrumb: [Creating AI assets, Use, AI Control Tower, Enable AI experiences]
---

# Create dataset assets

Create AI assets to track and manage the life cycles of your datasets.

## Before you begin

Role required: sn\_ai\_governance\_ai\_steward or sn\_ai\_asset\_mgmt.ai\_asset\_owner

## About this task

A dataset is a collection of structured or unstructured data that you can use to train and test AI models. Datasets can help you improve the performance and efficacy of your AI models.

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Control Tower**.

2.  From the AI Control Tower, open the AI assets view.

3.  From the navigation menu of the AI assets view, navigate toeither **AI asset inventory - Managed** &gt; **Datasets**or **AI asset inventory - Unmanaged** &gt; **Datasets**.

4.  Select **Add dataset**.

5.  On the form, fill in the fields.

<table id="table_xhd_l25_bfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the dataset.

</td></tr><tr><td>

Provider

</td><td>

People or organization that developed the dataset.

</td></tr><tr><td>

Acceptable usage

</td><td>

Acceptable use for the dataset. You can specify more than one use.

</td></tr><tr><td>

Version

</td><td>

Version of the dataset.

</td></tr><tr><td>

Data type

</td><td>

Type of data that the dataset contains. You can specify more than one data type.

</td></tr><tr><td>

Source

</td><td>

Source of the dataset, such as internal customer data within an organization or publicly available data from a government agency.

</td></tr><tr><td>

Description

</td><td>

Brief description of the dataset.

</td></tr><tr><td>

Managed by

</td><td>

User who is assigned to manage the dataset. This field is automatically set to the user who creates the dataset asset.**Note:** This field is editable only if you have the AI steward \(sn\_ai\_governance\_ai\_steward\) role. If you have the AI asset owner \(sn\_ai\_asset\_mgmt.ai\_asset\_owner\) role, this field is read-only.

</td></tr><tr><td>

State

</td><td>

State of the dataset. The options are **Draft** and **Deployed**.

</td></tr><tr><td>

Creation type

</td><td>

Method by which the dataset was created. Select one of the following options:-   **Curated**: The dataset was created through careful selection, organization, and refinement of data.
-   **Derived**: The dataset was created by processing, transforming, or combining data from existing datasets.
-   **Synthetic**: The dataset was created by using artificial data that mimics real-word data.


</td></tr><tr><td>

Base datasets

</td><td>

Base dataset that the dataset was built from.

</td></tr><tr><td>

Department

</td><td>

Department that the dataset belongs to.

</td></tr><tr><td>

Dataset creation date

</td><td>

Date and time that the dataset was created.

</td></tr><tr><td>

Dataset card

</td><td>

Brief document that describes important information about the dataset, including the context, intended use, limitations, and potential biases of the dataset.

</td></tr></tbody>
</table>6.  Select **Submit for review**.

    **Note:** If you aren’t ready to submit the dataset for review, select **Save** instead. You can then edit it and submit it for review later by navigating to **AI assets** &gt; **Lifecycle** &gt; **Onboard** and then selecting the dataset from the list. When the AI asset record opens, continue editing the dataset details.


## Result

The dataset is added to your AI asset inventory. It automatically enters the onboard stage of the AI asset life cycle and is updated with a Lifecycle status of AI steward review.

## What to do next

Users who are assigned the AI steward \(sn\_ai\_governance.ai\_steward\) role can start the review process to begin tracking and managing the life cycle of the dataset. For detailed instructions, see [Complete AI asset lifecycle](complete-ai-asset-lifecycle.md).

**Parent Topic:**[Creating AI assets](../concept/creating-ai-assets.md)

