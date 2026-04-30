---
title: Export an NLU model
description: Export a Natural Language Understanding \(NLU\) model to create a CSV file of the intents and utterances. You can then use the CSV file to edit, share, and import.
locale: en-US
release: zurich
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Creating models, Model management, Natural Language Understanding, Enable AI experiences]
---

# Export an NLU model

Export a Natural Language Understanding \(NLU\) model to create a CSV file of the intents and utterances. You can then use the CSV file to edit, share, and import.

## Before you begin

-   Make sure that the NLU Workbench plugin, NLU Workbench - Core plugin, and Predictive Intelligence plugin are all installed and activated on your instance.
-   Role required: nlu\_editor, nlu\_admin, or admin

## About this task

Exporting an NLU model creates a CSV file. The file contains a table of the utterances from the model and the matched intents. The data comes from the **Utterances** tab for each intent in the model.

**Note:** The file doesn't contain the sources of the utterances. Also the file doesn't transfer entities or vocabulary associated with the model. To export all model data, see [Add an NLU model to an update set](add-model-update-set.md).

## Procedure

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

    The Virtual Agent tab opens by default.

2.  Select the tab for your model's application, and find your model in the list.

3.  Scroll to the far right column of your model's row, and select the more options menu of the model you want to export.

    ![More options menu with the export model as CSV option highlighted.](../images/export-nlu-modelT1.png)

4.  In the more options menu, click **Export model as CSV**.

    The model CSV file downloads to your browser.


## What to do next

You can use the CSV file to share the model or edit the utterances. You can also create a model by importing the CSV file. For more information, see [Create an NLU model from a CSV file](create-nlu-model-csv.md).

**Parent Topic:**[Creating models](../concept/creating-models.md)

