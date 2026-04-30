---
title: View a survey scorecard
description: A survey scorecard provides a visual breakdown of survey responses by category, based on the way questions were answered.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Survey responses and results, Using surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# View a survey scorecard

A survey scorecard provides a visual breakdown of survey responses by category, based on the way questions were answered.

## Before you begin

Role required: survey\_admin or survey\_reader

## About this task

A scorecard displays charts for survey results, in which category and question responses are analyzed and current ratings are compared with previous ratings. Users can examine ratings over time, compare question ratings, or compare the ratings of all categories. All ratings are averages for the time range selected. The system dynamically updates a scorecard each time you view it, so the ratings reflect recently completed surveys.

## Procedure

1.  Navigate to **All** &gt; **Survey** &gt; **View Surveys**.

2.  Open a survey definition.

3.  Select the **View Scorecard** related link.

    **Note:** The **View Scorecard** related link is available only if there are survey results to report.

    The interactive scorecard displays the following filters:

    -   Question Results: Displays the result of all questions or an individual question.
    -   Category Results: Displays the results of all questions associated with an individual category or all categories.
    -   Average Ratings: Displays the result of weighted average rating for each survey question in an individual category or all categories.
    -   History: Displays the result of all questions in comparison with their history \(by calendar year or quarters\).
    -   Sentiment Analysis Results: Displays the results of sentiment analysis for the survey.

-   **[Survey scorecard category results](../reference/r_SurveyScorecardCategoryResults.md)**  
The Category Results view is a stacked bar chart showing survey results for all questions in an individual category or all categories by respondent count.
-   **[Survey scorecard question results](../reference/r_SurveyScorecardQuestionResults.md)**  
The Question Results filter displays the result of all questions or an individual question using charts or lists. For the String, Attachment, Date, Date/time, Reference, and Ranking data types, the results are displayed in the list view. The results of all other data types are displayed in the pie chart view.
-   **[Survey scorecard average ratings](../reference/r_SurveyScorecardAverageRatings.md)**  
The Average Ratings view displays the weighted average rating for each survey question in an individual category or all categories.
-   **[Survey scorecard history](../reference/r_SurveyScorecardHistory.md)**  
The History view compares the current ratings for the categories and their questions with ratings from the previous three years or four quarters.
-   **[Export a survey scorecard as an image](t_ExportAScorecardAsAnImage.md)**  
You can export a scorecard as an image to use in presentations or other documents.

**Parent Topic:**[Survey responses and results](../concept/c_SurveyResults.md)

**Related topics**  


[View results for all surveys](t_ViewResultsForAllSurveys.md)

[View the results for a survey](t_ViewResultsForASpecificSurvey.md)

[Export a quiz scorecard as an image](../../assessments/task/t_ExportAQuizScorecard.md)

[Request translations for surveys](request-translations-for-surveys.md)

[Edit translations for surveys](edit-translations-for-surveys.md)

[Survey responses in a database view](../concept/survey-result-database-view.md)

