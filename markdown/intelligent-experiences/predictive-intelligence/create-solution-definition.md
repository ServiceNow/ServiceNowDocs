---
title: Create and train a classification solution
description: Specify the records used to train a classification solution, what fields trigger a prediction, and how often you want to retrain your solution.
locale: en-US
release: australia
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Creating and training solutions, Predictive Intelligence, Enable AI experiences]
---

# Create and train a classification solution

Specify the records used to train a classification solution, what fields trigger a prediction, and how often you want to retrain your solution.

## Before you begin

-   [Create a custom stopwords list](create-custom-stopwords-list.md) if needed.
-   Role required: admin or ml\_admin

**Important:** In the Australia release, models in the classification, clustering, and similarity frameworks use Workflow solutions. These are pre-trained, so a word corpus isn't needed for your new solutions. When your existing solutions with a word corpus are re-trained after upgrading, they become Workflow solutions, and the Word Corpus field is removed from the form.

## About this task

A predictive model is only as good as the data that you use to train it. To select appropriate records for training, examine the table's database dictionary as well as the current quality of the record values that you want to use.

For information on using encrypted training data, see [Data Encryption in Predictive Intelligence](../reference/predictive-intelligence-encryption.md).

For information about the minimum and maximum number of records you can use for training, see [Predictive Intelligence properties](../reference/predictive-intelligence-properties.md).

**Note:** Classes that have fewer than 30 records in your training dataset are excluded from solution training. When your solution is trained and complete, any excluded classes are listed in the Solution Statistics section of your ML Solution form.

