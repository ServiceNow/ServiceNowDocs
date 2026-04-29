---
title: Sentiment analysis for surveys
description: You can use sentiment analysis to determine whether user responses for a survey are considered positive, negative, or neutral.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Survey administration, Use surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Sentiment analysis for surveys

You can use sentiment analysis to determine whether user responses for a survey are considered positive, negative, or neutral.

Activate the Sentiment Analysis \(com.snc.sentiment\_analysis\) plugin.

For a survey, you can select questions that should be used for analysis. The survey responses of these questions are sent to the thirdparty platforms for analysis through the specified connector configurations.

**Note:** You can only use string type questions for sentiment analysis.

The sentiment analysis results are displayed under **Survey** &gt; **Question Sentiment Results**. The sentiment label is based on the normalized score:

|Normalized score|Sentiment label|
|----------------|---------------|
|-1 to 0|Negative|
|0|Neutral|
|0 to 1|Positive|

## API Version and Score Calculation

Currently, this plugin uses the MSAzure text analytics API \(v2\), which is now deprecated. To ensure continued functionality and compatibility, we are migrating to the newer v3 API.

**v2 API response format:**

```

               {
               "documents": [
               {
               "id": "1",
               "score": 0.14829033613204956
               }
               ],
               "errors": []
               }
            
```

**v3 API response format:**

```

               {
               "documents": [
               {
               "id": "1",
               "sentiment": "negative",
               "confidenceScores": {
               "positive": 0.02,
               "neutral": 0.0,
               "negative": 0.97
               },
               "sentences": [
               {
               "sentiment": "negative",
               "confidenceScores": {
               "positive": 0.02,
               "neutral": 0.0,
               "negative": 0.97
               },
               "offset": 0,
               "length": 44,
               "text": "I love this hotel, but the service was slow."
               }
               ],
               "warnings": []
               }
               ],
               "errors": [],
               "modelVersion": "2025-01-01"
               }
            
```

**Score Calculation for v3 API**

Since the v3 API response format provides confidence scores instead of a single score, the normalized score is calculated using the following formula:

`score = (1 × positive) + (0.5 × neutral) + (0.01 × negative)`

This formula ensures:

-   Positive confidence pushes the score toward 1
-   Neutral confidence centers the score around 0.5
-   Negative confidence slightly pulls the score toward 0, with minimal weight \(0.01\) to account for negative sentiment

Since the three confidence scores always sum to 1, this formula generates a consistent value in the range of -1 to 1, representing the full mix of sentiment information from the Azure API.

-   **[Configure a sentiment connector](../task/configure-sentiment-connector.md)**  
Specify the service URL and other configuration information for third party APIs that are used for sentiment analysis.
-   **[Sentiment analysis property](../reference/sentiment-analysis-properties.md)**  
You can use the sentiment analysis property to customize the **Sentiment Analysis** module.
-   **[Sentiment analysis results](../reference/sentiment-analysis-results.md)**  
The sentiment analysis results view contains a bar chart that displays the percentage of positive, negative, and neutral results, along with the instance count for each category.

**Parent Topic:**[Survey administration](../reference/r_SurveyAdminTasks.md)

**Related topics**  


[View survey reports](../task/view-survey-overview.md)

[Survey designer](c_SurveyDesigner.md)

[View a survey instance](../task/t_ViewSurveyInstance.md)

[Survey users and groups](c_SurveyUsersAndGroups.md)

[Copy a survey](../task/copy-survey.md)

[Publish a survey](../task/t_PublishASurvey.md)

[Customize the appearance of a survey](../task/t_CustomizingAppearance.md)

[Survey definitions](c_SurveyDefinitions.md)

[Create a survey designer template question](../task/t_CreateASurveyDesignerTemplateQ.md)

[Survey questions](c_SurveyQuestion.md)

[Survey trigger conditions](c_TriggerConditions.md)

[Survey distribution](c_SurveyDistribution.md)

[Outlook Actionable Messages](../../outlook-actionable-messages/concept/outlook-actionable-messages.md)

[Surveys in Service Portal and the Now Mobile app](c_SurveyServicePortal.md)

[Surveys in ITSM Virtual Agent](survey-virtual-agent.md)

[Legacy survey migration](c_MigrateSurveys.md)

