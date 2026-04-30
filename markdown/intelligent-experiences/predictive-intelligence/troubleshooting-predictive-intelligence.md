---
title: Configuration tips for Predictive Intelligence
description: If you encounter issues during your solution training and solution prediction, follow these suggested resolutions.
locale: en-US
release: yokohama
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configure Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Configuration tips for Predictive Intelligence

If you encounter issues during your solution training and solution prediction, follow these suggested resolutions.

## Input Data

It is recommended to have at least 30,000 records to train your models with, but the accuracy of the model is determined by the input data.

There are three primary factors that determine the quality of the input data used to train solutions:

-   Cleanliness: Sanitized data reduces noise, making the model more accurate.
-   Quality: The input and output should be valid and correct to train the model to make accurate predictions.
-   Distribution: Data that represents the entire dataset as a whole will result in a model that can make more generalized predictions.

Most raw data sets contain dirty and unusable data. Reviewing your input sets before training is essential to keeping accurate predictive models.

It is recommended to use approximately 80% of your input data to train your model and about 20% of the data to evaluate whether the model is accurate. You can compare the model's predicted results against the real values for the 20% of remaining data.

## Solution training

<table id="table_i2c_rtl_r2b"><thead><tr><th>

Issue

</th><th>

Resolution or suggested action

</th></tr></thead><tbody><tr><td>

The solution training remains in Waiting for Training status for too long, as the scheduler job is using an incorrect Glide callback instance URL.

</td><td>

Ensure the **glide.servlet.uri** property in the Glide instance is set to the correct instance URL. This issue can occur when: -   An instance is cloned from production, yet it still refers to the production URL for the **glide.servlet.uri** property.
-   The Glide instance is provisioned and runs the training for the first time.

</td></tr><tr><td>

New categories have been added and aren't yet having an impact on training.

</td><td>

This is expected behavior, as the new categories may not yet have sufficient data until the solution is retrained.

</td></tr><tr><td>

The solution training fails.

</td><td>

When the training fails, click the **Show Training Progress** related link on the solution screen to determine where the potential problem resides.

</td></tr><tr><td>

The solution training fails due to user authentication.

</td><td>

Navigate to **System Security&gt; Users** and ensure the sharedservice.worker user is set to Active.

</td></tr><tr><td>

The model training returns saying the model cannot be created. The training fails and shows the “Error while training solution” message. The training progress window shows this message: “Solution training failed as either the data used isn't sufficient or the input field isn't predictive of the output field."

</td><td>

This issue can occur when the data quantity or the distribution of field values isn't sufficient for a model to build successfully. Follow these steps to troubleshoot:1.  Ensure the distribution of the output field isn't skewed.
2.  Retrain the model by changing the date filters to use a larger amount of data.
3.  If the input fields are not fully populated, add a filter to remove null records.

</td></tr><tr><td>

The solution has data in multiple languages but the coverage and precision results are poor.

</td><td>

Use the following options to help improve your metrics.

 Option 1: Update the processing language of the solution to the most prominent non-English language.

**Note:** English is applied by default for all datasets.

 Option 2: If there's sufficient data for each language/region:

1.  Add a filter criteria for a specific language/region where the primary language can be identified \(Dutch, English, French, German, Japanese, or Spanish\).
2.  Generate a solution for each language/region and apply the proper processing language to each solution.

</td></tr></tbody>
</table>## Solution prediction

<table id="table_aj5_5tl_r2b"><thead><tr><th>

Issue

</th><th>

Resolution or suggested action

</th></tr></thead><tbody><tr><td>

The prediction fails and returns a Java exception where the cause is unknown.

</td><td>

1.  Search for the exception in the Predictive Intelligence Glide logs.
2.  Submit an Incident record for Predictive Intelligence including all relevant details, such as the exception, the impacted instance, the solution name, and the input string.

</td></tr><tr><td>

There is no prediction applied to the incident/case record but the prediction returns a value when tested in the Rest API Explorer.

</td><td>

This can occur when the confidence of the prediction is less than the threshold required to make a prediction. After your solution is trained, use the following steps to confirm if your solution settings need adjusting.1.  Navigate to **System Web Services &gt; REST &gt; REST API Explorer** to find the confidence level for the prediction. See [Test a classification solution prediction](../task/test-solution-prediction.md).
2.  On your ML Solution Definition record, check the threshold set for your outcome class that was returned in the prediction by clicking on the name of the class. The **Class** page appears.
3.  Check the **Estimated Precision** and **Estimated Coverage** values. If the corresponding threshold is more than the prediction confidence of the outcome, this is the root cause for why you did not see any prediction.
4.  Adjust the class precision and coverage values to increase coverage or precision. See [Tune a trained classification solution](../task/configure-class-precision-coverage.md).

</td></tr></tbody>
</table>## Instance cloning

|Issue|Resolution or suggested action|
|-----|------------------------------|
|After an instance is cloned, predictions for your existing solutions fail.|The ML solution artifacts in the \[ml\_artifacts\] table are stored in the \[sys\_attachment table\]. If the \[ml\_artifacts\] table isn't included in the clone when you run it, the predictions fail. Ensure your clone includes the machine-learning artifacts, as these are critical components of your Predictive Intelligence solution.|
|After an instance is cloned, the solution training fails.|As the cloning run proceeds, it is possible that the sharedservice.worker user has either been inactivated, locked out, or the user ID isn't set. Resolve these problems so that the solution training succeeds.|

