---
title: Create a word corpus
description: Build a collection of words and phrases that functions as the vocabulary the system uses to compare your instance records based on their textual similarity. You can think of the word corpus as a dictionary that you want your machine-learning system to understand.
locale: en-US
release: zurich
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Create a word corpus

Build a collection of words and phrases that functions as the vocabulary the system uses to compare your instance records based on their textual similarity. You can think of the word corpus as a dictionary that you want your machine-learning system to understand.

## Before you begin

Role required: admin or ml\_admin

**Important:** In the Zurich release, models in the classification, clustering, and similarity frameworks use Workflow solutions. These are pre-trained, so a word corpus isn't needed for your new solutions.

After upgrading, your existing solutions with a word corpus become Workflow solutions the next time they are re-trained. Also the Word Corpus field is removed from the form.

The following information is provided for legacy context.

## About this task

The primary purpose for a word corpus is to infer textual data for training your NLU model. If using a word corpus in a solution, you must specify it for training in the solution definition phase of a solution. A trained word corpus can be reused across solutions and capabilities.

You can use a word corpus to help compare similar record text in a table or across multiple tables. A word corpus can also be helpful in other scenarios, such as clustering, where you group similar records together for data analysis, reuse, or review. The items you add to your corpus should be specific to your company and your industry so you can reuse it in other similarity or clustering solutions and apply it to various use cases.

In this example procedure, you're working on incident records and you want to locate relevant knowledge base \(KB\) articles that could provide resolutions to those incident cases. Your goal here is to create a word corpus that you can apply to a new similarity solution that compares active incidents to published KB articles.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Word Corpus**.

2.  In the Word Corpus form, click **New**.

3.  Configure these fields according to the following guidance.

    |Field|Description|
    |-----|-----------|
    |Name|A unique title that references the contents of your corpus. For example, in this use case you could enter a name such as `Active Incidents and Published KBs`, as the name indicates the tables that your corpus will mine to help create your solution.|
    |Active|Select this check box if you're creating more than one word corpus at a time and you plan to configure their detail components later. Otherwise, leave it blank because you can select it in a later step.|

4.  Select **Submit**.

5.  In the Word Corpus list view, locate your new word corpus and click its **Name** value to open the record.

6.  In the Word Corpus Contents section, Click **New**.

7.  In the Word Corpus Content form, configure these fields per the following guidance to define a content component for your word corpus.

<table id="table_zh4_52g_3hb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a title that references the data you want to add to your corpus, such as `Incidents closed in last 6 months`.

</td></tr><tr><td>

Table

</td><td>

Select the table that contains the data you want to include in your word corpus. For this use case, select **Incident \[incident\]**.**Note:** The number of records per table for Word Corpus creation used in Similarity and Clustering solutions is limited to 300,000.

</td></tr><tr><td>

Filter

</td><td>

Select the following filter condition values: **\[Closed\] \[is not empty\] and \[Created in last 6 Months\]**.

</td></tr><tr><td>

Field List

</td><td>

For this use case, select **Short description**, **Description**, and **Resolution notes**.

</td></tr><tr><td>

Domain

</td><td>

The system automatically displays the user group for your corpus. For example, in this use case it shows the global user group. You can select other user groups as well.

</td></tr></tbody>
</table>8.  Select **Submit**.

9.  In the Word Corpus Details section, select **New**.

10. Configure these fields according to the following guidance to define a second content component for your word corpus.

<table id="table_d4d_mfg_3hb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a title that references the data you want to compare to your first content component, such as `Published KB Articles`.

</td></tr><tr><td>

Table

</td><td>

Select the table that contains the data you want to compare to your first content component. For this use case, select **Knowledge \[kb\_knowledge\]**.**Note:** The number of records per table for word corpus creation used in Similarity and Clustering solutions is limited to 300,000 records per table.

</td></tr><tr><td>

Filter

</td><td>

Select the following Filter Condition values: **\[Workflow\] \[is\] \[Published\]**.

</td></tr><tr><td>

Field List

</td><td>

Select **Short description** and **Article body**.

</td></tr></tbody>
</table>11. Select **Submit**.

    Your two word corpus content components appear on the word corpus form.

    ![This image shows the two content components you've created for your word corpus.](../images/predict-intel-wordcorpus-click-update.png)

12. Select **Update**.


## Result

The completed word corpus you created appears on the word corpus form and is available for use in your similarity and clustering solution definition forms.

![When you click Update, the system validates the addition of the components to complete the corpus creation process.](../images/predict-intel-wordcorpus-result.png)

## What to do next

Create a solution in the appropriate framework. For more information, see the links in the Related Content panel on this page.

**Related topics**  


[Create and train a classification solution](create-solution-definition.md)

[Create and train a similarity solution](create-similarity-solution.md)

[Create and train a clustering solution](create-clustering-solution.md)

