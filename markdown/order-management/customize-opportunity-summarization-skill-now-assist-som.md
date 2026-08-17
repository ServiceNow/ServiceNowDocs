---
title: Customize the opportunity summarization skill in ServiceNow Otto for Sales Automation
description: Configure the opportunity summarization skill to generate AI-powered opportunity summaries in the CRM Workspace, including which data sources and fields contribute to the summary.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/customize-opportunity-summarization-skill-now-assist-som.html
release: australia
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 4
keywords: [opportunity summarization, generative AI skill, customize skill]
breadcrumb: [Opportunity Management, Sales automation apps, Configure, Sales Customer Relationship Management]
---

# Customize the opportunity summarization skill in ServiceNow Otto for Sales Automation

Configure the opportunity summarization skill to generate AI-powered opportunity summaries in the CRM Workspace, including which data sources and fields contribute to the summary.

## Before you begin

Use the AI Admin Hub console to configure the opportunity summarization skill. For additional information, see [Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md).

Role required: admin

## About this task

The opportunity summary draws from the following related tables by default:

-   Opportunity and opportunity line items
-   Activity data: touchpoints, appointments, meetings, emails, work notes, and tasks
-   Opportunity competitors and contacts
-   Account or consumer table

The opportunity summary appears on the Overview page and includes the following sections:

-   **Opportunity overview**

    Key details including the short description, opportunity amount, stage, account name, and the top three line items by value. For closed opportunities, the summary includes the outcome: won opportunities show the signed date; lost opportunities show the lost reason, competitor, and close date.

-   **Customer needs and pain points**

    The top two customer needs or pain points identified from the opportunity description, business goals and pain points from emails, and work notes. When sources conflict, the most recent email or work note takes precedence. The source of each need or pain point is included in the summary.

-   **Recent and upcoming activity**

    The most recent activity from touchpoints or emails, with its date and a brief description. Also includes the next open task with its due date, or the next scheduled touchpoint or meeting.

-   **Risks detected from activity**

    Up to two risks identified from recent emails, meetings, touchpoints, and tasks. Each risk includes the source. Risk types include unresolved technical concerns, budget uncertainty, timeline pressure, competitor activity, negative sentiment, price objections, and reduced scope.


## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **AI Skills**.

2.  In the **Sales** workflow group, locate the opportunity summarization skill for ServiceNow Otto for Sales Automation.

3.  Create a copy of the skill to customize.

    1.  Select the More actions icon \[Omitted image "more-options.png"\] Alt text: for the **Opportunity Summarization** skill, then select **Make a copy**.

        The copy is listed in the All section.

    2.  On the copied skill, select **Activate skill** to open and configure it.

        A guided setup leads you through General details, View opportunity input, Customize prompt output, Define availability, Define access, Select display, and Review and activate.

    **Note:** Only one version of a skill can be active at a time. Activating a copy deactivates any previously active version of the skill.

4.  In the General details step, enter a name and description for the skill, then select **Save and continue**.

    **Note:** The **More details on the skills** fields are read-only.

5.  Configure the base input table fields and related data sources for the skill.

    The skill uses the Opportunity \[sfa\_opportunity\] table as its base input table. Select only those related tables that are available in the base system as part of the input data.

    The following table lists the base input fields and descriptions.

<table id="table_opp_base_input_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base input field

</td><td>

Field in the base input table whose value the skill uses in its response.

 For example, `Number`.

</td></tr><tr><td>

Field description

</td><td>

Description of the base input field value.

 For example, `Opportunity number`.

</td></tr></tbody>
</table>    1.  Select **+New base input field** and configure the fields for the opportunity input template.

        Add multiple base input fields as needed.

    2.  Configure rule conditions using the condition builder to filter the data for the input template.

        Rule conditions determine when the input template is used. Select **New condition set** to add additional parameters.

    3.  Add additional data sources by selecting **New data source** for each related table to include, such as opportunity line items, emails, tasks, touchpoints, meetings, work notes, contacts, competitors, and the account table.

        Adding related table data sources provides more context to the AI model and improves summary quality.

        The selection of related table fields directly affects the quality of the generated summary.

    4.  Select **Save and continue**.

6.  Customize the prompt output.

    Review and test the default prompt. To customize prompts, select **Edit prompt in AI Skill Kit**. For more information, see [AI Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit-landing.md).

    1.  Select a record in the Test output section and test the prompt response by selecting **Run Test**.

    2.  Select **Save and continue**.

7.  Define when the skill is available to users in the Define availability section.

    1.  Configure the skill to be available to all users, or select **Customize skill availability** to set conditions using the condition builder.

        Select **New condition set** to add additional conditions as needed.

    2.  Select **Save and continue**.

8.  Specify which users can access the skill in the Define access section.

    Select **Roles** to restrict skill access by role. If you add a role in this step, you must also select it in the **Select display** step to make it active.

9.  Configure the **In-product desktop** field to display the opportunity summary in the CRM Workspace.

    1.  Select **In-product desktop** to display the skill on opportunity forms and workspaces.

        Select the arrow to identify which roles can use the skill in-product.

    2.  Select **Save and continue**.

10. Review your configuration and select **Activate** to complete the skill setup.

    The opportunity summary appears on the Overview page of each opportunity in the CRM Workspace.


**Related topics**  


[Summarize an opportunity using ServiceNow Otto for Sales Automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/now-assist-som-summarize-opportunity.md)

