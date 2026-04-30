---
title: View Task Intelligence prediction history
description: View details about historical predictions in the Predictor Result \[ml\_predictor\_results\] table.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use Task Intelligence, Automate and optimize, Use, Customer Service Management]
---

# View Task Intelligence prediction history

View details about historical predictions in the Predictor Result \[ml\_predictor\_results\] table.

The Predictor Result table includes entries for each prediction result, including the predicted language, predicted and actual values, and prediction confidence. You can use the data in this table to monitor model performance.

**Note:** Records are created in the Predictor Result table regardless of the model prediction behavior, including the Testing behavior that doesn’t add prediction values to the case.

## Viewing prediction data

Navigate to **All** &gt; **Task Intelligence for Customer Service** &gt; **History** to view the Predictor Result list.

Users with the following roles can access the **History** module:

-   Task Intelligence admin \[sn\_csm\_ml\_task.ti\_admin\]
-   Customer Service manager \[sn\_customerservice\_manager\]

Categorization feedback captures values when the status of a case changes to Closed. It captures these values if:

-   Case categorization is active.
-   The predicted field value is different from the case field value.

Categorization feedback works for record categorization solutions and for solutions with and without attachments. Email categorization solutions are trained using data from the Email \[sys\_email\] table. Case categorization solutions are trained using data from the Case \[sn\_customerservice\_case\] table or from tables that extend the Case table. Interaction categorization solutions are trained using data from the Interaction \[interaction\] table.

Categorization feedback is triggered by a flow.

-   When email information is used for prediction, the final input values remain empty.
-   When attachment information is used for prediction, the attachment sys\_ids are not included in the final input values.

Categorization feedback stores the following values in the Predictor Result table:

-   Predicted Output Value Name
-   Predicted Input Value Names
-   Predicted Output Value
-   Predicted Input Values
-   Final Input Value
-   Final Output Value
-   Predicted Confidence \(percentage\)

If the values for a case have been predicted using an email categorization solution:

-   The Final Input Value remains empty because it is not expected that the agent will modify the values of the email, such as subject and body.
-   The final value in the Predicted Output Value is stored in the Final Output Value once the case is closed.

If the values for a case or interaction have been predicted using a record categorization solution:

-   The values from the fields defined in Predicted Input Value Names are stored in Final Input Value.
-   The final value in the Predicted Output Value is stored in the Final Output Value once the case is closed.

## Email sentiment replies

Duplicate entries can be posted in the Predictor Result table for email sentiment replies. To help prevent these duplicate entries, deactivate the **Predict Sentiment for Cases** inbound email action. For more information, see [Inbound email actions](https://www.servicenow.com/docs/access?context=c_InboundEmailActions&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

