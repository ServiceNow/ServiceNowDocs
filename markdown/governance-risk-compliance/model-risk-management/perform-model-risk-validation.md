---
title: Perform model validation
description: Perform model validation to assess and validate the model, collect required documents, report any issues, and determine if the model is fit for use. This process confirms that the model meets required standards and is ready for deployment.
locale: en-US
release: yokohama
product: Model Risk Management
classification: model-risk-management
topic_type: task
last_updated: "2025-08-13"
reading_time_minutes: 2
breadcrumb: [Use, Model Risk Management, Governance, Risk, and Compliance]
---

# Perform model validation

Perform model validation to assess and validate the model, collect required documents, report any issues, and determine if the model is fit for use. This process confirms that the model meets required standards and is ready for deployment.

## Before you begin

Role required: sn\_model\_risk\_mgmt.model\_validator

## About this task

A model risk validation task contains the following stages:

-   Document collection
-   Validation checklist
-   Issues
-   Validation outcome

You can perform the listed activities in any sequence.

## Procedure

1.  To perform model validation from the GRC tasks page, navigate to **All** &gt; **Self-Service** &gt; **Employee Center** and do the following:

    1.  Under My active items, select **GRC tasks**.

    2.  Select the model validation from the My to-dos card.

2.  To perform model validation from the Model Risk Workspace, navigate to **All** &gt; **Model Risk Workspace** and do the following:

    1.  Select the list icon ![](../../grc-compliance-case-mgmt/image/list-icon.png).

    2.  From the list, navigate to **Models** &gt; **Pre-deployment**.

    3.  Select the model for which you want to perform validation.

3.  In the Pre-deployment state, select **Open task**.

    ![Model risk validation task workflow.](../image/validation-task-workflow.png)

    The model risk validation task workflow opens.

4.  To send an evidence collection request, select **Create Request**.

    For more information, see [Request evidence for model](request-evidence-for-model.md).

5.  In the Validation Checklist stage, select **Open** to perform the validation.

6.  Respond to all the factors or questions listed in the validation task.

7.  Select **Submit**.

    After you submit your responses, you’re no longer able to modify them.

8.  In the Issues stage, add new or existing issues with the model.

    When you add new or existing issues, they are associated with the model risk and the model risk task.

9.  In the Validation Outcome stage, select the outcome whether the model is fit to use or not and send it for approval.

    **Note:** All activities must be completed before sending the task for approval.


## Result

The model validation task is submitted for approval. If no approvers are configured, the task is marked as completed.

-   **[Request evidence for model](request-evidence-for-model.md)**  
Send evidence collection request for all the required documents to complete the model validation. Evidence request helps validators to electronically request the information that they need from the model owner to perform model validation.

**Parent Topic:**[Using Model Risk Management](../concept/using-mrm.md)

**Related topics**  


[Request evidence for model](request-evidence-for-model.md)

