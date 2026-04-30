---
title: HR PIWB template: Recommend estimated time to resolve
description: Train your solution by using historical data to predict numeric outputs based on the historic data. Configure the solution definition to predict the estimated time to resolve a HR case.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [HR Predictive Intelligence Workbench implementation, HR Predictive Intelligence Workbench, Integration of HR Service Delivery with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# HR PIWB template: Recommend estimated time to resolve

Train your solution by using historical data to predict numeric outputs based on the historic data. Configure the solution definition to predict the estimated time to resolve a HR case.

## Before you begin

Role required: sn\_piwb\_hr\_content.admin

## About this task

Regression solutions enable you to predict a point estimate and prediction interval. When making predictions, regression also enables you to specify a confidence level for the prediction interval \(range\). Understand the ETTR configuration information from [Estimated time to resolve HR cases](../concept/train-model-ettr.md).

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence Workbench** &gt; **Use Cases** &gt; **Create New from Templates**.

2.  From the templates list, go to **Estimated Time to Resolve an HR case** and click **Start**.

    A pop-up with model name appears. This use case is handled in the classic Predictive Intelligence. You will be taken there to complete setup. You can perform the following steps:

    1.  Ensure you click **View product documentation for setting up this use case** to review the instructions on how to configure the solution definition.

        **Note:** Ensure you review and understand the documentation for creating the solution definition.

    2.  Click **Take me there** to get started with the solution definition.
    Machine Learning Solutions landing page appears.

    ![List of ML usecases for HR PIWB](../image/piwb-hr-ml-list.png "HR ML usecases")

3.  Go to **Regression** &gt; **ml\_sn\_sn\_hr\_core\_global\_hr\_case\_resolution\_time** from the available Solution Definitions, click **Configure**.

    Regression solution definition for HR case resolution time appears.

4.  On the solution definition form, configure these fields per the following guidance.

<table id="table_kx3_qgr_qlb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Enter a unique name for your regression solution. For example, enter `HR Case Resolution Time`.

</td></tr><tr><td>

Name

</td><td>

As you enter your solution Label value, this field automatically populates with a system-assigned name that's similar to your label value `ml_sn_sn_hr_core_global_hr_case_resolution_time`

</td></tr><tr><td>

Word Corpus

</td><td>

Select an existing word corpus that's relevant to your solution. For example, in this use case you select a word corpus that has a title such as **Word Corpus Regression**.

 If you don’t have a relevant word corpus, follow the steps in Create a word corpus. When the word corpus is complete, you can select it from the Word Corpus field in your Regression Definition form.

 However, the word corpus selection is optional. If your input data has text columns and you don't choose a word corpus, your regression solution trains a new word corpus model by using the text columns in your input data. The resulting word corpus can be reused in any other regression solution or other ML solution type.

 **Note:** The number of records per table for word corpus creation used in regression solutions is limited to 300,000.

</td></tr><tr><td>

Table

</td><td>

Select the database table on which you’re applying regression. The table should contain historical records the system can use to predict the length of time for its database restore `HR Case [sn_hr_core_case]`.

</td></tr><tr><td>

Output Field

</td><td>

Select the field whose value you want the predictive model to set. In general, a good output field is a numeric, integer, or floating point field.

 In this example scenario, you use the **actual\_resolution\_time** field to measure a length of time. The output field should generate a numeric value.

</td></tr><tr><td>

Fields

</td><td>

Select one or more field types that help the system identify the records you want to train using regression. In this scenario, you use **short\_description, description, hr\_service,assignment\_group, topic\_detail, topic\_category, priority,sys\_class\_name**. Input field types can be string, nominal, or numeric.

</td></tr><tr><td>

Filter

</td><td>

\(Optional\) Add filter conditions to the output field records you want to train using regression. Ensure you have sufficient records by adjusting the filters.The minimum number of records for regression training is 10,000 records.

 The maximum number of records for regression training is limited to 300,000.

</td></tr><tr><td>

Processing Language

</td><td>

Select the dominant language of the dataset you're training on the solution definition. If the dataset language is English, choose **English**. Also, English processing is applied to all datasets by default. For example, if you select Italian, the system processes the data in both English and Italian.**Note:** The term processing indicates some of the language-specific steps used as part of training a solution. For example, tokenizing words, removing stop words, and stemming.

</td></tr><tr><td>

Stopwords

</td><td>

When you select your processing language, the system automatically adds a Stopwords list that uses the same language. For example, if your processing language is Italian, the **Default Italian Stopwords** list appears. The **Default English Stopwords** list also appears in your selection as well. If you create a custom stopwords list, you can select it from the Stopwords field to add it to your solution. In this scenario, you use the **Default English Stopwords** list.

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

 The minimum number of records required for regression solution training is at 10,000.

 The ML scheduler limits the number of trainings an instance can commit to 50 new ML training requests per instance within a 24 hour window. This excludes scheduled re-training requests. In addition, clustering and similarity updates are also excluded from this limit, even if the new training requests exceed 50 within a 24 hour window.

</td></tr></tbody>
</table>5.  Click the appropriate context menu option or button for your solution definition.

    |Option|Description|
    |------|-----------|
    |**Save or Save &amp; Train**|Save your solution definition record so you can return to it later, or save and submit it for training.|
    |**Submit or Submit &amp; Train**|Create your solution definition record and submit it, or submit and train it.|

6.  If you submitted the solution for training, click **OK** on the **Training Activation** window to confirm.

    The system schedules the solution for training with the nearest training service. The system sends you a notification when the training completes, including any errors that may have occurred in the training. Any other users can subscribe to the Predictive Intelligence Notifications category. When training completes, the system uploads the solution as an Attachment record.

    When the configuration is complete, the employees and agents see the estimated time to resolve at the request sections.


## What to do next

In this scenario, you created an ML solution from your solution definition. In the Related Links section of your ML solution, see the Solution Statistics, Test Solution, and Solution Definition tabs. On the Solution Statistics tab, review the Point Estimate and Range \(prediction interval\) statistics your solution has provided.

![Regression solution definition statistics for HR case](../image/hr-regression.png "Regression solution definition")

On the Test Solutions tab of your solution, you can test the prediction output for the records you used as input to the prediction by entering values for the input fields. You can also use the default prediction confidence level of `95`, or enter a different level between `0` and `100`. Using 95 as the value means that the system is 95% confident that the actual prediction falls within the prediction interval. Click the **Run Test** button to find the prediction output.

After you run the test, the prediction output statistics appear. The Point Estimate on the screen is a single value at one point in time. When the configuration is complete, the employees and agents see the estimated time to resolve at the request sections.

You can verify the integration status from **HR Administration** &gt; **HR AI Configurations** &gt; **Solution definition**. The use case is now mapped to the selected solution definition.

-   **[Estimated time to resolve HR cases](../concept/train-model-ettr.md)**  
Determine the Estimated Time to Resolve a Case \(ETTR\) for a case by analyzing similar closed cases in the past for better visibility and transparency.
-   **[Viewing ETTR predictions](../concept/create-regression-solution-hr.md)**  
View the examples of ETTR views across the journey of a case which indicates the estimated time to resolve based on the historical data.

**Parent Topic:**[HR Predictive Intelligence Workbench implementation](../concept/hr-piwb-implementation-guidance.md)

**Related topics**  


[Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

[Get started with Predictive Intelligence](https://www.servicenow.com/docs/access?context=install-predictive-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&section=get-started-predictive-intelligence&ft:locale=en-US)

