---
title: Custom app record summarization skill
description: The Now Assist for App Engine custom app record summarization skill generates AI summaries for the contents of records in custom applications and tables.
locale: en-US
release: zurich
product: Now Assist for App Engine
classification: now-assist-for-app-engine
topic_type: concept
last_updated: "2025-10-09"
reading_time_minutes: 4
keywords: [custom table record summarization, Now Assist for App Engine, AI skill, AI in custom apps, table summary generation]
breadcrumb: [Explore, Now Assist for App Engine, AI in custom applications, Developing your application, Building applications]
---

# Custom app record summarization skill

The Now Assist for App Engine custom app record summarization skill generates AI summaries for the contents of records in custom applications and tables.

## Record summarization overview

Starting with version 28.2.4 of Now Assist for App Engine, you can use the custom app record summarization skill to generate AI summaries for records in custom tables and applications. Record summarization enables you to learn important details and context about a record quickly, helping to save you time and reduce repeated efforts.

The custom app record summarization skill is highly configurable, enabling you to define the data, experience, and access for the summaries that Now Assist generates. You can specify the tables and fields that you want Now Assist to summarize. You can also include additional data sources, such as emails and attachments, for Now Assist to use when generating summaries. You can then define which users have access to the summaries and how users interact with the summaries. Learn more about the custom app record summarization skill and how you can configure it to work for your custom applications in the following sections.

## Data sources

The custom app record summarization skill can generate summaries for records in any table that's created within a custom application. The application can be global or scoped.

You can configure the custom app record summarization skill to summarize as many tables as needed for your custom application. During the configuration process, you define which table or tables you want the skill to summarize. For each table that you select, you must define the fields that Now Assist should include in the summaries and provide additional context about the fields that you selected.

For example, let's say that you want Now Assist for App Engine to summarize the records in a table for your paid time off \(PTO\) request application. You select the table that stores details about each employee's PTO request, such as the dates that the employee is requesting time off from work and the approval status of the request. When you select the fields that you want to include in the summaries that Now Assist generates, you must enter a description for each field. Field descriptions provide additional information and context about the purpose of the field, helping Now Assist to generate summaries that are more accurate. The following table illustrates how to write field descriptions for Now Assist summaries.

|Field in the PTO request table|Field description|
|------------------------------|-----------------|
|**PTO start date**|`Date that the employee's PTO begins. Date is in MM-DD-YYYY format.`|
|**PTO end date**|`Date that the employee's PTO ends. Date is in MM-DD-YYYY format.`|
|**Approval status**|`Field that indicates whether the PTO request has been approved, denied, or hasn't been reviewed yet.`|

## Additional data sources

Now Assist for App Engine can include additional data sources when generating a summary of a record, such as:

-   Related tables
-   Relationships
-   Emails
-   Attachments

For each related table or relationship that you add, you must provide the fields and field descriptions that you want Now Assist to include in summaries. Activities, such as emails and attachments, don't have fields that you can select and configure. If you select either email or attachment as an additional data source to include in a summary, Now Assist attempts to fetch that data at the time that the summary is generated. If an email or attachment is present within the record, Now Assist includes that information in the summary that it generates. Otherwise, the summary is generated without the email or attachment.

**Important:** Record summarization that includes an attachment has a greater assist usage. To track your Now Assist usage, see [Monitoring Now Assist usage in Subscription Management](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Display options

You can choose where you want record summarization to be available to your application users during the skill configuration process. The display options that you can select are: in-product, Now Assist panel, or both.

**Note:** The display options that you choose applies to every application that uses the Now Assist for App Engine custom app record summarization skill.

-   **In-product**

    When selected, Now Assist summaries are displayed on forms and workspaces.

    ![You can select the Summarize button on a record page to generate a summary.](../image/na4ae-in-product-display.png "Now Assist summary on a record page")

    ![You can select the Summarize button within a workspace to generate a summary.](../image/na4ae-summary-in-workspace.png "Now Assist summary in a workspace")

    For more information about adding record summarization to a workspace, see the following resources:

    -   [Customize UI Builder pages using components](../../../administer/ui-builder/concept/work-components.md)
    -   [Components documentation for the AI summary card](https://horizon.servicenow.com/workspace/components/now-ai-summary-card?release=zurich)
    -   [UI Builder setup documentation for the AI summary card](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/now-ai-summary-card/uib-setup)
-   **Now Assist panel**

    When selected, Now Assist summaries are accessible through chat in the Now Assist panel. If you don't see this option when configuring the skill, you must activate the Now Assist panel. For more information, see [Turn on the Now Assist panel](https://www.servicenow.com/docs/bundle/zurich-intelligent-experiences/page/administer/now-assist-admin/task/activate-now-assist-panel.html).

    ![You can select Summarize a Custom Table Record in the Now Assist panel to summarize a record through chat.](../image/na4ae-now-assist-panel.png "Option to generate a summary in the Now Assist panel")


## Access

You can define which users and groups have access to generate Now Assist summaries. During configuration, you can add roles and conditions that restrict when and for whom the skill is available. You can also customize whether certain roles have access to a particular display option.

