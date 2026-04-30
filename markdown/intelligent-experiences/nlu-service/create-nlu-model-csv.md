---
title: Create an NLU model from a CSV file
description: Upload a CSV or XLSX \(Excel Workbook\) file containing utterances and their intents to create a Natural Language Understanding \(NLU\) model. Use this method to quickly create models from your data or other exported models.
locale: en-US
release: xanadu
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Creating models, Model management, Natural Language Understanding, Enable AI experiences]
---

# Create an NLU model from a CSV file

Upload a CSV or XLSX \(Excel Workbook\) file containing utterances and their intents to create a Natural Language Understanding \(NLU\) model. Use this method to quickly create models from your data or other exported models.

## Before you begin

-   Make sure that the NLU Workbench plugin, NLU Workbench - Core plugin, and Predictive Intelligence plugin are all installed and activated on your instance.
-   You can create NLU models for Virtual Agent and AI Search.
-   Role required: admin or nlu\_admin

## About this task

In this example procedure, you're building an NLU model to help Virtual Agent understand user requests regarding calendars.

In a CSV file, you've listed the intents and utterances in two columns.

![Intent and utterance formatting in a CSV file.](../images/create-nlu-model-csv3.png "Sample CSV setup")

Note the following for creating NLU models by CSV import:

-   A model needs at least 1 intent with a minimum of 5 training utterances in each intent. For optimum performance, aim to have 15 training utterances per intent.
-   Utterances should not contain a comma.
-   Importing with a CSV file does not preserve entities. Make sure to annotate utterances as needed after importing.

## Procedure

1.  Set your scope to the application scope you want for your new model.

2.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

    The Virtual Agent tab opens by default.

3.  Select the tab for the type of model you want to create, such as AI Search.

4.  Select the **Create new model** button.

5.  In the **How do you want to create your model?** window, select **Import data from a CSV**.

6.  In the **Add some details** window, add the **Name** and **Short description** for the model.

    ![Define details screen for importing data from CSV.](../images/create-nlu-model-csv1.png)

    In this example scenario, you enter `Calendar Model` for the name and `Model for answering and performing calendar requests` for the short description.

7.  Select the language and purpose from the drop-down lists.

    In this example scenario, you select `English` and `Virtual Agent`.

8.  Click **Next**.

9.  On the **Import CSV screen**, click **Select file**.

    ![Import CSV screen for importing data from CSV.](../images/create-nlu-model-csv2.png)

10. Choose the CSV or XLSX \(Excel Workbook\) file from the pop-up.

11. Select **Next**.

    Your model starts building. After completion, select **View model** to open the model details page.


## What to do next

Add intents and training utterances to continue building the model. Add entities and vocabulary to help the model understand inputs from your users. For more information, see [Build and train your model](../concept/managing-model-content.md).

Add test utterances and intents to build the model's default test set. For more information, see [Test set creation and management](../concept/nlu-test-set-creation-management.md).

**Parent Topic:**[Creating models](../concept/creating-models.md)

