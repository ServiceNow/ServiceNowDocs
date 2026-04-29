---
title: Survey designer elements
description: The survey designer is accessible from Survey Survey Designer .
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Survey designer, Survey administration, Use surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Survey designer elements

The survey designer is accessible from **Survey** &gt; **Survey Designer**.

The survey designer contains the **Controls** tab, the **Questions** tab, the **Categories** tab,a header bar, and the design canvas.

## Controls tab

To create a question, drag the appropriate data type control from the **Controls** palette and drop it onto the designer canvas.

![Data type controls for questions](../image/SurveyDesignerControls.png "Controls")

The assessment engine provides a built-in result calculation feature that converts responses to scored question data types to a score from 0 through 10.

<table id="table_dgb_pvh_br"><thead><tr><th>

Data type

</th><th>

Scored

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Attachment

</td><td>

No

</td><td>

Question with a Manage Attachments icon that allows users to attach one or more files.

</td></tr><tr><td>

Boolean

</td><td>

Yes

</td><td>

Question with a check box or Yes and No choices for user responses.

</td></tr><tr><td>

Choice

</td><td>

Yes

</td><td>

List of predefined options. For more information, see the definition of the **Choices** field in [Create a question in the survey designer](../task/t_CreateQuestSurveyDesigr.md).**Note:** The Choice values can only be numeric, string values will not be saved.

</td></tr><tr><td>

Date

</td><td>

No

</td><td>

Date field.

</td></tr><tr><td>

Date/Time

</td><td>

No

</td><td>

Date and time field.

</td></tr><tr><td>

Number

</td><td>

No

</td><td>

Number field with predefined minimum and maximum values. The default is 1-10.

</td></tr><tr><td>

Percentage

</td><td>

No

</td><td>

Percentage field with a prescribed range.

</td></tr><tr><td>

Scale

</td><td>

Yes

</td><td>

Predefined Likert scale. Answer options appear as radio buttons.

</td></tr><tr><td>

Numeric Scale

</td><td>

Yes

</td><td>

Selectable number scale. The default is 1-5. Answer options appear as radio buttons.

</td></tr><tr><td>

String

</td><td>

No

</td><td>

Single or multi-line text field.

</td></tr><tr><td>

Template

</td><td>

Yes

</td><td>

Choice list of templates that provide a predefined scale of options. For details, see [Quiz scorecards](../../assessments/concept/c_QuizScorecards.md).

</td></tr><tr><td>

Reference

</td><td>

No

</td><td>

Choice list of fields from a specified reference table. This data type does not support reference qualifiers. For example, a user could select a user name if you specify sys\_user as the reference table.

</td></tr><tr><td>

Image Scale

</td><td>

Yes

</td><td>

Question with a choice of images that can be selected. A template can be used to apply the same images to multiple questions.

</td></tr><tr><td>

Multiple Selection

</td><td>

Yes

</td><td>

Question with multiple check boxes that can be selected.

</td></tr><tr><td>

Ranking

</td><td>

 

</td><td>

Question with an order number to be selected for each option. One order number cannot be selected twice. This question can be mandatory and it can also be dependent on a parent question, but not vice versa.

</td></tr></tbody>
</table>## Questions tab

This tab displays all metrics added to the question bank for surveys. Use the **Filter** field to search for questions. Each metric is displayed with its name and type.

## Categories tab

This tab displays all metric categories added to the question bank for surveys. All metrics in the question bank are group under the corresponding metric category. Use the **Filter** field to search for categories or questions.

## Header bar

The tabs on the header bar display views and a menu of functions. Click a tab to change the view on the canvas:

-   **Design**: Add and configure the properties of categories and questions. This is the default view.
-   **Configuration**: Create introductions and end notes for surveys and select a [signature](../../assessments/task/t_CreateAnAssessmentSignature.md).
-   **Availability**: Select the recipients for each category in the survey.

Point to the menu icon \(![Menu icon](../image/Menu.png)\) to select an option. The list of options depends on the currently open survey.

-   **Save**: Save the current survey without changing its state.
-   **Preview**: Display a preview of the survey as it appears to recipients.
-   **Publish**: Distribute the survey to the selected recipients.
-   **Save and Publish**: Save the survey to the **Draft** state and distribute the survey in one step.
-   **New Survey**: Open a fresh canvas for a new survey.
-   **Load Survey**: View the list of existing surveys.
-   **Copy Survey**: Copy the current survey.

## Design canvas

New surveys open in the canvas of the **Design** view. The survey **Name** field appears above first category in the canvas. A blank question field appears in the category container.

![New survey question field](../image/SurveyDesignerNewSurvey.png "Initial appearance of the Survey Designer canvas")

**Parent Topic:**[Survey designer](c_SurveyDesigner.md)

**Related topics**  


[Configure a survey in the survey designer](../task/t_ConfigSurveyInSurveyDesgnr.md)

[Survey categories](c_SurveyCategory.md)

[Create a question in the survey designer](../task/t_CreateQuestSurveyDesigr.md)

[Survey question data types](../reference/r_SurveyQuestionDataTypes.md)

[Create custom metric type](../task/create-custom-templates-questions.md)

[Edit a survey in the survey designer](../task/t_EditASurveyInTheSurveyDesigner.md)

[Configure category weights for a survey](../task/t_ConfigCatWeightsForSurvey.md)

