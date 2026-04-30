---
title: Sync a table vocabulary source
description: Synchronize your table vocabulary sources to obtain the latest changes to the ServiceNow source table. Synchronizing your vocabulary sources ensures your NLU models have the latest values when predicting intents.
locale: en-US
release: xanadu
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2024-09-13"
reading_time_minutes: 2
breadcrumb: [NLU vocabulary, Build and train your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# Sync a table vocabulary source

Synchronize your table vocabulary sources to obtain the latest changes to the ServiceNow source table. Synchronizing your vocabulary sources ensures your NLU models have the latest values when predicting intents.

## Before you begin

-   Make sure that the NLU Workbench plugin, NLU Workbench - Core plugin, NLU Common Model plugin, and Predictive Intelligence plugin are all installed and activated on your instance.
-   Role required: admin or nlu\_admin

## About this task

When you reference a vocabulary source in an utterance, it pulls the values at the time the model is trained. However, if the table values change over time, the model still references the values from the last training session.

You can select a schedule to automatically refresh the vocabulary values used by NLU. This schedule can be edited later. For more information, see [Create a table vocabulary source](create-table-lookup-source.md).

You can also manually sync a table vocabulary source, such as before model training.

**Note:** If an utterance references a table vocabulary source that has never been synchronized, the model fails to train. Check the vocabulary source's current status, and sync manually if **Never synced**.

In the following example scenario, you're manually syncing the @AccessRoles vocabulary source to the Catalog Item table.

## Procedure

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **Vocabulary Sources**.

2.  In the ServiceNow Tables tab, point just to the right of the **Refresh** column to invoke the **Sync lookup** icon.

    ![ServiceNow Tables tab of the Vocabulary Sources screen. Pointing to the refresh column invokes the sync lookup button.](../images/nlu-models5.png)

3.  Select **Sync**.

    The vocabulary source starts synchronization.


## What to do next

The syncing operation can take some time, depending on the source table size.

![ServiceNow Tables tab of the Vocabulary Sources page. The Current status column shows the progress or condition of the synchronization job.](../images/nlu-models6.png "ServiceNow Tables tab of the Vocabulary Sources page")

The values in the Last refresh and Current status columns reflect the current status of the vocabulary source.

![ServiceNow Tables tab of the Vocabulary Sources page. The Last refresh and Current status columns provide synchronization information.](../images/nlu-models7.png "ServiceNow Tables tab of the Vocabulary Sources page")

Proceed to train your model. For more information on model training, see [Train and try your NLU model](test-train-nlu-model.md).

For information about errors when syncing a table vocabulary source, see article [KB1588239](https://support.servicenow.com/kb_view.do?sysparm_article=KB1588239) in the Now Support Knowledge Base.

**Parent Topic:**[NLU vocabulary](../concept/using-nlu-vocabulary.md)

**Related topics**  


[Create a table vocabulary source](create-table-lookup-source.md)

