---
title: Survey scorecard question results
description: The Question Results filter displays the result of all questions or an individual question using charts or lists. For the String, Attachment, Date, Date/time, Reference, and Ranking data types, the results are displayed in the list view. The results of all other data types are displayed in the pie chart view.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/r\_SurveyScorecardQuestionResults.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [View a survey scorecard, Survey responses and results, Use surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Survey scorecard question results

The Question Results filter displays the result of all questions or an individual question using charts or lists. For the String, Attachment, Date, Date/time, Reference, and Ranking data types, the results are displayed in the list view. The results of all other data types are displayed in the pie chart view.

## Pie chart

The pie chart shows question results for all data types other than those that are displayed in the list view. See [Survey question data types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/r_SurveyQuestionDataTypes.md).

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

\[Omitted image "SurveyScorecardQuestionPie.png"\] Alt text: Survey scorecard question results - pie chart

**Parent Topic:**[View a survey scorecard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_ViewAScorecard.md)

**Related topics**  


[Survey scorecard category results]()

[Survey scorecard average ratings]()

[Survey scorecard history]()

[Export a survey scorecard as an image]()

