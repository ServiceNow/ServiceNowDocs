---
title: Survey responses in a database view
description: You can view survey responses in a database view for reporting purposes. For each survey instance, you can view the instance as a single row and the answers to each survey question \(metric\) in the corresponding columns. Analyze the responses easily and, if you want, export the survey responses.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Survey responses and results, Using surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Survey responses in a database view

You can view survey responses in a database view for reporting purposes. For each survey instance, you can view the instance as a single row and the answers to each survey question \(metric\) in the corresponding columns. Analyze the responses easily and, if you want, export the survey responses.

You can create a database view on the Survey Definition form. After the database view is created, you can either export the survey response using the standard capabilities of the ServiceNow® platform or choose to create a report of the survey responses using the Reporting module.

Use the **View Responses in Rows** related link on the Survey Definition form to view each survey instance response in a separate row and each survey question as the name of the corresponding column. The answer to the question is displayed in that column. To export the survey response in a tabular form, in the context menu, click **Export**.

The first three columns of the form show the number of the survey instance \(instance ID\), who the survey is assigned to, and the task. A maximum of five active metrics are displayed in the view by default. The Survey Definition form doesn’t show the **View Responses in Rows** related link when the following conditions occur.

-   There are more than five active metrics.
-   There are no responses to the survey instance.
-   There are more than 100 K responses for that particular survey. To view this database view of the survey responses, the number of responses must be less than or equal to 100 K. But, the database view is still accessible for more than 100 K responses when it’s already open in a new tab.

The database view can show the start date, due date, expiry date, and completed date, but this information is not available by default. If the survey instance is triggered, then the trigger record is displayed in the Task column. The total number of survey responses isn’t displayed in the database view. For the ranking and multiple-choice metrics, based on user survey responses, multiple records are displayed instead of one record per survey instance.

**Note:** Any change or update to survey configuration or metadata \(For example, addition or deletion of a new metric or category\) might affect the database view. In such cases, an event \(survey.results\_view.updated\) is generated so that users can take necessary actions to synchronize the data.

**Parent Topic:**[Survey responses and results](c_SurveyResults.md)

**Related topics**  


[View results for all surveys](../task/t_ViewResultsForAllSurveys.md)

[View the results for a survey](../task/t_ViewResultsForASpecificSurvey.md)

[View a survey scorecard](../task/t_ViewAScorecard.md)

[Export a quiz scorecard as an image](../../assessments/task/t_ExportAQuizScorecard.md)

[Request translations for surveys](../task/request-translations-for-surveys.md)

[Edit translations for surveys](../task/edit-translations-for-surveys.md)

