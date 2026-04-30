---
title: Quiz designer
description: The quiz designer provides a single interface that users with the assessment\_admin role can use to create, edit, and distribute quizzes.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Using Quizzes, Quizzes, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Quiz designer

The quiz designer provides a single interface that users with the assessment\_admin role can use to create, edit, and distribute quizzes.

You can also use it to edit existing quizzes and change scoring parameters.

Alternatively, you can use the modules of the [assessment engine](../reference/r_Assessments.md) to create and edit the records that make up a quiz. All quiz records are stored in assessment tables and displayed in Quiz views of those tables. For details, see [Create quizzes with forms](c_CreateQuizzesWithForms.md).

## Tools on the Quiz Designer

The quiz designer includes a design canvas, a header bar, and many controls that you can use to create quizzes.

To open the quiz designer, navigate to **Quizzes** &gt; **Quiz Designer**.

The designer contains the following elements:

-   **Controls** tab
-   **Questions** tab
-   **Categories** tab
-   **Header** bar
-   Design canvas

## Controls tab

Controls for the supported question data types are available in the Controls palette. Drag and drop a control onto the designer canvas to create a question of that type.

![](../images/QuizDesignerControls.png "Question controls")

|Data type|Description|Scored|
|---------|-----------|------|
|Attachment|Question with a Manage Attachments icon that allows users to attach one or more files.|Y|
|Boolean|Question with a check box or a **Yes/No** list for user responses.| |
|Choice|List of predefined options. For more information, see the definition for **Choices** [Create quiz questions](../task/t_CreateAQuizQuestion.md). Multiple correct answers are supported.|Y|
|Date|Date field.|N|
|Date/Time|Date and time field.|N|
|Number|Number field with predefined minimum and maximum values. The default is 1-10.|N|
|Percentage|Percentage field with a prescribed range.|N|
|Scale|Predefined Likert scale. Answer options appear as radio buttons. Multiple correct answers are supported.|Y|
|Numeric Scale|Selectable number scale. The default is 1-5. Answer options appear as radio buttons. Multiple correct answers are supported.|Y|
|Image Scale|Predefined set of images. Five emojis similar to the Likert scale \(very dissatisfied to very satisfied\) are provided. However, you can upload additional images in JPG, PNG, or GIF format. Multiple correct answers are supported.|Y|
|String|Single or multiline text field.|N|
|Template|Choice list of templates that provide a predefined scale of options. For details, see [Configure a template question](../task/t_ConfigureATemplateQuestion.md). Multiple correct answers are supported.|Y|
|Reference|Choice list of fields from a specified reference table. This data type does not support reference qualifiers.| |

## Questions tab

This tab displays all metrics added to the question bank for quizzes. Use the **Filter** field to search for questions. Each metric is displayed with its name and type.

## Categories tab

This tab displays all metric categories added to the question bank for quizzes. All metrics in the question bank are group under the corresponding metric category. Use the **Filter** field to search for categories or questions.

## Header Bar

The header bar contains tabs that display different views and a menu of various functions.

Click one of the following tabs to change the view in the canvas:

-   **Design**: Add categories and questions, and configure the properties of each. This is the default view of the canvas when you open the designer.
-   **Configuration**: Create introductions and end notes for quizzes, and select a [signature](../task/t_CreateAnAssessmentSignature.md).
-   **Availability**: Select the recipients for each category in the quiz.

Point to the menu icon \(![Menu icon](../../survey-administration/image/Menu.png)\) in the in the upper right of the quiz designer to select the following options:

-   **Save**: Saves the current quiz.
-   **Preview**: Displays a preview of the quiz as it appears to the recipients.
-   **Publish**: Distributes the quiz to the selected recipients.
-   **Save and Publish**: Saves and distributes the quiz in one step.
-   **New Quiz**: Opens a fresh canvas for a new quiz.
-   **Load Quiz**: Opens a list of existing quizzes that you can select and edit.
-   **Copy Quiz**: Creates a copy of the quiz.

The availability of each option depends on the status of the quiz that is opened in the quiz designer.

## Design Canvas

New quizzes open in the **Design** view. The quiz **Name** field appears above first category in the canvas. A blank question field appears in the category container.

-   **[Create a quiz](../task/t_CreateaQuiz.md)**  
When you create a quiz, you can create one or more categories and then add questions to each category.
-   **[Edit a quiz](../task/t_EditaQuiz.md)**  
You can update a quiz after the quiz has been distributed.
-   **[Enable a quiz retake](../task/t_EnableAQuizRetake.md)**  
You can configure a quiz to allow recipients to resubmit their answers as many times as they like, until the quiz's due date.
-   **[View a quiz result](../task/t_ViewAQuizResult.md)**  
You can view quiz results for each question and category, or view the quiz scorecard for a detailed breakdown.

**Parent Topic:**[Using Quizzes](using-quizzes.md)

**Related topics**  


[View an assessment category result](../task/t_ViewACategoryResult.md)

[View a quiz scorecard](../task/t_ViewAQuizScorecard.md)

[Create a quiz](../task/t_CreateaQuiz.md)

[Edit a quiz](../task/t_EditaQuiz.md)

