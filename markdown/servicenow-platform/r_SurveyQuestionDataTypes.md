---
title: Survey question data types
description: You must choose a data type for each survey question. The data type determines the format of the question and the kind of data that is collected on survey questionnaires.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/r\_SurveyQuestionDataTypes.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Survey designer, Survey administration, Use surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Survey question data types

You must choose a data type for each survey question. The data type determines the format of the question and the kind of data that is collected on survey questionnaires.

The following data types are available for surveys:

## Attachment data type

On questionnaires, users can attach one or more files to a question.

Users click the Manage Attachments icon and select one or more files in the Attachments pop-up window to attach to the question. From this window, users can:

-   View a list of the attached files.
-   View an attached file in a separate window.
-   Rename an attached file.
-   Add or delete files

Once a survey has been submitted, attachments cannot be updated or deleted.

Any type of file supported by the platform can be attached to a question. One or more files can be attached a question while taking a survey or completing an assessment.

The assessment administrator can see the attachments associated with an individual question as well as those associated with the survey.

See [Administering attachments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AdministeringAttachments.md) for more information.

## Boolean data type

On questionnaires, users select a check box beside a statement or leave it cleared.

\[Omitted image "CheckboxDataType.png"\] Alt text: Boolean data type question

If you select **Boolean**, you must fill in the **Scale definition** field. Select **High** if it is best when users select the check box.

## Choice data type

On questionnaires, users select a value from a list of choices.

\[Omitted image "SurveyDataTypeChoice.png"\] Alt text: Choice data type question

If you select **Choice**, you must fill in the **Scale definition** field and create answer options. Select **High** for the scale definition if the answer option with the largest metric definition **Value** is best.

**Note:** The system sets the **Min** and **Max** fields automatically based on the **Value** settings for the associated metric definitions.

## Date and Date/Time data types

The **Date** and **Date/Time** data types are similar.

-   **Date:** On questionnaires, users select a date.

    \[Omitted image "SurveyDataTypeDate.png"\] Alt text: Date data type question

-   **Date/Time:** On questionnaires, users select a date and time.

    \[Omitted image "SurveyDataTypeDateTime.png"\] Alt text: Date/time data type question


## Likert Scale data type

On questionnaires, users select a multiple choice value from a custom Likert scale. Each answer option is represented by a radio button on the scale. A Likert scale question that evaluates an application's ease of use might have the answer options **Easy**, **Average**, and **Difficult**.

\[Omitted image "SurveyDataTypeScale.png"\] Alt text: Likert scale data type question

If you select **Likert Scale**, you must fill in the **Scale definition** field and create answer options. Select **High** for the scale definition if the answer option with the largest metric definition **Value** is best.

**Note:** The system sets the **Min** and **Max** fields automatically based on the **Value** settings for the associated metric definitions.

## Number data type

On questionnaires, users enter a number.

\[Omitted image "SurveyDataTypeNumber.png"\] Alt text: Number data type question

If you select **Number**, you must fill in these additional fields:

-   **Scale definition**: Select **High** if a larger number is better, such as for a question that measures the number of sales made in a quarter.
-   **Min** and **Max**: Enter the smallest and largest numbers users can enter. State the range of acceptable answers in the question text.

## Percentage data type

On questionnaires, users enter a number.

\[Omitted image "SurveyDataTypePercentage.png"\] Alt text: Percentage data type question

If you select **Percentage**, you must fill in these additional fields:

-   **Scale definition**: Select **High** if a larger percentage is better, such as for a question that measures the percentage of work an agent has completed.
-   **Min** and **Max:** Enter the smallest and largest numbers users can enter. Generally **0** and **100** are appropriate minimum and maximum values. If you choose values other than **0** and **100**, it is usually best to state the range of acceptable answers in the question text.

## Reference data type

On questionnaires, users select a value from a list that is generated from a specified reference table. The response field supports auto-completion.

