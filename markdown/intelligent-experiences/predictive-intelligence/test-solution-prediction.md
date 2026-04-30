---
title: Test a classification solution prediction
description: Once your machine-learning \(ML\) solutions are trained, you can call on the Predictive Intelligence API to make a solution prediction. In this example procedure, we use the REST API Explorer to test a classification solution prediction for incident categorization.
locale: en-US
release: xanadu
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Testing and monitoring predictions, Using Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Test a classification solution prediction

Once your machine-learning \(ML\) solutions are trained, you can call on the Predictive Intelligence API to make a solution prediction. In this example procedure, we use the REST API Explorer to test a classification solution prediction for incident categorization.

## Before you begin

Train your ML solution prior to testing a prediction.

Role required: web\_service\_admin, rest\_api\_explorer, or admin or ml\_admin

## About this task

This procedure uses sample data to illustrate what you can do in your instance, and may not represent data or records that are actually in your instance.

This scenario illustrates a classification solution prediction for a hypothetical ML solution that you have previously created and trained. You can also use the REST API Explorer to test a similarity solution prediction.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Classification** &gt; **Solution Definitions**.

2.  Locate the ML solution definition whose prediction you want to test, and copy its **Name** value to your clipboard or a Notepad file.

    In this case, use the **Name** field value in your ML Solution Definition Incident Categorization record, as illustrated in the following example.

    ![This image hows you where to find the Name field value in your ML Solution Definition Incident Categorization record.](../images/predictive-intelligence-solution-name.png)

3.  Write down and save the **Input Fields** used in your ML Solution Definition record that you want the REST API Explorer to use in its call to the Predictive Intelligence API.

    In this case, we use the **short \_description** field, as the prediction model has been trained to use this field to learn its category definition.

    ![Where to find the Input Fields that you want the REST API Explorer to use in its call to the Predictive Intelligence API](../images/predictive-intelligence-solution-description.png)

4.  Navigate to **System Web Services** &gt; **REST** &gt; **REST API Explorer**.

5.  Set these choice fields as follows.

    |Field|Value|
    |-----|-----|
    |**Namespace**|now \(leave as default\)|
    |**API Name**|Predictive Intelligence|
    |**API Version**|latest \(leave as default\)|

    The Predictive Intelligence form appears. You use this form to prepare your call request to the Predictive Intelligence API.

6.  In the solution-name **Value** field, type `ml_incident_categorization`.

    **Note:** This is the Name value you captured in Step 1 of this procedure.

7.  Click **Add query parameter**.

    The Predictive Intelligence form refreshes to show the **Query parameters** section.

8.  Type `short_description` in the first field.

    **Note:** This is the input field you captured in Step 2 of this procedure.

9.  Type a short description of an incident in the second field, for example, `Unable to connect`.

10. Click the **Send** button.

    The REST API Explorer sends your request to the Predictive Intelligence API.

    The system predicts the output value in the Response Body section of the API output. You can use other short descriptions to test what the solution is predicting.

11. Send a different request to the Predictive Intelligence API so that you can test the prediction model again.

    1.  Return to the **Query parameters** section of the Predictive Intelligence form.

    2.  Type a short description that references a different kind of incident in the second field, for example, `Unable to connect to MSSQL`.

    3.  Click the **Send** button.

    The Response Body section may refresh to show a different outcome than what you saw in Step 9, depending on which incident categories you configured in your solution definition setup. In other words, changing the short description text can recategorize the incident as a different kind of issue.


## Example

You can also test the Predictive Intelligence prediction model when you create a new incident record using the incident form.

1.  Navigate to **Incident** &gt; **Create New**.
2.  In the new Incident form that loads, set the fields as follows.
    -   **User:** Enter the Caller name.
    -   **Category:** Leave as default.
    -   **Short description:** Enter a short description that you want to test.
3.  Submit the incident form.

Result: When the form refreshes, an information message appears with the incident category automatically set to a specific value.

**Note:** For some short descriptions, the prediction might not process because the solution does not have enough confidence in predicting the value for this input.

**Related topics**  


[Predictive Intelligence API](https://www.servicenow.com/docs/access?context=agent-intelligence-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

[MLPredictor - Global](https://www.servicenow.com/docs/access?context=c_MLPredictorAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

