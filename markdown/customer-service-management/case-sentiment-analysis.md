---
title: Sentiment Analysis
description: Sentiment Analysis can help you gauge customer emotions, enabling you to provide more empathetic and compassionate customer experiences.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Task Intelligence for Customer Service, Machine learning solutions for Customer Service Management, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Sentiment Analysis

Sentiment Analysis can help you gauge customer emotions, enabling you to provide more empathetic and compassionate customer experiences.

Use the sentiment analysis feature included with Task Intelligence for Customer Service to:

-   Evaluate email and case text.
-   Identify the current sentiment of new cases.
-   Identify the ongoing sentiment of updated cases.
-   Display this information to agents and managers.

![My Cases list view in CSM Configurable Workspace showing positive, negative, and neutral case sentiment fields.](../image/task-intel-case-list-sentiment2.png "Case list with sentiment fields")

Agents can use current case sentiment to prioritize their work and ongoing sentiment as it trends over time to see if cases are moving in the right direction.

Managers can use sentiment to route cases to agents with the right empathy skills, monitor cases and reassign as needed, and avoid escalations. Manager can also identify coaching opportunities by looking at cases that ended on a negative sentiment.

**Note:** In the Xanadu release, the sentiment analysis feature can predict sentiment for cases created in English.

## Sentiment analysis machine learning models

Sentiment analysis uses a pre-trained machine learning model to evaluate email and case text and predict sentiment. This analysis takes place when a case is created and when it is updated by the customer.

<table id="table_akj_3ms_jyb"><thead><tr><th>

Cases scenario

</th><th>

Description

</th></tr></thead><tbody><tr><td>

When a case is created

</td><td>

The sentiment analysis model evaluates the following text to make a prediction:

-   Text in the subject line and body of emails.
-   Text in the short description and description of cases.

 If the model can make a prediction, it returns the following information:

-   A sentiment label and corresponding sentiment level.
    -   Positive \(1.0\)
    -   Neutral \(0.5\)
    -   Negative \(0.0\)
-   A confidence level for the prediction.

 If the model can make a prediction, the sentiment is added to the **Original sentiment** field.

 If the model can't make a prediction, the **Original sentiment** is not set.

 This system stores the sentiment prediction information in the Predictor Results for Task table.

</td></tr><tr><td>

When a case is updated

</td><td>

The sentiment analysis model evaluates the following text to make a prediction:

-   The text from the body of a reply email.
-   Comments that a customer adds to the case.

 If the model can make a prediction, it returns the following information:

-   An updated sentiment label and corresponding sentiment level.
-   A confidence level for the prediction.

 The system:

-   Updates the **Current sentiment** field with the current sentiment.
-   Compares the updated current sentiment to the original current sentiment, calculates the change in sentiment, and updates the **Sentiment over time** field.

    -   If there is an increase in the score, the **Sentiment over time** field shows Improving.
    -   If there is a decrease in the score, the **Sentiment over time** field shows Declining.
    -   If there is no change in the score, the **Sentiment over time** field continues to display the previous value.
**Note:** If the **Original sentiment** is Neutral and the **Current sentiment** is Neutral, then the **Sentiment over time** is Neutral.


 If the model can't make a prediction, no information gets recorded and the value in the **Current sentiment** field remains the same.

</td></tr></tbody>
</table>For more information about the pre-trained machine learning model, see [Create a model to predict case sentiment](csm-task-intel-create-sentiment-solution.md).

## Prediction feedback

The system stores feedback on prediction results in the Predictor Result \[ml\_predictor\_results\] table. Users with the ml\_admin role can access the table and view the results. For sentiment analysis:

-   The default value in the **Predicted correctly** field for each sentiment prediction is set to true.
-   The **Final input value** and **Final output value** fields remain empty because sentiment analysis predictions do not collect feedback from agents.

The Predictor Result table also stores information about skipped and failed predictions. For more information about this table, see [Components installed with Task Intelligence for Customer Service](../reference/case-categorization-components.md).

**Parent Topic:**[Task Intelligence for Customer Service](csm-task-intelligence.md)

**Related topics**  


[Configure Sentiment Analysis](case-sentiment-analysis-configure.md)

[Configure Sentiment Analysis](case-sentiment-analysis-configure.md)

[Create a model to predict case sentiment](csm-task-intel-create-sentiment-solution.md)

