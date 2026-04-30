---
title: HR surveys
description: HR Surveys let users rate their satisfaction with HR case resolution, and provide management with feedback to improve HR processes.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# HR surveys

HR Surveys let users rate their satisfaction with HR case resolution, and provide management with feedback to improve HR processes.

One predefined HR survey is provided: HR Request Satisfaction Survey. HR administrators and HR managers can edit HR surveys and the associated trigger conditions.

The HR Request Satisfaction Survey is triggered randomly for 50% of closed HR cases. Users receive an email with the survey link after they accept the resolution or when the HR case is closed incomplete.

HR managers and administrators can review responses by question and see a scorecard. Comments entered by users provide feedback that can be used to improve the performance of HR case management. The following survey options can be configured.

-   The look and feel of the questionnaire, for example, by adding the company logo.
-   Conditional questions that appear when users answer other questions in a certain way.
-   The trigger condition, for example, to send it for every case or to a lower percentage of users.

With trigger conditions, the system generates a survey instance each time a specific action occurs on a given table, such as when an HR request closes. You can choose to send a survey every time the condition is met. Or, you can set a probability for the system to send a survey at random when the condition is met. Trigger conditions are ideal for sending surveys to measure satisfaction with a recent experience, such as closing an HR request.

When defining conditions like case sensitivity or null values, see API[GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

For more detailed information about working with surveys, trigger conditions, and survey questions, see [Get started with Survey Management](https://www.servicenow.com/docs/access?context=r_SurveyManagementLandingPage&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

-   **[Add or modify an HR survey](../task/t_CreateOrModifyAnHRSurvey.md)**  
You can modify the predefined HR satisfaction surveys to suit the needs of the organization, and create HR surveys.
-   **[Add or modify HR survey categories and questions](../task/t_CreateOrModifyHRSurveyQuestionsIst.md)**  
When an HR survey definition is created, a survey category is automatically added. You can create questions that are associated with this category or define another category for questions.
-   **[Publish a new HR survey](../task/t_PublishANewHRSurveyIst.md)**  
Publish a new survey so users can complete it.
-   **[Add a trigger condition for an HR survey](../task/t_CreateTriggerConditionForHRSurveyIst.md)**  
When you create an HR survey, you can add a trigger condition to specify when the survey is sent and to whom.

**Parent Topic:**[HR Administration](c_AdministerHRServiceManagement.md)

