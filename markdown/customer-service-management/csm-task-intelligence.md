---
title: Task Intelligence for Customer Service
description: Task Intelligence for Customer Service offers several AI capabilities such as language detection, record categorization, Sentiment Analysis, and Document Intelligence. These capabilities automate several routine tasks across the case lifecycle and enable agents to focus on complex case resolution.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Task Intelligence for Customer Service

Task Intelligence for Customer Service offers several AI capabilities such as language detection, record categorization, Sentiment Analysis, and Document Intelligence. These capabilities automate several routine tasks across the case lifecycle and enable agents to focus on complex case resolution.

![Case form with highlighted Task Intelligence features that automate routine tasks across the case lifecycle. For the text description, refer to the Task Intelligence for Customer Service features table.](../image/task-intel-overview-screenshot.png "Task Intelligence features on the Case form")

<table id="table_epw_m1g_vtb"><thead><tr><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Record categorization](case-categorization-overview.md)

</td><td>

Task Intelligence for Customer Service provides the following types of categorization:

-   **Multi-lingual record categorization**: Use a machine learning model that understands English, French, German, and Spanish to evaluate text in emails and records created in different languages and to predict and automatically populate fields on records in the Case table, tables that extend the Case table, and the Interaction table.

This feature uses one machine learning model to support multiple languages so you no longer need one model per language. The model can also support additional languages on demand.

-   **Attachment-based record categorization**: Use a machine learning model to parse email or record text and attachments and automatically populate fields on case and interaction records based on signals contained in the text.

This feature evaluates text in the email subject and body, the record short description and description, and the attachments and uses all of this information to predict field values. As a result, you can integrate predictions with any routing engine and automatically route records to the appropriate service desk based on these values.


</td></tr><tr><td>

[Sentiment Analysis](case-sentiment-analysis.md)

</td><td>

Detect and display the initial and ongoing sentiment of customer service cases by evaluating the following text:

-   Email subject and body
-   Case short description and description

Help agents gauge customer emotions and better prioritize their work while enabling them to provide more empathetic and compassionate customer experiences.

 Sentiment Analysis is currently available in English.

</td></tr><tr><td>

[Language detection](case-language-detection.md)

</td><td>

Identify the language used to create a customer service case and add the language to the **Language** field for the case record. This feature can identify up to 20 different languages.

 Add the identified language to the case as a skill, which is stored in the Task Skills table. This table can be configured as a related list on the Case form.

 Use the identified language to route cases to assignment groups and agents with the necessary language skills.

</td></tr><tr><td>

[Document Intelligence](csm-document-intelligence.md)

</td><td>

Document intelligence reduces the time needed to resolve the case by automating some of the routine case tasks, which enables agents to focus on more complex case resolution.

 Extract relevant information from PDF and image files, such as credit card numbers, vendor names, or customer addresses, and add that information to fields on the case.

</td></tr><tr><td>

[Task Intelligence Admin Console](csm-task-intel-admin-center.md)

</td><td>

The Admin Console provides a business friendly interface that you can use to create, train, and deploy machine learning models to predict field values for records, extract sentiment, and detect language.

 The models provide flexible options to either auto-fill values on the records or to provide recommendations only, depending on the sensitivity of those fields. An option is also available to run the model in the background only for monitoring purposes.

</td></tr><tr><td>

DocIntel Admin experience

</td><td>

The Document Intelligence application includes the DocIntel Admin experience, which provides an easy-to-use interface that you can use to do the following:-   Create and configure document processing use cases
-   Monitor the performance of Document Intelligence use cases

For more information, see [Create a Document Intelligence use case](csm-task-intel-create-di-use-case.md).

</td></tr><tr><td>

[Similar case recommendation](similar-case-recommendation.md)

</td><td>

Use the Similar Case Recommendation feature to quickly locate similar cases that offer valuable insights into the current issue. Also, use this feature to suggest cases that might be related to major problems, helping you provide more informed and efficient support.

</td></tr></tbody>
</table>## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Task Intelligence for Customer Service application

The Task Intelligence for Customer Service application \(com.snc.csm\_ml\_task\) is available from the ServiceNow Store. This application has the following plugin dependencies:

-   Predictive Intelligence for Customer Service Management \(com.snc.csm\_ml\)
-   Customer Service \(com.sn\_customerservice\)
-   Skills Management \(com.snc.skills\_management\)
-   Dynamic Translation \(com.glide.dynamic\_translation\)
-   ServiceNow Language Detection Service Spoke \(com.glide.language\_detection\_spoke\)
-   Predictive Intelligence - Task Intelligence \(com.glide.platform\_ml\_task\)
-   Admin Center for Task Intelligence \(com.sn\_ti\_admin\)

## Configuring Task Intelligence for Customer Service

After installing the Task Intelligence for Customer Service application, you can configure the different features and use the Task Intelligence Admin Console to create models. For more information, see:

-   [Install and configure Task Intelligence features](configure-task-intelligence.md#section_ojj_m5f_5vb)
-   [Set up and deploy Task Intelligence models](configure-task-intelligence.md#section_swl_45f_5vb)

## Using Task Intelligence for Customer Service

Use the Task Intelligence features to complete the following tasks:

-   Create field prediction and sentiment models for case and interaction records
-   Review and submit values extracted by Document Intelligence
-   Review Task Intelligence analytics and prediction history

For more information about these tasks, see [Use Task Intelligence for Customer Service](use-task-intelligence.md).

## AI Prediction Banner Display Behavior

AI prediction banner display in CSM Configurable Workspace: AI prediction banners in CSM Configurable Workspace are controlled by specific client-side and back end configurations that determine when and how prediction results are displayed to agents.

Client-side control: The AI Banner Display Client controls the functionality of prediction banners in CSM Configurable Workspace. This is the current implementation that replaces the deprecated version.

Default display behavior: The displayBanner property is set to false by default in the back end logic. This means that AI prediction banners are not automatically displayed unless explicitly configured to do so.

Default page requirement: AI prediction banners only work on the default page of the workspace. If you have customized workspace pages or are using non-default page layouts, the prediction banners will not display.

Standard UI Form versus workspace display: There is a clear distinction between how prediction results are displayed in the Standard UI form \(back end\) and how they are displayed in CSM Configurable Workspace. Predictions may be available and processing correctly in the Standard UI form, but the CSM Configurable Workspace display requires proper client-side configuration through the AI Banner Display Client to surface these predictions to agents.

**Tip:** When troubleshooting AI prediction banner visibility issues, verify both the back end prediction processing and the workspace client-side display configuration. Ensure you are using the default workspace page layout for banner functionality.

