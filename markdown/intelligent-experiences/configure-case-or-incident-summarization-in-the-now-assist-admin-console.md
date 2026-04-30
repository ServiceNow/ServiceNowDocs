---
title: Configure case or incident summarization in the Now Assist Admin console
description: Configure case or incident summarization by using the guided setup in the Now Assist Admin console. You can choose the input tables and fields as well as customize the prompt output for copies of the record summarization skills.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [Configure, Case, incident, record, summarization, Now Assist, guided setup, admin console, gen AI, generative AI]
breadcrumb: [Make a copy of a Now Assist skill, Using Now Assist Admin, Now Assist, Enable AI experiences]
---

# Configure case or incident summarization in the Now Assist Admin console

Configure case or incident summarization by using the guided setup in the Now Assist Admin console. You can choose the input tables and fields as well as customize the prompt output for copies of the record summarization skills.

Prompt configurability in the Now Assist Admin console for setting up case/incident summarization skill copies 

## Before you begin

You can only customize the input data and prompt output for a copy of a record summarization skill. To learn more about making a skill copy, see [Make a copy of a Now Assist skill](make-a-copy-of-a-now-assist-skill.md). After you create a skill copy, you can learn the steps to complete the skill setup here.

Role required: nsa\_admin

## About this task

By default, many settings for Now Assist record summarization are optimized for general use cases. Review your goals for incorporating generative AI on your instance to determine whether you want to make changes and what those changes are. After you have made a plan, you can create a copy of a skill and modify the input sources and prompt output.

## Procedure

1.  In the **Name of the skill** field, enter the skill name.

    The default name adds \(copy\) to the end of the original skill name. For example, Case summarization \(copy\). Changing the name to be more specific makes it easier to identify later if you want to make changes.

2.  Add a description for the skill.

3.  Go to the next step by selecting **Save and continue**.

4.  Choose the input fields and data sources for each input template.

    The default options are selected for you. Some options are read only. After you make any changes to the input template, you can save your work by selecting **Save template**.

    1.  Select an input template.

        The three default input templates are for new records, records that are in progress, and closed records.

    2.  Add the base input table fields by selecting **New base input field**, choosing a field, and entering a field description.

        Each base input table field requires a description. The description informs the large language model \(LLM\) what the field is for and how the information should be interpreted. The more information that you put in the description means that the model has more context for the data.

        ![Choose an input template, add the base table input fields, and use the save template button to save your work.](../image/na-record-summarization-input1.png)

    3.  Add or modify the rule conditions for the base table.

        The rule conditions determine when the input template is used. Record summarization is only available to the records that match the rule conditions of an input template.

        ![Add rule conditions to the base input table.](../image/na-record-summarization-input2.png)

    4.  Add additional input data sources by selecting **New data source** and choosing either **Related Table** or **Activity: Email**.

        Each related table is configured with input fields and descriptions. More specific descriptions for related tables help provide more context to the LLM. Activity fields, such as Email, don't have input fields that you can configure.

        ![Add additional input data sources such as related tables and activity fields.](../image/na-record-summarization-input3.png)

    5.  Add a filter condition to the related table.

        You can add more rule conditions to the related table. These rule conditions determine whether the data from the additional data source is incorporated into the summary. You can generate summaries on cases that don't match additional data source rule conditions as long as the base table rule conditions are met.

        ![Add extra rule conditions to the related table.](../image/na-record-summarization-input4.png)

5.  Select **Save and continue**.

6.  Choose prompt output sections to appear in summaries by moving a prompt section in the Available prompt sections list to the Final prompt sections list.

    You can reorder sections by dragging the boxes in the Final prompt sections list. Some input templates have sections that are marked with the lock icon \(![Lock icon.](../image/na-lock-icon.png)\). These sections must appear in the final summary, but you can still reorder them with any sections you have added.

    ![Add prompt output sections to the summary. The SLA has been added here.](../image/na-record-summarization-prompt1.png)

7.  In the Test response panel, select a record from the **Choose a record** field.

8.  Generate a summary for the chosen record by selecting **Run Test**.

    **Important:** Each time that you test your prompt output, the operation counts as an assist that is tracked by your Now Assist subscription. To track your Now Assist usage, [Monitoring Now Assist usage in Subscription Management](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

    Running multiple tests with different records can help ensure that you're satisfied with the results.

9.  Select **Save and continue**.

10. Choose when the skill is available by selecting either **Skill is always available** or **Customize skill availability**.

    If you choose **Customize skill availability**, you can use the condition builder to add conditions that restrict when the skill is available. For example, you could make the skill only available for certain assignment groups.

11. Select **Save and continue**.

12. Choose where you want record summarization to be available by selecting the toggle next to your preferred display option.

    You can select both in-product, Now Assist panel, or both.

    -   **In-product**: When selected, Now Assist skills are displayed on forms and workspaces.

        For the skills that appear in-product, select the down arrow to identify the roles that can use the skill.

    -   **Now Assist panel**: When selected, Now Assist skills are available in the Now Assist panel. If you don't see this option, you must activate the Now Assist panel. For more information, see [Activate the Now Assist panel standard chat](activate-now-assist-panel.md).

        For the skills that appear in the Now Assist panel, select the down arrow to identify the roles that can use the skill.

    You can add roles by entering the name of the role in the **User roles** field. You can remove existing roles by selecting the X icon in the role bubble. You must specify at least one role, but you can add as many roles as you like.

13. Select **Save and continue**.

14. Review your choices and select **Activate** to complete the configuration.


## Result

Your customized version of case or incident summarization is active on the instance.

## What to do next

Analyze your skill performance on the Now Assist Admin console to help determine the success of the new version of the skill. Learn more about tracking Now Assist usage at [Monitoring Now Assist usage in Subscription Management](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

**Parent Topic:**[Make a copy of a Now Assist skill](make-a-copy-of-a-now-assist-skill.md)

