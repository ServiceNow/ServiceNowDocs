---
title: Create AI model assets
description: Create AI assets to track and manage the life cycles of your AI models.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/create-ai-model-assets-newexperience.html
release: australia
topic_type: task
last_updated: "2026-04-10"
reading_time_minutes: 5
breadcrumb: [Creating AI assets manually, Managing your AI asset inventory, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Create AI model assets

Create AI assets to track and manage the life cycles of your AI models.

## Before you begin

Role required: AI steward \[sn\_ai\_governance\_ai\_steward\] or AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]

**Note:** Users with the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role can only create AI assets and submit them for life-cycle review. They can't initiate or complete any life-cycle reviews.

## About this task

An AI model is a program that is trained to process data and generate outputs, such as predictions, content, recommendations, and decisions, without human intervention. You can use an AI model to perform a specific task, such as image recognition, data classification, or price prediction.

When you manually create an asset, the asset defaults to a **Design** state.

## Procedure

1.  Navigate to **All** &gt; **Al Control Tower** &gt; **Home** &gt; **Inventory**.

2.  On the Inventory page, select **Add AI asset**.

    The Add AI asset dialog box opens.

3.  In the dialog box, select **Enter asset details**.

4.  From the list of available asset types, select **AI model**.

    The dialog box closes and you are automatically redirected to the Add AI model asset form.

5.  In the Details section of the form, fill in the fields.

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

Asset state

</td><td>

Current state of the AI model. Select one of the following options:-   **Design**
-   **Build**
-   **Available**
-   **Deployed**


</td></tr><tr><td>

Managed by

</td><td>

User who is assigned to manage the AI model. This field is automatically set to the user who creates the AI model asset.**Note:** This field is editable only if you have the AI steward \[sn\_ai\_governance\_ai\_steward\] role. If you have the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role, this field is read-only.

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
</table>6.  Select **Next** to move to the next section of the form.

    You can also select **Save draft** to save the details in the form or select **Cancel** that provides you with the following options:

    -   **Keep editing**: to continue editing the form.
    -   **Save draft and exit**: saves the form and you exit the form.
    -   **Discard and exit**: your unsaved changes are discarded and you exit the form.
7.  In the Relationships section of the form, associate the AI model with related datasets.

    Related datasets include any collections of data that can help test or train the AI model.

    1.  Depending on the type of related dataset that you want associate the AI model with, select one of the following options from the asset type menu:

        -   To associate the AI model with a dataset that can help test it, select **Evaluation datasets**.
        -   To associate the AI model with a dataset that can help train it, select **Training datasets**.
        -   To associate the AI model with a configuration item \(CI\), select **Configuration items**
        The corresponding asset list opens.

    2.  Associate the AI model with a related dataset.

        1.  Select **Add from inventory**.
        2.  In the dialog box, select the check box for the related dataset that you want to associate the AI model with.

            **Note:** If you want to associate the AI model with multiple related datasets, select the check box for each dataset.

        3.  Select **Add**.
8.  Select **Submit for review**.

    The Asset record page opens and your asset is in an unmanaged state. You can edit details related to your asset on the **Details** tab by using the pencil icon in the sections titled **About this asset** and **Use and purpose**.

9.  If you have the AI steward \[sn\_ai\_governance\_ai\_steward\] role, select the **Actions** menu and then select **Start lifecycle review**.

    **Important:** Only users with the AI steward \[sn\_ai\_governance\_ai\_steward\] role can start the life-cycle review.

    The Start AI steward review dialog box opens.

10. In the **Managed by** field of the dialog box, search for and select the user that you want to assign the life-cycle review to.

    **Important:** You must select a user with the AI steward \[sn\_ai\_governance\_ai\_steward\] role.

11. Select **Start review**.

    The asset automatically changes from an unmanaged asset to a managed asset and starts the onboarding workflow. The Lifecycle tab now contains three sub tabs: **Onboard**, **Maintain**, and **Retire**. The **Maintain**, and **Retire** sub tabs are disabled and are enabled once onboarding is complete.

    The **Onboard** sub tab contains the Onboarding playbook with tasks displayed. If tasks are not already present in the Onboarding playbook, users with the AI steward \[sn\_ai\_governance\_ai\_steward\] role can create tasks by selecting **New** and assign them to other AI stewards.

12. If you're assigned to the life-cycle review, select **Mark complete** to complete each activity in the onboarding playbook.

    If your tasks are open and you select **Mark complete**, those tasks automatically get closed with the **Closed skipped** state and you move to the next stage of onboarding. Once you move forward, you can no longer create tasks in the previous stage.

    You can select the **Actions** menu and select **Reject request** to cancel the onboarding playbook and mark this asset as unmanaged.

    When all stages in the onboarding playbook are marked as complete, the playbook status updates to **Completed**. The **Maintain** and **Retire** tabs show a status of **Not Started**.

    **Note:** The end-to-end onboarding process from start to finish may take a few days.


