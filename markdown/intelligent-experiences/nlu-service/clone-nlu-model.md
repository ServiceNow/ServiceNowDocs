---
title: Duplicate an NLU model
description: Duplicate an existing Natural Language Understanding \(NLU\) model to create a new one. Duplicating a model copies the settings and contents of the original model, including its default test set.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Creating models, Model management, Natural Language Understanding, Enable AI experiences]
---

# Duplicate an NLU model

Duplicate an existing Natural Language Understanding \(NLU\) model to create a new one. Duplicating a model copies the settings and contents of the original model, including its default test set.

## Before you begin

-   Make sure that the NLU Workbench plugin, NLU Workbench - Core plugin, and Predictive Intelligence plugin are all installed and activated on your instance.
-   Identify an existing NLU model to copy from. The source model should have the language and purpose you want for the new model. If a suitable model does not exist, create and train one.
-   Role required: nlu\_admin or admin.

## About this task

In this example procedure, you've already created a model that's titled NLU for Access Requests. You want to customize it for another department. You duplicate the model to create a new, separate model. To customize the new model, you then add content related to the other department.

## Procedure

1.  Set your scope to the scope of the model you want to create.

    After creation, these model settings cannot be changed: language, purpose, scope.

2.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

3.  On the far right column of the model list, select the **More options** menu for the model you want to duplicate.

    ![More options menu with Duplicate this model selected.](../images/clone-nlu-modelT1.png)

4.  Select **Duplicate this model**.

5.  In the **Duplicate this Model** window, enter a name and description for the new model.

    ![Duplicate this Model window.](../images/clone-nlu-modelT2.png)

    In this example scenario, you enter `NLU for Access Requests Copy1` for the description.

6.  Click **Duplicate**.

    The system duplicates the model. The **Model details** page loads for your new model.


## What to do next

You can customize the new model by adding new content to it. Train, test, and publish the new model. For more information, see [Build and train your model](../concept/managing-model-content.md).

To duplicate an entire model group, or one of the models in a group, see [Multilingual model management](../concept/multilingual-model-managent.md).

To transfer a model to a different instance, see [Add an NLU model to an update set](add-model-update-set.md).

**Parent Topic:**[Creating models](../concept/creating-models.md)

