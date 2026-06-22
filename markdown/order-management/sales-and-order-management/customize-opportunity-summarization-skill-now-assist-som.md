---
title: Customize the opportunity summarization skill in Now Assist for SFA
description: Configure the opportunity summarization skill to generate AI-powered opportunity summaries in the CRM Workspace, including which data sources and fields contribute to the summary.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-and-order-management/customize-opportunity-summarization-skill-now-assist-som.html
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 3
keywords: [opportunity summarization, Now Assist for SFA, generative AI skill, customize skill]
breadcrumb: [Configure, Now Assist for SFA, Sales Customer Relationship Management]
---

# Customize the opportunity summarization skill in Now Assist for SFA

Configure the opportunity summarization skill to generate AI-powered opportunity summaries in the CRM Workspace, including which data sources and fields contribute to the summary.

## Before you begin

Use the Now Assist Admin console to configure the opportunity summarization skill. For additional information, see [Overview tab in Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/configuring-now-assist.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Now Assist Skills**.

2.  In the **Sales** workflow group, locate the opportunity summarization skill for Now Assist for SFA.

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

    Review and test the default prompt. To customize prompts, select **Edit prompt in Now Assist Skill Kit**. For more information, see [Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/now-assist-skill-kit-landing.md).

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


