---
title: Create a table vocabulary source
description: Use the values from a ServiceNow table as a vocabulary source. Your Natural Language Understanding \(NLU\) models use your provided synonym to interpret utterances that contain values from the chosen source fields of the table.
locale: en-US
release: yokohama
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [NLU vocabulary, Build and train your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# Create a table vocabulary source

Use the values from a ServiceNow table as a vocabulary source. Your Natural Language Understanding \(NLU\) models use your provided synonym to interpret utterances that contain values from the chosen source fields of the table.

## Before you begin

-   Make sure that the NLU Workbench plugin, NLU Workbench - Core plugin, NLU Common Model plugin, and Predictive Intelligence plugin are all installed and activated on your instance.
-   Role required: admin or nlu\_admin

## About this task

Add a ServiceNow table to be used as a vocabulary source. Select one or more source fields of the table. Then, provide a synonym to be used by the model when interpreting utterances that contain values from the table. Note that the **Reference** field is not supported as a source field.

When you create and sync a table vocabulary source, the values from the table in your instance are extracted, and a vocabulary source is created in the NLU Service. For more information on the NLU Service, see [NLU Service Updates](../concept/nlu-service-updates.md).

**Note:** You should not create multiple vocabulary sources that reference the same table and fields. Create only one vocabulary source \(and provide a synonym\) for the particular table and fields you want to reference in the model. Otherwise, it would cause confusion in the model and interfere with prediction quality.

In this example procedure, you want your models to be able to interpret utterances with locations. The ServiceNow location \(cmn\_location\) table already contains information regarding important locations. You set up the location table to be used as a vocabulary source.

## Procedure

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **Vocabulary Sources**.

2.  Click **ServiceNow Tables**.

3.  Click **Add another table**.

4.  On the Add another table to refer to page, configure the fields.

    1.  Select the table, handle, and synonym for the table.

        In this example, use the following configurations:

        -   **Table**: Select **Location \(cmn\_location\)**.
        -   **Handle**: Use the system-generated handle, @Location.
        -   **Synonym**: Use the system-generated synonym, Location. You can update this value to ensure that it’s a synonym for each individual item in the vocabulary source.

            **Note:** Choose a synonym that is a commonly-occurring word in the same language as your vocabulary source.

        ![Table, Handle, and Synonym fields on the Add another table to refer to page.](../images/create-table-lookupT1.png)

    2.  Select the fields you want to refer to from the source table.

        **Note:** To add multiple fields, select the plus icon.

        In this example, use the following configurations:

        -   **Field name**: Select the **Country \(country\)** and **City \(city\)** fields.
        -   **Options**: Click **Options**, then select the **Use this field to look up values** check box for both of the **Field name** values. Checking the box makes it so either a country name or a city name can be used in an utterance for finding a record in the vocabulary source. You can also use multiple comma-separate values in this field, for example, if your city column has multiple names, such as NYC, New York, and New York City.
        -   **Fields can appear together**: Leave the check box empty. This field is typically used in an NLU Search model, where users can enter words next to each other in an utterance to find a record. For example, you can enter `Pierre` `Development` while searching for an employee named Pierre who works in the Development team, where **Name** and **Team** are two fields in the table.
        ![Fields section of the Add a table to refer to page. Select one or more fields and configure the options.](../images/create-vocab-table2.png)

    3.  Configure the advanced options.

        In this example, use the following configurations:

        -   **Language**: Select **English - en**.
        -   **Filter by**: You can use the condition builder to filter the values in the source table for the vocabulary source. Leave empty for this scenario.
        -   **Refresh**: Select **Every 7 days**. By selecting this, you set the system to get new values from the table every seven days. There are different refresh options you can choose based on how often the source table is updated.
        -   **Enable Fuzzy matching**: Checking this box make it so a record can be matched even if an utterance contains a slightly misspelled word or part of a word. For example, when searching for a city such as Kansas City, you might enter Kansas City or just Kansas, and the system will still be able to match with the correct location record. Fuzzy matching may return false matches in some cases. Use fuzzy matching sparingly and test out your model before using it.
        -   **Make case sensitive**: If you don't enable fuzzy matching, you can check this box to make the values in the source table case sensitive. If an utterance doesn't use the correct cases, the model doesn't predict the intent.
        ![Advanced Options section of the Add a table to refer to page. Select a language, refresh time and any filters.](../images/create-vocab-table3.png)

5.  Click **Save**.

    **Result:** Your **@Location** table vocabulary source appears on the Vocabulary sources screen, where it begins to sync with its source table.

6.  If the sync doesn't start immediately, select the **Sync Lookup** icon on the far right to sync the source table data with the NLU Service.

    **Result:** When the sync completes, you can use the vocabulary source in your models. You don't need to retrain the model after updating a table vocabulary source.


## What to do next

Add a vocabulary source to a model by annotating an utterance. Use the @ symbol when adding an example utterance to an intent.

**Parent Topic:**[NLU vocabulary](../concept/using-nlu-vocabulary.md)

