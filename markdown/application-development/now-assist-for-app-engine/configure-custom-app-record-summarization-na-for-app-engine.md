---
title: Configure the custom app record summarization skill
description: Configure the custom app record summarization skill to define the records and outputs for ServiceNow Otto for App Engine summaries.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/now-assist-for-app-engine/configure-custom-app-record-summarization-na-for-app-engine.html
release: australia
product: Now Assist for App Engine
classification: now-assist-for-app-engine
topic_type: task
last_updated: "2026-07-24"
reading_time_minutes: 4
keywords: [ServiceNow Otto for App Engine, configure ServiceNow Otto for App Engine, configure custom app record summarization, configure AI skill]
breadcrumb: [Configure, ServiceNow Otto for App Engine, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Configure the custom app record summarization skill

Configure the custom app record summarization skill to define the records and outputs for ServiceNow Otto for App Engine summaries.

## Before you begin

Role required: admin

You must have the custom app record summarization skill activated to configure the skill. For more information, see [Activate the custom app record summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-app-engine/activate-custom-app-record-summarization-na-for-app-engine.md).

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Skills**.

2.  On the AI Admin Hub Skills page, select App Engine from the side panel.

3.  In the custom app record summarization card, select the actions icon \[Omitted image "sn-studio-more-options-icon.png"\].

4.  Select **Edit**.

5.  On the Select an app page, choose the app containing the data that you want to summarize by selecting the check box next to the app name.

6.  Select **Save and continue**.

7.  Choose the table that contains the data you want to generate AI summaries for.

    You can generate summaries for records in most custom tables on the ServiceNow AI Platform. However, some tables are restricted. For more information, see [Custom app record summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-app-engine/custom-app-record-summarization-na-for-app-engine.md).

    1.  On the Choose data source page, select the **Base input table** field.

    2.  Select the table containing the data you want to summarize.

        When you select a table from the list, the required fields from the table are automatically included in the AI summary.

    3.  To include additional fields from the table in the summary, select **+ New base input field** and select the field that you want to add.

    4.  For each field in the table that you want included in the AI summary, enter a description and context for the field in the **Field description** field.

    5.  To add related data sources that you want included in summaries, such as related tables, select **+ New data source**, then select the additional data source from the list.

        For more information about the kinds of data sources that can be included in AI summaries, see [Custom app record summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-app-engine/custom-app-record-summarization-na-for-app-engine.md).

    6.  To add more tables, select **+ New input table**. Then repeat the process in steps a through e to define the fields that you want to be included in the summary.

    7.  When you're finished, select **Save and continue**.

8.  Test the summaries that are generated.

    **Important:** Each time you test the output of generative AI skills, the operation counts as an assist that is tracked by your subscription. To track your AI usage, see [Monitoring Now Assist usage in Subscription Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/monitoring-now-assist-usage.md).

    1.  On the Test summary output page, in the **Base input table** field, select the table that you want to test from the list.

    2.  In the **Additional instructions for LLM** field, enter additional information about the context and purpose of the table.

    3.  In the **Record** field, select the record that you want included in the AI summary.

    4.  Select **Run test**.

    5.  Review the AI-generated summary in the Result panel.

    6.  Test each table that you want to summarize and adjust the instructions and field descriptions as needed to improve the summary quality.

    7.  When you have completed testing, select **Save and continue**.

9.  Define which users have access to the skill.

    1.  To adjust which roles have access to the skill, select the edit icon \(\[Omitted image "crs-edit-pencil-icon-purple.png"\]\).

    2.  Follow the instructions outlined in [Configure security controls for a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/nask-access-control.md) to control who has access to the skill.

    3.  When finished, select **Save and continue**.

10. Choose the display option that determines how users access the skill.

    For more information about display options, see [Custom app record summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-app-engine/custom-app-record-summarization-na-for-app-engine.md).

    1.  Select the toggle on icon \(\[Omitted image "toggle-on.png"\] Alt text:\) for the display option that you want to enable.

    2.  To enable access for certain roles, select the expand icon \(\[Omitted image "na4ae-expand-icon.png"\]\) for the display option that you want to define access to.

    3.  In the **user roles** field, enter the name of the role that you want to grant access to, then select the role from the list.

        **Note:** You can grant access to multiple roles. Select all roles that you want to grant access to from the list.

    4.  When finished, select **Save and continue**.

11. Review and verify that the skill details are correct.

12. When you're ready to activate the skill, select **Done**.


## Result

The custom app record summarization skill is now ready for use in the custom app that you defined.

## What to do next

To use the custom app record summarization skill, see [Using ServiceNow Otto for App Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-app-engine/use-now-assist-for-app-engine-enterprise.md).

