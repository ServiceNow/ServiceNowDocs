---
title: Sentiment analysis for surveys
description: You can use sentiment analysis to determine whether user responses for a survey are considered positive, negative, or neutral.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/sentiment-analysis.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Survey administration, Use, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
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

-   **[Configure a sentiment connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configure-sentiment-connector.md)**  
Specify the service URL and other configuration information for third party APIs that are used for sentiment analysis.
-   **[Sentiment analysis property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/sentiment-analysis-properties.md)**  
You can use the sentiment analysis property to customize the **Sentiment Analysis** module.
-   **[Sentiment analysis results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/sentiment-analysis-results.md)**  
The sentiment analysis results view contains a bar chart that displays the percentage of positive, negative, and neutral results, along with the instance count for each category.

**Parent Topic:**[Survey administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/r_SurveyAdminTasks.md)

**Related topics**  


[View survey reports]()

[Survey designer]()

[View a survey instance]()

[Survey users and groups]()

[Copy a survey]()

[Publish a survey]()

[Customize the appearance of a survey]()

[Survey definitions]()

[Create a survey designer template question]()

[Survey questions]()

[Survey trigger conditions]()

[Survey distribution]()

[Outlook Actionable Messages]()

[Surveys in Service Portal and the Now Mobile app]()

[Surveys in ITSM Virtual Agent]()

[Legacy survey migration]()

