---
title: Customize an order summarization skill in Now Assist for Order Management
description: If you have the admin role, you can configure the Now Assist for Order Management application so that your order agent and fulfilment agent can use the generative AI skills in CSM Configurable Workspace and in Platform.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-11-12"
reading_time_minutes: 4
breadcrumb: [Configure, Now Assist for Order Management]
---

# Customize an order summarization skill in Now Assist for Order Management

If you have the admin role, you can configure the Now Assist for Order Management application so that your order agent and fulfilment agent can use the generative AI skills in CSM Configurable Workspace and in Platform.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Now Assist Skills**.

2.  In the **Customer** workflow group, view the skills for the Now Assist for Order Management under SOM.

3.  Copy the Order Summarization skill for customization.

    1.  Choose either Order Summarization \(Order Capture\) or Order Summarization \(Order Fulfilment\) to make a copy of an active skill.

        **Note:** Only one version of a skill can be active at a time for each skill. If you create and activate a copy of the skill, any previously activated version of the skill is deactivated.

    2.  Select the More actions icon ![More options icon.](../../tmt-order-mgt/image/more-options.png) for the skill, and create a copy that you can customize by selecting **Make a copy**.

        The copy that you make is listed in the All section.

    3.  Select **Activate skill** on the copied skill to open and modify it.

        A guided setup leads you through configuring General details, View order input, Customize prompt output, Define Availability, Define access, select display, and Review and activate of the skill to be customized.

4.  In the General details step, fill in the fields.

    1.  Enter a name and description for the skill.

    2.  Select **Save and continue** to go to the next step.

    **Note:** The **More details on the skills** are read-only fields.

5.  Configure the base input table fields and related lists for the different input templates \(Product Order Capture or Service Order Capture\) for the skill.

    **Note:** The **Choose base table** is a ready-only field.

    Each skill relies on a base input table and input fields with descriptions to provide context for all the LLM Services to generate a response.

    Select only those related tables that are offered as the base system as part of the input data.

    1.  Select **+New base input field** and configure the base input table fields for each input template \(Product Order Capture or Service Order Capture\).

        Add multiple base input fields, as necessary.

        The following table lists the base input table fields and descriptions.

<table id="table_c53_vp5_dbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base input field

</td><td>

Field in the base input table whose value this skill uses in its response.

 For example, `Number`.

</td></tr><tr><td>

Field description

</td><td>

Description of the base input field value.

 For example, `Order number.`

</td></tr></tbody>
</table>    2.  For each input template, configure the rule conditions by using the condition builder to filter the data.

        The rule conditions determine when the input template is used. By default, the record state determines the input template that all LLM services use.

        You can build the condition out further by selecting **+New condition set** and configuring additional parameters.

    3.  For each input template, select **+New data source** to configure the additional input data sources, as needed.

        Adding input data source, like the related tables, provides more context to all LLM services in a related list.

        You can also add the rule conditions to these additional data sources.

        The selection of the related table fields has a direct impact on the quality of the corresponding prompt header.

    4.  Select **Save and continue** to go to the next step.

6.  Customize prompt output.

    Review and test the default prompt provided. The prompt is fixed and can’t be customized directly in this step or from the Now Assist Admin screen.

    To customize or create prompts, select **Edit prompt in Now Assist Skill Kit**. You are redirected to the Now Assist Skill Kit, where you can manage prompt configurations for the skill. For more info, see [Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=now-assist-skill-kit-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

    1.  For each input template \(Product Order Capture or Service Order Capture\), select a record in the Test output section and test the prompt response output format by selecting **Run Test**.

    2.  Select **Save and continue** to go to the next step.

7.  Define how the skill is available to your users in the Define availability section.

    1.  Configure the skill to be available to users, or select conditions that must be met before the skill is available.

        Selecting **Customize skill availability** displays a condition builder to filter the data further.

        Select **+New condition set** to configure additional conditions, as needed.

    2.  Select **Save and continue** to go to the next step.

8.  Select **Define access** to determine who can access this skill.

    By selecting specific roles, you're controlling who can use it. The roles you choose will also be available in the next step **Select display**.

    Default and Custom Roles:

    -   If no changes are made, the default role sn\_ind\_tmt\_orm.order\_agent automatically appears in **User access - Access Control List \(ACL\)**.
    -   Select **Roles** to apply role restrictions whenever the skill is invoked, defining which data and resources \(for example, tables\) it can access in **Role restrictions to skill**.

        **Note:** In the **Select Display** step, you can only choose roles that were added in the **Define Access** step. If you add a role in **Define Access**, you must manually select it in **Select Display** to make it active.

9.  Configure **In-product desktop** to display the order summarization for Order Management.

    1.  Select **In-product desktop** to display Now Assist skills on the forms and workspaces.

        For the skills that appear in-product, select the right arrow to identify the roles that can use the skill.

    2.  Select **Save and continue** to go to the next step.

10. Review and activate the skill.

    Review your choices and select **Activate** to complete the skill customization.

    Select **Summarize** in an order to generate the order summary.


**Parent Topic:**[Configuring Now Assist for Order Management](../concept/now-assist-for-order-management-configuring.md)

