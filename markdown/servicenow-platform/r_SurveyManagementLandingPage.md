---
title: Surveys
description: With Surveys, you can create, send, and collect responses for basic surveys. If installed, you can also use the Survey widget to set up a survey within Service Portal.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Surveys

With Surveys, you can create, send, and collect responses for basic surveys. If installed, you can also use the Survey widget to set up a survey within Service Portal.

Two versions of the application are supported, Surveys, which is the latest version, and Legacy Surveys. Survey improves the user interface and extends the capabilities of the Legacy Surveys application.

Surveys \| Getting started

## Configuring surveys

There are many options for advanced configuration in Surveys:

-   Create a survey, add questions, and choose recipients, all in one interface.
-   Create conditional questions, which appear only when users answer other questions a certain way.
-   Restrict a survey so only specific survey users can take it, and send invitations to those users simultaneously. Alternatively, make the survey a public survey so that any user can take the survey, even anonymous users \(users who have not logged in to the ServiceNow system\).

    **Tip:** The assessment\_take2 UI page should be public for public surveys. If that page is not public, anonymous users do not have access to the page and public surveys do not work.

-   Set a schedule to automatically assign a survey to users and to limit how often the same user can take a survey.
-   Customize the look and feel of survey questionnaires.
-   Save anonymous survey responses.
-   Convert survey responses to numerical scores and view them on scorecards.
-   Deactivate a survey for maintenance or to retire it without deleting it.

**Note:** Because surveys use the same tables and other back-end components as assessments, you may see assessment elements such as table and field names in certain places throughout the survey feature.

## Legacy Surveys

Survey administrators can continue to use legacy survey functionality and data, however, it is recommended that you migrate legacy surveys to the Surveys application. Concurrent use of both survey applications can cause confusion and redundancy.

Survey wizards are not impacted and cannot be migrated.

**Note:** The Legacy Surveys application is not described in the documentation that you are viewing. It is documented on the ServiceNow wiki.

|Capability|Surveys|Legacy Surveys|
|----------|-------|--------------|
|Surveys in Service Portal.|![check mark](../image/Tick.png)| |
|Save new survey responses each time a user takes the same survey.|![check mark](../image/Tick.png)| |
|Create question templates to reuse sets of answer options.|![check mark](../image/Tick.png)| |
|Categorize survey questions and report on category results.|![check mark](../image/Tick.png)| |
|Deactivate a survey without deleting it.|![check mark](../image/Tick.png)| |
|Create conditional questions.|![check mark](../image/Tick.png)| |
|Send surveys automatically based on a schedule.|![check mark](../image/Tick.png)| |
|Customize survey questionnaire color scheme.|![check mark](../image/Tick.png)| |
|Save anonymous survey responses for logged-in users.|![check mark](../image/Tick.png)| |
|View survey responses on graphical scorecards.|![check mark](../image/Tick.png)| |
|Save surveys in a draft state until they are ready to publish.|![check mark](../image/Tick.png)| |
|Create and send surveys from one page.|![check mark](../image/Tick.png)| |
|Allow only specific users to access a survey.|![check mark](../image/Tick.png)| |
|Send surveys based on conditions.|![check mark](../image/Tick.png)|![check mark](../image/Tick.png)|
|Send survey email notifications.|![check mark](../image/Tick.png)|![check mark](../image/Tick.png)|
|Limit how often a user can take the same survey.|![check mark](../image/Tick.png)|![check mark](../image/Tick.png)|
|Add introduction and end note text.|![check mark](../image/Tick.png)|![check mark](../image/Tick.png)|
|Create survey modules.|![check mark](../image/Tick.png)|![check mark](../image/Tick.png)|
|Public survey: Allow persons to take a survey without logging in.|![check mark](../image/Tick.png)|![check mark](../image/Tick.png)|
|Use update sets to track changes.|![check mark](../image/Tick.png)|![check mark](../image/Tick.png)|

-   **[Using surveys](../concept/using-surveys.md)**  
Survey administrators—users with the survey\_admin role—create and maintain surveys and configure how they are distributed and published. Surveys on Service Portal are also supported.
-   **[Surveys reference](survey-reference.md)**  
Reference topics provide additional information about the forms, fields, and properties you use while working with surveys.

**Parent Topic:**[Assessments and Surveys](../../assessments/concept/assessments-surveys-landing-page.md)

**Related topics**  


[Legacy survey migration](../concept/c_MigrateSurveys.md)

[Survey designer](../concept/c_SurveyDesigner.md)

[Survey roles](r_SurveyManagementRoles.md#)

[Surveys in Service Portal and the Now Mobile app](../concept/c_SurveyServicePortal.md)

[Service Portal](https://www.servicenow.com/docs/access?context=c_ServicePortal&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)

