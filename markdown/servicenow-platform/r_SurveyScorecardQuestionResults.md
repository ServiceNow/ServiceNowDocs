---
title: Survey scorecard question results
description: The Question Results filter displays the result of all questions or an individual question using charts or lists. For the String, Attachment, Date, Date/time, Reference, and Ranking data types, the results are displayed in the list view. The results of all other data types are displayed in the pie chart view.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [View a survey scorecard, Survey responses and results, Using surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Survey scorecard question results

The Question Results filter displays the result of all questions or an individual question using charts or lists. For the String, Attachment, Date, Date/time, Reference, and Ranking data types, the results are displayed in the list view. The results of all other data types are displayed in the pie chart view.

## Pie chart

The pie chart shows question results for all data types other than those that are displayed in the list view. See [Survey question data types](r_SurveyQuestionDataTypes.md).

-   Checkbox.
-   Boolean.
-   Choice.
-   Likert Scale.
-   Number.
-   Percentage.
-   Yes/No.
-   Image Scale.
-   Multiple Selection.
-   Template. The question result shows the aggregated net promoter score \(NPS\) with promoters, detractors, and passives.

    |Question score|NPS category|
    |--------------|------------|
    |9 or 10|Promoter|
    |7 or 8|Passive or Neutral|
    |0 to 6|Detractor|

    The result is calculated as:

    -   %Promoters = Number of promoters / Sample size
    -   %Detractors = Number of detractors / Sample size
    -   %Passives = Number of passives / Sample size
    -   NPS = %Promoters - %Detractors

**Note:** The **Checkbox** and **Yes/No** data types are combined into the **Boolean** data type in the survey designer.

When a user submits a survey, three records \(one for each Timeframe\) will be created/ updated- **Year**, **Quarter**, and **Monthly** in the **asmt\_nps\_result** table. For example, if a user submits a survey on November month of 2023, which falls under Quarter 3. Then three records are generated for the dates.

-   Year: 2023-01-01
-   Quarter: 2023-10-01
-   Monthly: 2023-11-01

Now if a second user submits in December month of 2023, which falls under same Quarter 3, as above scenario. Then only a single record is created for Monthly Time frame.

![Survey scorecard question results - pie chart](../image/SurveyScorecardQuestionPie.png "Survey scorecard question results - pie chart")

**Parent Topic:**[View a survey scorecard](../task/t_ViewAScorecard.md)

**Related topics**  


[Survey scorecard category results](r_SurveyScorecardCategoryResults.md)

[Survey scorecard average ratings](r_SurveyScorecardAverageRatings.md)

[Survey scorecard history](r_SurveyScorecardHistory.md)

[Export a survey scorecard as an image](../task/t_ExportAScorecardAsAnImage.md)

