---
title: Add an NLU model to an update set
description: Use update sets to move your Natural Language Understanding \(NLU\) models from one instance to another. Update sets include all records needed for your model to function on the target instance.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2026-04-17"
reading_time_minutes: 5
breadcrumb: [Creating models, Model management, Natural Language Understanding, Enable AI experiences]
---

# Add an NLU model to an update set

Use update sets to move your Natural Language Understanding \(NLU\) models from one instance to another. Update sets include all records needed for your model to function on the target instance.

## Before you begin

-   Make sure that the NLU Workbench plugin, NLU Workbench - Core plugin, and Predictive Intelligence plugin are all installed and activated on your instance.
-   The following instructions apply to NLU models for Virtual Agent and AI Search.
-   Role required: admin

## About this task

Use update sets to transfer a model from a source instance to a target instance. The target instance must already have the same scope as the model's scope in the source instance.

Adding a model to an update set includes the following resources:

-   Model content \(intents, utterances, entities, annotations, vocabulary, and the default test set\)
-   Associated vocabulary sources
-   Corresponding latest active ML solution
-   ML model artifacts
-   ML solution and definition \(last three runs, provided one of them was successful\)

For more information on update sets, see System update sets.

If you want to add the model to a different update set, you must make that update set the current one. See Create and select an update set as the current set.

For optimum portability, add your NLU model to a new, dedicated update set rather than to a system Default update set. To do this, a new update set must be manually created in the model's scope. An error is displayed if the current update set is the scope's Default. This error contains a link for manually creating a new update set.

If the model contains records from multiple scopes, such as vocabulary tables, its update set must have a parent-child \(batch\) structure. Follow the procedure from step 5 to create a parent-child update set.

When models \(either Global or scoped\) are moved using update sets, their training and publishing state remains the same after transfer. So a model that is trained and published before it is added to an update set does not require retraining or republishing on the target instance.

For information about parent-child update sets, see Working with batched update sets. The following video provides a demonstration of this process.

A video walkthrough of migrating NLU models by update sets in the Vancouver release.

## Procedure

1.  Select **All** and enter `sys_nlu_model.list` into the navigator.

    ![System navigator with sys_nlu_model.list entered.](../images/add-model-updateT1.png)

2.  Select the **Model Name** of the model.

    ![NLU models system list.](../images/add-model-updateT2.png)

    The **Display name** is the name you gave the model when creating it. The **Model name** is given to the model by the system.

3.  If Global is your current application, follow the prompt at the top to edit the record.

    ![Message regarding current application scope. Click "here" to edit the record and add it to an update set.](../images/add-model-updateT3.png)

4.  In the **Related Links** section, click **Add model to current update set.**

    ![Model page with the add model to current update set button highlighted.](../images/add-model-updateT4.png)

    If the model's records are all in one scope, the system adds the model to the current update set. Once completed, the record can be found in the sys\_update\_set table.

    However, the system displays an error if the designated scope is the Default scope. Continue with the following steps.

5.  If the system displays the error **You are attempting to add a record to the system default update set**, continue with the remaining steps in this procedure.

    ![Error upon Adding model to update set. The option to create a New Local Update Set is highlighted.](../images/add-model-update5V.png)

    In the error banner, select the **New Local Update Set** link to create a new update set which is not Default. In the case of a parent-child update set, the parent is first created in the model's scope. \(Any child update sets are created in a later step\).

    **New Local Update Set** opens a new record in the sys\_update\_set table.

6.  For the new update set record, provide a name, review other values including Application scope, then select **Submit and Make Current**.

    ![The form for a new Update Set, with the Submit and Make Current button highlighted.](../images/add-model-update6V.png)

    A new update set is created, and the screen re-opens to the model's record in the sys\_nlu\_model table.

7.  In the model's record in sys\_nlu\_model, select **Add model to current update set** under **Related Links**.

    When the model's records are in multiple scopes, this step creates child update sets that have Global scope.

    **Note:** If the model's records are all in one scope, the system adds the model to the current update set. Once completed, the record can be found in the sys\_update\_set table.

8.  If the model is in a non-Global scope: In the Update Sets table sys\_update\_set, locate the parent update set and its child update sets \(refresh the page if necessary\).

    -   The parent update set has the value **\(empty\)** in the Parent column.
    -   Child update sets have the name of the parent in the Parent column, and **Global** in the Application column.
    -   Both parent and child update sets contain the same value in the Batch Base column.
9.  Open the parent's record in sys\_update\_set and set the **State** field to `Complete`.

    A Confirmation dialog box pops up. Select `Yes` to confirm. This sets the parent and all child update sets to Complete.

10. To migrate the update set file, select **Export Update Set Batch to XML** in the parent's record in sys\_update\_set.

    The parent and child update sets are packaged together and exported.


## What to do next

In the target instance, navigate to **Retrieved Update Sets** and select **Import Update Sets from XML**. When unpackaged, the parent and all children will be listed in the Retrieved Update Sets table. Open the parent and select **Preview Update Set Batch**.

If a referenced record in the source instance is not present on the target instance, you may encounter errors while applying the update set. For example, the origin field on sys\_nlu\_intent could refer to an intent from a different model that doesn't exist on the target instance. You can select **Accept remote update** on the failed records to commit the update set anyway.

