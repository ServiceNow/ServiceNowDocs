---
title: Configure Predictive Intelligence for User Reported Phishing
description: Configure and prepare the model to identify user reported phishing emails.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure Predictive Intelligence for User Reported Phishing

Configure and prepare the model to identify user reported phishing emails.

## Before you begin

Role required: ml\_admin

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence for Phishing** &gt; **Configuration**.

2.  In Step 1 of the configuration, select one of the following options from the Close code source list:

    -   Default close code: Select this option to specify the default security incident close codes that must be used by the training model to identify malicious emails and legitimate ones. Click the lock icon and select one or more False positive codes or Confirmed phishing codes.
    -   Custom close code: Select the Custom close code option if you want to define close codes from custom fields that may be used as part of your existing incident response procedures. To define a close code, select a field from the security incident table and specify one or more filter conditions.
    ![User Reported Phishing: ML Config: Close codes](../image/cj-sir-ml-urp-config5.png)

3.  In Step 2, import historical data that can be used to train the model.

    Select the Data Source for importing the historical data. This can be:

    -   User reported phishing email table: You can see the number of records that can be imported as historical data. Select this option and click **Import**.
    -   Custom data source: You can attach a single formatted CSV file that contains historical data records. Select the file and click **Import**.
    **Note:** The CSV file that you import must contain the following headers:

    -   Label
    -   Header
    -   Body text
    Each record must contain a Malicious or Legitimate tag in the Label column in the CSV file.

    Click **Cancel Import** to stop importing the data. The import process is canceled and all records that have been imported so far are deleted.

4.  After you have imported the historical data, click the link to refresh the page.

    You can then either import more training data or continue with the next step.

5.  In Step 3, verify if the number of records available for training meet the minimum threshold requirements.

    **Note:** The default values for maximum and minimum number of training records are displayed. These thresholds can be modified in the Platform Machine Learning Properties page. Contact Customer Support for assistance.

6.  If the training data is sufficient, click **Train model**.

    You can update the inputs for training in the screen below.

    ![User Reported Phishing: ML Config: Inputs](../image/cj-sir-ml-urp-config4.png)

7.  Prediction inputs that you can modify include:

    -   What are you interested in predicting?
    -   What input data is helpful to predict the output field?
    -   What historical data do you want to use to train the solution and how frequently do you want to retrain it?
    The default values for these inputs are displayed. You can modify them and click either of the following:

    -   **Update**: Updates the training model definition.
    -   **Update &amp; Retrain**: Updates the training model definition and retrains the model \(Triggers the **Train Model** function\).
8.  Finally, when you have completed training the model, click the **Activate Prediction** check box.

    Predictions are now provided on every user reported phishing record using that model. If you would like to stop providing predictions on the user reported phishing records, clear the **Activate Prediction** check box and click **Deactivate**.