**Note:** Reference qualifiers are not supported.

For example, a user could select a user name in response to a question if you specify User \[sys\_user\] as the reference table.

\[Omitted image "ReferenceQExample.png"\] Alt text: Reference data type question

## String data type

On questionnaires, users enter text. When you select **String**, the **String option** field appears. Select one of the following options to determine how the string field appears on questionnaires:

-   \[Omitted image "StringSingleLineDataType.png"\] Alt text: String single-line data type question

-   \[Omitted image "StringSingleLineWideDataType.png"\] Alt text: String single-line wide data type question

-   \[Omitted image "StringMultilineDataType.png"\] Alt text: String multiline data type question


## Template data type

On questionnaires, users select a value from a predefined series of answer options. To use this data type, a question template must be defined.

If you select **Template**, you must fill in these additional fields:

-   **Template**: Select a template.
-   **Scale definition**: Select **High** if the answer option with the largest template definition **Value** is best.

## Yes/No data type

On questionnaires, users select **Yes** or **No** from a list.

\[Omitted image "SurveyDataTypeYesNo.png"\] Alt text: Yes/no data type question

If you select **Yes/No**, you must fill in the **Scale definition** field. Select **High** if **Yes** is the best answer.

## Image Scale data type

On questionnaires, users select an image from a predefined set of images as their response. Image scale questions can also be used in a template for better performance with surveys that have the same type of answer options.

Five emojis, similar to the Likert scale \(very dissatisfied to very satisfied\) are provided. However, you can upload additional images in JPG, PNG, or GIF format. Two images can be uploaded, one for selected case and another for unselected case. For example, the selected image can be \[Omitted image "Selected\_image.png"\] Alt text: Representation of selected image, and the unselected image can be \[Omitted image "Unselected\_image.png"\] Alt text: Representation of unselected image. Larger size images are reduced to 64 x 64 pixels.

\[Omitted image "SurveyDataTypeImageScale.png"\] Alt text: Image Scale data type question

The result behavior depends on the presence of uploaded images. If no selected image is uploaded, then the question shows up blank.

|Selected image|Unselected image|Result|
|--------------|----------------|------|
|Yes|Yes|Unselected image loads. Clicking the image changes it to the selected image.|
|Yes|No|Selected image loads with 50% opacity. Clicking the image changes the opacity to 100%.|
|No|Yes|A blank placeholder box is displayed.|
|No|No|A blank placeholder box is displayed.|

**Note:**

-   N/A option is not supported for image scale type question.
-   For an image scale type question, an empty string is saved as an answer for a hidden and dependent question of an unselected image.

## Multiple selection data type

On questionnaires, users can select multiple check boxes indicating all answers that apply. For instance, a user can be instructed to "Select all that apply" in a multiple selection question.

\[Omitted image "SurveyDataTypeMultSelect.png"\] Alt text: Multiple Selection data type question

## Ranking data type

On questionnaires, users can select a different order number for each option to rank them. Drag-and-drop functionality is also supported, which allows a user to either fill in the number, or simply drag an option.

\[Omitted image "SurveyDataTypeRanking.png"\] Alt text: Setting the order of the options

One order number cannot be selected twice. This question can be mandatory and it can also be dependent on a parent question, but not vice versa.

**Parent Topic:**[Survey designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_SurveyDesigner.md)

**Parent Topic:**[Survey questions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_SurveyQuestion.md)

**Related topics**  


[Survey designer elements]()

[Configure a survey in the survey designer]()

[Survey categories]()

[Create a question in the survey designer]()

[Create custom metric type]()

[Edit a survey in the survey designer]()

[Configure category weights for a survey]()

[Create or modify survey questions]()

[Survey question template]()

[Add a metric category and metric in the question bank for surveys]()

[Create or modify answer options]()

[Change the order of survey questions]()

[Survey question template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_SurveyQuestionTemplate.md)

