---
title: Survey responses and results
description: There is a metric result record for each user response to each question on every survey instance. Survey results for each question and category are calculated automatically based on the metric result records.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Survey responses and results

There is a metric result record for each user response to each question on every survey instance. Survey results for each question and category are calculated automatically based on the metric result records.

If you use survey result calculations for results and scorecards, ensure that the [positive indicator](../task/t_CreateQuestSurveyDesigr.md) field for the question is set appropriately, based on the answer options. To have any results, a category must contain scored questions.

## Survey responses

Survey responses are stored in the Metric Result \[asmt\_metric\_result\] table and display the recipients' answers to each question in a category. To view general results, navigate to **Survey** &gt; **Survey Responses**. To view results for a particular criterion, use a filter on the Metric Result \[asmt\_metric\_result\] table. For example, to view results based on the assignment group, apply a filter condition for assignment group.

![Survey metric results](../image/SurveyDesignerResults.png "Survey metric results")

## Category results

Category results are stored in the Assessment Category Result \[asmt\_category\_result\] table and display the overall ratings for each category based on the weighted value for each scored question. To view these results, navigate to **Assessments** &gt; **Results** &gt; **Category results** and filter the results using the **\[Type.Evaluation method\] \[is\] \[Survey\]** condition.

![Assessment category results](../image/SurveyDesignerCategoryResultsList.png "Assessment category results")

## Survey scorecards

A scorecard provides a visual breakdown of survey responses, based on the way questions were answered, by category. To access a scorecard, see [View a survey scorecard](../task/t_ViewAScorecard.md).

-   **[View results for all surveys](../task/t_ViewResultsForAllSurveys.md)**  
You can view the survey responses that are stored on the Metric Result \[asmt\_metric\_result\] table.
-   **[View the results for a survey](../task/t_ViewResultsForASpecificSurvey.md)**  
You can view the responses for one survey definition. Survey results are stored on the Metric Result \[asmt\_metric\_result\] table.
-   **[View a survey scorecard](../task/t_ViewAScorecard.md)**  
A survey scorecard provides a visual breakdown of survey responses by category, based on the way questions were answered.
-   **[Export a quiz scorecard as an image](../../assessments/task/t_ExportAQuizScorecard.md)**  
You can export scorecards as images.
-   **[Request translations for surveys](../task/request-translations-for-surveys.md)**  
Request translations for surveys to localize them into one or more languages. Localization requested items that are created for the selected surveys in all the selected languages.
-   **[Edit translations for surveys](../task/edit-translations-for-surveys.md)**  
Edit the translations for surveys, and after you make the changes, you can publish the translation.
-   **[Survey responses in a database view](survey-result-database-view.md)**  
You can view survey responses in a database view for reporting purposes. For each survey instance, you can view the instance as a single row and the answers to each survey question \(metric\) in the corresponding columns. Analyze the responses easily and, if you want, export the survey responses.

**Parent Topic:**[Using surveys](using-surveys.md)

**Related topics**  


[View a survey scorecard](../task/t_ViewAScorecard.md)

[Survey designer elements](c_SurveyDesignerElements.md)

[Configure category weights for a survey](../task/t_ConfigCatWeightsForSurvey.md)

