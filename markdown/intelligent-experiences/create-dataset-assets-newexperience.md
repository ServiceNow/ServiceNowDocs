---
title: Create dataset assets
description: Create AI assets to track and manage the life cycles of your datasets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/create-dataset-assets-newexperience.html
release: australia
topic_type: task
last_updated: "2026-04-13"
reading_time_minutes: 4
breadcrumb: [Creating AI assets manually, Managing your AI asset inventory, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Create dataset assets

Create AI assets to track and manage the life cycles of your datasets.

## Before you begin

Role required: AI steward \[sn\_ai\_governance\_ai\_steward\] or AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]

**Note:** Users with the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role can only create AI assets and submit them for life-cycle review. They can't start or complete any life-cycle reviews.

## About this task

A Model Context Protocol \(MCP\) server is an external service or integration endpoint that AI agents connect to retrieve context, execute tools, or access data.

## Procedure

1.  Navigate to **All** &gt; **Al Control Tower** &gt; **Home** &gt; **Inventory**.

2.  On the Inventory page, select **Add AI asset**.

    The Add AI asset dialog box opens.

3.  In the dialog box, select **Enter asset details**.

4.  From the list of available asset types, select **Dataset**.

    The dialog box closes and you're automatically redirected to the Add dataset asset form.

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

Asset state

</td><td>

Current state of the dataset. Select one of the following options:-   **Design**
-   **Build**
-   **Available**
-   **Deployed**
**Note:** A concatenation of asset state and asset status appears on each asset record page The available UI actions on the asset record page vary based on the current state and status.

</td></tr><tr><td>

Asset status

</td><td>

Status of the dataset in a workflow. If this field is empty, that indicates the dataset is not going through any workflow. A value indicates if this dataset is going through a workflow, is approved or is rejected.**Note:** A concatenation of asset state and asset status appears on each asset record page The available UI actions on the asset record page vary based on the current state and status.

</td></tr><tr><td>

Managed by

</td><td>

User who is assigned to manage the dataset. This field is automatically set to the user who creates the dataset asset.**Note:** This field is editable only if you have the AI steward \[sn\_ai\_governance\_ai\_steward\] role. If you have the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role, this field is read-only.

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
</table>6.  Select **Save draft** to save the details in the form or select **Cancel** that provides you with the following options:

    -   **Keep editing**: to continue editing the form.
    -   **Save draft and exit**: saves the form and you exit the form.
    -   **Discard and exit**: your unsaved changes are discarded and you exit the form.
7.  Select **Submit for review**.

    The Asset record page opens and your asset is in an unmanaged state. You can edit details related to your asset on the **Details** tab by using the pencil icon in the sections titled **About this asset** and **Use and purpose**.

8.  If you have the AI steward \[sn\_ai\_governance\_ai\_steward\] role, select the **Actions** menu and then select **Start lifecycle review**.

    **Important:** Only users with the AI steward \[sn\_ai\_governance\_ai\_steward\] role can start the life-cycle review.

    The Start AI steward review dialog box opens.

9.  In the **Managed by** field of the dialog box, search for and select the user that you want to assign the life-cycle review to.

    **Important:** You must select a user with the AI steward \[sn\_ai\_governance\_ai\_steward\] role.

10. Select **Start review**.

    The asset automatically changes from an unmanaged asset to a managed asset and starts the onboarding workflow. The Lifecycle tab now contains three sub tabs: **Onboard**, **Maintain**, and **Retire**. The **Maintain**, and **Retire** are disabled and are enabled once onboarding is complete.

    The **Onboard** sub tab contains the Onboarding playbook with tasks displayed. If tasks are not already present in the Onboarding playbook, users with the AI steward \[sn\_ai\_governance\_ai\_steward\] role can create tasks by selecting **New** and assign them to other AI stewards.

11. If you're assigned to the life-cycle review, select **Mark complete** to complete each activity in the onboarding playbook.

    If your tasks are open and you select **Mark complete**, those tasks automatically get closed with the **Closed skipped** state and you move to the next stage of onboarding. Once you move forward, you can no longer create tasks in the previous stage.

    You can select the **Actions** menu and **Reject request** to cancel the onboarding playbook and mark this asset as unmanaged.

    When all stages in the onboarding playbook are marked as complete, the playbook status updates to **Completed**. The **Maintain** and **Retire** tabs show a status of **Not Started**.

    **Note:** The end-to-end onboarding process from start to finish may take a few days.


