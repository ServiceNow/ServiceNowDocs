---
title: Create a mapped entity
description: Create an entity mapped to a vocabulary source, or to a list of values you manually create for the entity. Mapped entities can help provide multiple values the model can use as context when interpreting utterances.
locale: en-US
release: zurich
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [NLU entities, Build and train your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# Create a mapped entity

Create an entity mapped to a vocabulary source, or to a list of values you manually create for the entity. Mapped entities can help provide multiple values the model can use as context when interpreting utterances.

## Before you begin

-   Make sure that the NLU Workbench plugin, NLU Workbench - Core plugin, NLU Common Model plugin, and Predictive Intelligence plugin are all installed and activated on your instance.
-   Create or use an existing NLU model for Virtual Agent or AI Search.
-   Create or use an existing intent.
-   Role required: nlu\_editor, nlu\_admin, or admin. The nlu\_editor must be assigned to the model.

## About this task

Mapped entities take the words of the utterance and extract value based on a designated source. The model uses the source when predicting the intent.

When you create a mapped entity, you have the following three options for the source.

-   Manual list of values: Use this option to manually enter a list of values for the entity. For example, you could create a mapped entity named priority and map it to the word urgent in an utterance, then manually build a list for it with values of High, Medium, and Low.
-   Table vocabulary source: Use this option if you have a ServiceNow table that has the values you're looking for. Mapping an entity to a table vocabulary source enables the entity to reference multiple values from the table. For example, use a @Location vocabulary source, where @Location has values for cities and countries.
-   List vocabulary source: Use this option if you don't have a ServiceNow table that has the values you're looking for. For example, use a @mouse vocabulary source, where @mouse has values for various models of hand-held computer devices.

In this example procedure, you create a mapped entity for urgency.

## Procedure

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

    The Virtual Agent tab opens by default.

2.  Select the tab for your model's application, then the name of your model.

3.  On the model details page, select the **Intents** tab.

4.  In the Intents section of the model, select the name of an intent.

    For this example procedure, you select **\#SubmitRequest**.

5.  In the Utterances tab, select a word in an utterance

    In this scenario, you select the word urgent in the utterance I have an urgent request.

6.  Select **Mapped entities**.

7.  Select **Create New Entity.**

    ![Create new entity button in the entity window in the utterances tab.](../images/create-mapped-entityT1.png)

8.  On the form, configure the fields.

<table id="table_z33_p1y_h5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entity Name

</td><td>

Name for the entity.

</td></tr><tr><td>

Type

</td><td>

Type of entity.

</td></tr><tr><td>

Model availability

</td><td>

Select this option if you want this entity to be included in all intents in your model.

</td></tr><tr><td>

Source

</td><td>

Source of the entity values.

</td></tr><tr><td>

Provide values for this entity

</td><td>

Values used to provide context for the model.

</td></tr></tbody>
</table>    For this example procedure, use the following configurations:

    -   **Entity Name**: `priority`
    -   **Type**: Mapped
    -   **Model availability**: Select the check box
    -   **Source:** **Use this if you have a table or list to refer to where the actual values and values they're mapped to are stored**
    -   **Mapped value for the entity**: `high, medium, low`.
    ![Create a new entity window for a mapped entity.](../images/create-mapped-entityT2.png)

9.  Click **Save**.

    **Result:** Your mapped entity saves. The entity appears on the **Associated entities** tab. Now the model can leverage machine learning and use the values provided to identify possible values.

    ![Entity window with a mapped entity with multiple values.](../images/create-mapped-entityT3.png)


## What to do next

You can create a mapped entity using a vocabulary source to use the values in the source as the mapped entity.

**Parent Topic:**[NLU entities](../concept/entities.md)

**Related topics**  


[Create a simple entity](create-nlu-entities.md)

[Create a pattern entity](create-pattern-entity.md)

[Create a system-derived entity](create-system-derived-entity.md)

[Create an open-ended entity](create-open-ended-entity.md)

[Import entities](import-common-entities-nlu.md)

[Using regular expressions in entities](../concept/using-regular-expressions-nlu.md)

[Create a table vocabulary source](create-table-lookup-source.md)

[Create a list vocabulary source](create-static-list-source.md)

