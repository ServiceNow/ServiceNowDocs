---
title: Create and train a similarity solution
description: Create and train a machine learning solution to collect and compare your existing records to new similar records. For example, you can compare the text in an open Incident record to a resolved Incident record to reuse its resolution.
locale: en-US
release: australia
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Creating and training solutions, Predictive Intelligence, Enable AI experiences]
---

# Create and train a similarity solution

Create and train a machine learning solution to collect and compare your existing records to new similar records. For example, you can compare the text in an open Incident record to a resolved Incident record to reuse its resolution.

## Before you begin

-   Role required: ml\_admin or admin

**Important:** From the Washington DC release, models in the classification, clustering, and similarity frameworks use Workflow solutions. These are pre-trained, so a word corpus isn't needed for your new solutions. When your existing solutions with a word corpus are re-trained after upgrading, they become Workflow solutions, and the Word Corpus field is removed from the form.

## About this task

After comparing your existing records based on similarity, the system recommends examples that you can review and reuse in your solution.

When applied in your forms and flows, similarity solutions are domain-aware, so records from other domains on the instance are not displayed to users. For more information, see KB article [Similarity prediction behavior in domain separated environment](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2035643) on Now Support.

For information on using encrypted training data, see [Data Encryption in Predictive Intelligence](../reference/predictive-intelligence-encryption.md).

In this example procedure, you're working on Incident records and you want to locate relevant Knowledge Base articles that could provide resolutions to those incidents.

![Form view of a new Predictive Intelligence similarity solution definition](../images/predictiveintel_similaritysolution_newW.png)

## Procedure

1.  Ensure that you are in the application scope that you want for your solution definition, then navigate to **All** &gt; **Predictive Intelligence** &gt; **Similarity** &gt; **Solution Definitions**.

2.  In the Similarity Definitions list, select **New**.

3.  On the Similarity Definition form, fill in the fields.

<table id="table_o1g_bfj_3fb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Enter a unique name for your similarity solution. For example, in this use case you could enter `Match Knowledge Articles to Incidents`.

</td></tr><tr><td>

Name

</td><td>

As you enter a Label value, this field automatically populates with a system-assigned, read-only name based on your Label value.

</td></tr><tr><td>

Word Corpus

</td><td>

If you have a legacy similarity solution, you can select a relevant word corpus from the **Word Corpus** field in the definition form.

 **Note:** Starting from the Washington DC release, a word corpus is not required because a pre-trained model is used instead. The **Word Corpus** field is not visible in the definition form for pre-trained models.

 For more information, see [Create a word corpus](create-word-corpus.md).

</td></tr><tr><td>

Table

</td><td>

In the Table field, select the table that contains records you want to use as an information source. In this use case you select the **Knowledge \[kb\_knowledge\]** table, because its KB Article records might provide information relevant to the Incidents that you're trying to resolve.

 After you assign a Table, the number of records matching your filter conditions is displayed as a link. Select this link to view the list of records.

</td></tr><tr><td>

Test Table

</td><td>

In the Test Table field, select the table containing the records that you want to target. In this use case, you select the **Incident \[incident\]** table, as it contains the Incident records that you're trying to resolve.

**Note:** You can select the same table for Table and Test Table. For example: using filter conditions, you could collect information from recent Incidents to help with target Incidents.

</td></tr><tr><td>

Fields

</td><td>

For the Table that you selected, enter fields that are likely to contain words and phrases relevant to the Incidents you're trying to resolve. In this example, you choose **Short description** and **Article body**. Including the article body increases your chances of capturing informative details regarding the subject.

**Note:** **Journal Type** is not a supported data type.

</td></tr><tr><td>

Test Fields

</td><td>

For the Test Table that you selected, enter fields that contain text that you want to compare to other similar records. In this example, you choose the **Short description** of the Incident records you're trying to resolve.

</td></tr><tr><td>

Filter

</td><td>

Select **Add Filter Condition** to apply conditions to the Fields records you're using as an information source. For example, in this use case you could set a **workflow\_state=published** condition to retrieve published KB articles only.

**Note:** Script includes can't be referenced from the Filter. Use database views as an alternative.

</td></tr><tr><td>

Processing Language

</td><td>

Select the dominant language of the dataset you're training on. Also, English processing is applied to all datasets by default. For example, if you select Italian, the system processes the data in both Italian and English.**Note:** The term processing indicates some of the language-specific steps used as part of training a solution, such as tokenizing words, removing stop words, and stemming.

</td></tr><tr><td>

Stopwords

</td><td>

When you select your processing language, the system automatically adds a Stopwords list for that language. For example, if your processing language is Italian, the **Default Italian Stopwords** list appears. The **Default English Stopwords** list is also included.To use a custom stopwords list, select the lock icon\(![Lock icon.](../../../common/image/icon-lock.png) \) and then search in the **Select target record** field.

</td></tr><tr><td>

Training Frequency

</td><td>

Select a retraining frequency. The available options range from **Run Once** up to **Every 180 days**.

</td></tr><tr><td>

Update Frequency

</td><td>

Select how often you want to refresh the data you use to retrieve your similarity results. For example, for open incident records, you could select an update frequency of **Every 15 minutes**, as new incidents typically occur frequently throughout the day. This frequency may increase the likelihood that newly opened records are included in the refresh.

However, for KB Knowledge article records, which are typically not created often, you could choose a less frequent update frequency such as **Every 1 day**.

**Note:** The ML scheduler limits the number of trainings an instance can commit to 50 new ML training requests per instance within a 24 hour window. This excludes scheduled re-training requests. In addition, clustering and similarity updates are also excluded from this limit, even if the new training requests exceed 50 within a 24 hour window.

</td></tr></tbody>
</table>4.  Select the appropriate button for the solution definition.

    |Option|Description|
    |------|-----------|
    |**Save**|Save your solution definition record so you can return to it later.|
    |**Submit &amp; Train**|Create your solution definition record and train it.|

5.  If you submitted the solution for training, select **OK** on the **Training Activation** window to confirm.


## Result

-   The system schedules the solution definition for processing with the nearest training service and sends you a notification when the training completes. The notification includes any errors that may have occurred during the training. Other users can subscribe to the Predictive Intelligence Notifications category.
-   The trained solution delivers paired example records ranked by their degree of similarity. The list of examples is available from **Similarity Examples** under Related Links on your solution's form.
-   When training completes, the system uploads the solution as an Attachment record.

## What to do next

Review the similarity examples on the Related Links section of your Solution form. See [Review solution similarity examples](review-similarity-examples.md).

