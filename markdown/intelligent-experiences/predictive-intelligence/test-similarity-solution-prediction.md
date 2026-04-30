---
title: Test a similarity solution prediction
description: Once your machine-learning \(ML\) solutions are trained, you can call on the Predictive Intelligence API to make a solution prediction. In this example procedure, we use the REST API Explorer application to test a similarity solution prediction for resolved incident recommendations.
locale: en-US
release: yokohama
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Testing and monitoring predictions, Predictive Intelligence, Enable AI experiences]
---

# Test a similarity solution prediction

Once your machine-learning \(ML\) solutions are trained, you can call on the Predictive Intelligence API to make a solution prediction. In this example procedure, we use the REST API Explorer application to test a similarity solution prediction for resolved incident recommendations.

## Before you begin

Train your ML solution prior to testing a prediction.

Role required: web\_service\_admin, rest\_api\_explorer, or admin or ml\_admin

## About this task

This procedure uses sample data to illustrate what you can do in your instance, and may not represent data or records that are actually in your instance.

This scenario illustrates a similarity solution prediction for a hypothetical ML solution that you have previously created and trained. You can also use the REST API Explorer to test a classification solution prediction.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Similarity** &gt; **Solution Definitions**.

2.  Locate the ML solution definition whose prediction you want to test, and copy its **Name** value to your clipboard or a Notepad file.

    In this case, we use the **Name** field value in your ML Solution Definition Recommended Resolved Incidents record, as illustrated in the following example.

    ![Show the user where to find the ML solution definition name](../images/predict-intel-similarity-soldef-name.png)

3.  Copy the **Input Fields** value\(s\) used in your ML Solution Definition record that you want the REST API Explorer to use in its call to the Predictive Intelligence API.

    In this case, we use the **Short description** field type, as the prediction model has been trained to use this field to learn, pair, and recommend similar records for your review.

    ![Show the user where to find the Input Field types.](../images/predict-intel-similarity-soldef-inputfields.png)

4.  Right-click the browser tab you're using to view your instance, and select **Duplicate**.

5.  In the duplicate browser tab, navigate to **System Web Services** &gt; **REST** &gt; **REST API Explorer**.

6.  Click **Explore**.

7.  Set these choice fields as follows.

    |Field|Value|
    |-----|-----|
    |**Namespace**|now \(leave as default\)|
    |**API Name**|Predictive Intelligence|
    |**API Version**|latest \(leave as default\)|

    The Predictive Intelligence form appears. You use this form to prepare your call request to the Predictive Intelligence API.

8.  In the solution-name **Value** field, enter `ml_x_snc_global_recommended_resolved_incidents`.

    **Note:** This is the Name value you captured in Step 2 of this procedure.

9.  Click **Add query parameter**.

10. In the Query parameters section, enter the value of one of the Input Fields from the solution you're testing.

    1.  In the first field, paste `short_description`.

        **Note:** This is one of the input fields you captured in Step 2 of this procedure.

        You can use other field types, such as **Description** or **Resolution notes** to test what the solution is predicting.

    2.  In the second field, enter some text that you might find in an incident record.

        For instance, enter `Discovery errors`.

11. Click the \[+\] button to create a second query condition that defines the number of results you want to query.

    1.  In the first field, enter `top_n`.

    2.  In the second field, enter `3`.

    These conditions set the query to retrieve the top three most similar incident records.

12. Click **Send**.

    The REST API Explorer sends your request to the Predictive Intelligence API.

13. In the Response body section, copy the three outcome values that your API call returned, as illustrated in the image below.

    ![Shows the user the top 3 REST API Explorer response body outcomes.](../images/predict-intel-simtest-soldef-outcomes.png)

14. In your original browser tab, navigate to **Servicedesk** &gt; **Incidents**.

15. As shown in the image below, set filter conditions for the three REST API outcomes to the Incidents table list view.

    1.  Add the Active and Sys ID conditions below to the Incidents list view Filter icon.

    2.  Paste the three REST API outcomes into the **Input value** field of the Sys ID condition that you created.

    3.  Click **Run**.

    ![Shows the user the filter conditions to set on the Incident list view and where to paste the REST API outcomes.](../images/predict-intel-simtest-soldef-outcomeconditions.png)

16. Per the image below, compare the returned list of incidents with the input for the prediction output in the REST API Explorer.

    1.  Click the Incident Number to open the Incident record.

        ![Shows the user the 3 Incident records that share the text from the input field.](../images/predict-intel-simtest-soldef-top3incidents.png)

    2.  Per the image below, review the Resolution notes text in the Incident record.

        ![Shows the user the Resolution notes in one of the Incident records.](../images/predict-intel-simtest-soldef-recommendation.png)


**Related topics**  


[Predictive Intelligence API](https://www.servicenow.com/docs/access?context=agent-intelligence-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

[MLPredictor - Global](https://www.servicenow.com/docs/access?context=c_MLPredictorAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