![Any classes that were excluded from your solution training are listed in the Solution Statistics section of your trained solution's ML Solution form.](../images/excluded-classes-ml-solution-form.png)

You must create a separate solution definition for each predictive model you want to support. The following procedure explains how to create a new classification solution, but you can also copy an existing solution definition and its configuration into a new record by selecting **Copy Solution Definition** from the context menu. Edit the field values on the new record as needed.

From the Yokohama release, you can also create a Workflow Classification solution using a script if you want to include an analysis of the key features influencing the model's predictions. For more information see [Model Explainability](predictive-intel-explainability.md).

## Procedure

1.  Ensure that you are in the application scope you want for your solution definition, then navigate to **All** &gt; **Predictive Intelligence** &gt; **Classification** &gt; **Solution Definitions**.

2.  On the Classification Definitions list, select **New**.

3.  On the empty Classification Definition form, configure the fields according to the following guidance.

<table id="table_zcc_rq4_j1b"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Enter a unique name for the solution record.

</td></tr><tr><td>

Name

</td><td>

The system generates the value of this read-only field based on the Label value that you entered.

</td></tr><tr><td>

Word Corpus

</td><td>

Select a word corpus that's relevant to your solution. For more information, see [Create a word corpus](create-word-corpus.md).

 **Note:** Word Corpus is not a required field for customers implementing Predictive Intelligence for the first time starting in Utah. A pre-trained model is used instead. The Word Corpus field is removed for pre-trained models.

</td></tr><tr><td>

Table

</td><td>

Select the table containing the target records that you want the system to predict.

</td></tr><tr><td>

Output Field

</td><td>

Select the field whose value you want the predictive model to set.

 In general, a good output field has these characteristics.

-   It's a choice field or a string field with a finite set of possible values.
-   It has some causal connection to the input fields.
 For example, on the default **Incident Categorization** solution definition, the output field is set to **Category**.

</td></tr><tr><td>

Fields

</td><td>

Select the input fields that you want the solution to use to generate a prediction.

 Input fields are fields within a record that may contain the classification information your prediction solution needs to succeed. For example, if you're predicting the correct class for triaging an incident record, the prediction should gather records containing text that references the class. Most records have contextual text in their **Short description** field, so it's a great input field to use in general. You could also use **Resolution notes** as an input field, as it too might reference the incident class in the detailed notes for the incident.

 In general, good input fields have these characteristics.

-   The fields are available to users when creating records.
-   The field data type can be string, reference, choice, or HTML. The more information that a field provides, the more often a solution can make a prediction, and the more often predictions are accurate.
-   The field has a default value and should not be blank.
 All default solution definitions use the **Short description** field.

</td></tr><tr><td>

Filter

</td><td>

Click **Add Filter Condition** to apply conditions to the records you're training.

 For example, the **Incident Categorization** solution definition uses a filter with these conditions: **\[Created\]\[on\]\[Last 12 months\] AND \[Active\]\[is\]\[false\] AND \[State\]\[is one of\]\[Resolved \| Closed\]**

 To train a solution, the filter must return at least one record. If your filter returns no records, update it until it returns records for training.

**Note:** The recommended number of records for training a good solution is from 30,000 through 300,000. If you submit more than 300,000 records, the most recent 300,000 records are used to train the solution. Use only authentic records from the database.

 In general, a good filter has these characteristics.

-   The training records are inactive and their states indicate work completed within your standard process, such as resolved or closed.
-   The target fields contain only correct values. Filter out records with unreliable target field values. For example, if you're predicting the assignment group/category and your historic incident data contains assignment groups/categories that are no longer used, add a filter to remove such records from the training.
-   The training records contain multiple examples of each target field value you want the solution to predict.
-   The training records include common variations of the input fields.
 Use relative date filters such as last 3 months or last 12 months. Don't use hard-coded dates because these filters aren't updated when the solutions are retrained, unless you update them manually.

</td></tr><tr><td>

Processing Language

</td><td>

Select the dominant language of the dataset that you're training on the solution definition. If the dataset language is Italian, choose `Italian`. Also, English processing is applied to all datasets by default. For example, if you select Italian, the system processes the data in both English and Italian.**Note:** The term processing indicates some of the language-specific steps used as part of training a solution. For example, tokenizing words, removing stop words, and stemming.

</td></tr><tr><td>

Stopwords

</td><td>

When you select your processing language, the system automatically adds a Stopwords list for that language. For example, if your processing language is Italian, the **Default Italian Stopwords** list appears. The **Default English Stopwords** list is also included. If you create a custom stopwords list, you can select it from the Stopwords field to add to your solution.

</td></tr><tr><td>

Training Frequency

</td><td>

Select how often the system regenerates the solution. The available options range from **Run once** up to **Every 180 days**.

**Note:** The minimum number of records required for classification solution training is set at 10,000.

 By default, the system runs training once. This provides you time to review and update the solution definition until it provides acceptable coverage and precision values.

 When your solution definition is fairly stable, consider scheduled trainings, as data can age over time, thus degrading the accuracy of your prediction model.

 **Note:** The ML scheduler limits the number of trainings an instance can commit to 50 new ML training requests per instance within a 24-hour window. This limit excludes scheduled retraining requests, clustering updates, and similarity updates, even if the new training requests exceed 50 within a 24-hour window.

</td></tr></tbody>
</table>4.  Click the appropriate context menu option or button for your solution definition.

    |Option|Description|
    |------|-----------|
    |**Save or Save &amp; Train**|Save your solution definition record so you can return to it later, or save and submit it for training.|
    |**Submit or Submit &amp; Train**|Create your solution definition record and submit it, or submit and train it.|

5.  If you submitted the solution for training, click **OK** on the **Training Activation** window to confirm.

    -   The system schedules the solution for training with the nearest training service. The system sends you a notification when the training completes, including any errors that may have occurred in the training. Other users can subscribe to the Predictive Intelligence Notifications category. When training completes, the system uploads the solution as an Attachment record.
    -   A bubble chart populates the Solution Visualization tab of your solution form, showing the estimated precision and coverage for each of the classes covered by the solution. The size of the bubble indicates the percent of records \(distribution\) that belong to the class. When you point to a bubble, you can see its estimated coverage, estimated precision, and distribution.
    ![The estimated precision and coverage for each of the classes covered by the solution.](../images/predict-intel-classification-bubblechart.png)


## What to do next

In the Class Confidence section of the Solution Statistics tab in your solution, review the trained solution precision and coverage statistics.

In the Test Solutions tab in your solution, you can test the prediction output by entering values from the input fields, such as the Short Description.

![How to test the prediction output for the records you used as input to the prediction by entering values from the input fields, such as the Short Description](../images/predict-intel-classification-testsolution-tab.png)

