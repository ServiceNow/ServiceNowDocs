---
title: Create and train a regression solution
description: Train your solution by using historical data to predict numeric outputs, such as a temperature or a stock price. For example, you can use regression to estimate the time it takes to resolve an incident or a case.
locale: en-US
release: xanadu
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Creating and training solutions, Predictive Intelligence, Enable AI experiences]
---

# Create and train a regression solution

Train your solution by using historical data to predict numeric outputs, such as a temperature or a stock price. For example, you can use regression to estimate the time it takes to resolve an incident or a case.

## Before you begin

**Important:** Support for new regression solutions is deprecated in the Xanadu release. You will still be able to edit and train any existing solutions, but you won't be able to create new ones.

Role required: ml\_admin or admin

## About this task

Regression solutions enable you to predict a point estimate and prediction interval. The resulting model delivers the following statistics:

-   Mean Absolute Error \(MAE\), which measures the mean deviation of a predicted value from the actual value. This metric is useful as it's easy to understand as its scale is the same as that of its target. However, MAE is unbounded, making it difficult to compare across models.
-   Symmetric Mean Absolute Percentage Error \(SMAPE\) is a percentage value of the deviation from the predicted to the actual. SMAPE is a bounded version of MAE except that it has a value range between 0 and 100. The lower the SMAPE value, the better the model accuracy.
-   Range Accuracy is the percentage of actual values between a predicted range. In other words, it's the range between the upper and lower bounds of the prediction. For example, if four out of five actuals lie within the predicted range, the range accuracy is 80%.
-   Average Interval Width is the difference between the upper and lower bounds of the prediction. This metric explains how informative the interval is. The smaller the average width, the better the model

When making predictions, regression also enables you to specify a confidence level for the prediction interval \(range\).

In this example procedure, you create and train a regression solution definition to predict the amount of time it takes to restore a cloud database.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Regression** &gt; **Solution Definitions**.

2.  On the Regression Definitions list, click **New**.

3.  On the Regression Definition form, configure these fields per the following guidance.

<table id="table_kx3_qgr_qlb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Enter a unique name for your regression solution. For example, in this use case you could enter `Regression Test for DB Restore`.

</td></tr><tr><td>

Name

</td><td>

As you enter your solution Label value, this field automatically populates with a system-assigned name that's similar to your label value.

</td></tr><tr><td>

Word Corpus

</td><td>

Select an existing word corpus that's relevant to your solution. For example, in this use case you select a word corpus that has a title such as **Incidents in the last 3 months**.

 If you don’t have a relevant word corpus, follow the steps [to create a word corpus](create-word-corpus.md) first. When the word corpus is complete, you can select it from the Word Corpus field in your Regression Definition form.

 However, the word corpus selection is optional. If your input data has text columns and you don't choose a word corpus, your regression solution trains a new word corpus model by using the text columns in your input data. The resulting word corpus can be reused in any other regression solution or other ML solution type.

 **Note:** A pre-trained model is used instead of the Word Corpus for users who activated Predictive Intelligence starting in Utah.

</td></tr><tr><td>

Table

</td><td>

Select the database table on which you’re applying regression. The table should contain historical records the system can use to predict the length of time for its database restore.

</td></tr><tr><td>

Output Field

</td><td>

Select the field whose value you want the predictive model to set.

 In general, a good output field is a numeric, integer, or floating point field.

 In this example scenario, you use the **Duration** field to measure a length of time. The output field should generate a numeric value.

</td></tr><tr><td>

Fields

</td><td>

Select one or more field types that help the system identify the records you want to train using regression. In this example scenario, you use **Short description**, **Source datacenter**, **Target datacenter**, and **Database size**. \(short\_description, Sourcedc, Targetdc, and Dbsize.\) Input field types can be string, nominal, or numeric.

</td></tr><tr><td>

Filter

</td><td>

\(Optional\) Add filter conditions to the output field records that you want to train using regression.**Note:**

-   The minimum number of records for regression training is 10,000 records.
-   The maximum number of records for regression training is limited to 300,000.


</td></tr><tr><td>

Processing Language

</td><td>

Select the primary language of the dataset that you're training on the solution definition. If the dataset language is Italian, choose **Italian**. Also, English processing is applied to all datasets by default. For example, if you select Italian, the system processes the data in both English and Italian.**Note:** The term processing indicates some of the language-specific steps used as part of training a solution. These steps include tokenizing words, removing stop words, and stemming.

</td></tr><tr><td>

Stopwords

</td><td>

When you select your processing language, the system automatically adds a Stopwords list that uses the same language. For example, if your processing language is Italian, the **Default Italian Stopwords** list is displayed. The **Default English Stopwords** list also displays in your selection. If you create a custom stopwords list, you can select it from the Stopwords field to add it to your solution. In this scenario, you use the **Default English Stopwords** list.

</td></tr><tr><td>

Training Frequency

</td><td>

Select how often the system regenerates the solution based on records matching the **Filter**. Your options include:

-   Run Once
-   Every 30 days
-   Every 60 days
-   Every 90 days
-   Every 120 days
-   Every 180 days
 In this scenario, you select Every 30 days

 By default, the system runs training once. This practice provides you time to review and update the solution definition as needed until it provides acceptable coverage and precision values.

 **Note:**

-   The minimum number of records required for regression solution training is set at 10,000.
-   The ML scheduler limits the number of trainings an instance can commit to 50 new ML training requests per instance within a 24-hour window. This limit excludes scheduled requests for retraining. In addition, clustering and similarity updates are also excluded from this limit, even if the new training requests exceed 50 within a 24-hour window.


</td></tr></tbody>
</table>4.  Click the appropriate context menu option or button for your solution definition.

    |Option|Description|
    |------|-----------|
    |**Save or Save &amp; Train**|Save your solution definition record so you can return to it later, or save and submit it for training.|
    |**Submit or Submit &amp; Train**|Create your solution definition record and submit it, or submit and train it.|

5.  If you submitted the solution for training, click **OK** on the **Training Activation** window to confirm.

    The system schedules the solution for training with the nearest training service. The system sends you a notification when the training completes, including any errors that may have occurred in the training. Any other users can subscribe to the Predictive Intelligence Notifications category. When training completes, the system uploads the solution as an Attachment record.


## What to do next

In this example scenario, you created an ML solution from your solution definition. The Solution Statistics, Test Solution, and Solution Definition tabs appear in the Related Links section of your ML solution.

On the Solution Statistics tab, review the Point Estimate and Range \(prediction interval\) statistics generated by your solution.

![The prediction statistics for the solution you created and trained.](../images/create-regression-solution-stats.png)

On the Test Solutions tab of your solution, you can test the prediction output for the records you used as input to the prediction by entering values for the input fields, such as the **Source datacenter**, **Target datacenter**, and **Database size**. You can also use the default prediction confidence level of `95`, or enter a different level between `0` and `100`. Using 95 as the value means that the system is 95% confident that the actual prediction falls within the prediction interval. Click the **Run Test** button to find the prediction output.

![The values you need to enter in order to run a prediction output test.](../images/create-regression-solution-stats1.png)

After you run the test, the prediction output statistics appear. The Point Estimate on the screen is a single value at one point in time. For example, the database restore takes 134.47 seconds to complete. The Lower and Upper bounds on the screen signify a range accuracy value. For example, the database restore takes from 84.53 to 185.41 seconds to complete.

![The test output values for the Point Estimate and Range Accuracy predictions.](../images/create-regression-solution-stats2.png)

