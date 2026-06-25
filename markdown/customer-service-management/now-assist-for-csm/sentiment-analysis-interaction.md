---
title: Sentiment analysis for email interactions
description: Configure Sentiment analysis for email interactions to evaluate sentiment, trends, and reasoning at interaction level and help agents resolve cases more efficiently.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/now-assist-for-csm/sentiment-analysis-interaction.html
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-03-23"
reading_time_minutes: 4
keywords: [Generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Activate Now Assist Skills, Configure, Now Assist for CSM, Customer Service Management]
---

# Sentiment analysis for email interactions

Configure Sentiment analysis for email interactions to evaluate sentiment, trends, and reasoning at interaction level and help agents resolve cases more efficiently.

## Before you begin

Role required: admin

Install the plugin for email interactions.

## About this task

Sentiment analysis for email interactions is generated from the information that you enter in the following fields:

-   Description
-   Short Description

Any modifications to the names or labels of these fields can result in issues with sentiment analysis. Sentiment is calculated using several factors:

-   Latest requester message
-   Overall conversation between agent and customer captured in transcript
-   Sentiment history \(trend\)
-   Issue complexity
-   Feedback or continued frustration at the end of conversation
-   Frequency of updates and response time
-   Language tone

The Sentiment Reasoning field in the record provides details on which factors were considered for reasoning. This includes:

-   Tone of the requester's messages across the transcript.
-   Feedback or continued frustration in the latest requester's messages.
-   Complexity of the issue based on interactions from both the requester and the agent.

## Procedure

1.  Navigate to **Admin &gt; Now Assist Admin &gt; Skills**.

2.  Select the **Customer** workflow, and **CSM** as the product.

3.  Activate skill for the **Sentiment analysis for email interactions** skill.

    Each skill has a guided setup with multiple steps. A check symbol next to each step indicates whether its setup is complete, partially complete, or incomplete. After configuring a step, select **Save and continue** to move forward, or **Back** to return to a previous step.

4.  Select **General details** and review the name and description of the skill.

    Additional information regarding details of the skill are displayed, but can't be edited.

5.  Select **Choose Input** and review the tables and fields to create prompts that determines where data is pulled from.

    **Note:** You cannot modify the input data source.

<table id="table_qrf_yz5_r3c"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Interaction

</td></tr><tr><td>

Input fields

</td><td>

-   Description
-   Short Description


</td></tr></tbody>
</table>6.  Select **Role attribution**

    **Note:** You cannot modify the input data source in base system.

<table id="table_dj3_lg5_r3c"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Interaction

</td></tr><tr><td>

Requester fields

</td><td>

-   Opened for
-   Created by


</td></tr><tr><td>

Fulfiller fields

</td><td>

Assigned to

</td></tr></tbody>
</table>7.  Select **Define Availability** to customize how and when the skill capability is active and accessible.

    -   Select **Skill is always available** so no restrictions are placed on when a skill is available.
    -   Select **Customize skill availability** to define conditions and use the condition builder to configure fields and values.
8.  Select **Define Trigger** and edit the job schedule frequency period to configure how often the skill will be triggered.

    To enable a scheduled job for a custom table, follow these steps:

    1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.
    2.  Search and select **Sentiment analysis scheduler job interaction CSM**.
    3.  Replace the table name **interaction** with the name of your custom table in the script.
    4.  Select **Update**.
9.  Select **Save and continue**.

10. Select **Define access** to determine who can access this skill.

    By selecting specific roles, you're controlling who can use it. The roles you choose will also be available in the next step **Select display**.

    Default and Custom Roles:

    -   If no changes are made, the default roles sn\_customerservice\_agent and sn\_customerservice.consumer\_agent will automatically appear in **Define Access** and **Select Display**.
    -   If custom roles were added before the upgrade, they’ll be updated automatically by a script.
    -   If new roles are created after the upgrade, you must manually add them in both the **Define Access** and **Select Display**.

        **Note:** In the **Select Display** step, you can only choose roles that were added in the **Define Access** step. If you add a role in **Define Access**, you still must manually select it in **Select Display** to make it active.

11. Select **Save and continue**.

12. **Select display** and toggle to determine if the skill appears in In-product desktop, displaying Sentiment analysis for email interactions in all CSM products.

13. Select **Save and continue**.

14. After selecting **Review and Activate** to examine changes, select **Done** to close the sentiment analysis generation settings.

15. Select **Activate** to turn on the skill for agents and complete the configuration.


## What to do next

-   Now Assist Skill Kit is the ServiceNow framework for [cloning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/clone-the-now-assist-for-csm-skills.md) and [customizing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/customizing-now-assist-skills.md) Now Assist skills. When configuring Sentiment Analysis for email interactions, the base table provides the core email record data. Additional inputs supply the LLM with broader context- such as email thread history, linked case fields, or customer contact data that can improve the accuracy of sentiment output.
-   You can customize the email sentiment prompt. Follow the steps to customize:
    1.  Access the OneExtend Capability Definition record by going to the sys\_generative\_ai\_config table. Here is an example for Azure OpenAI \(other providers like Claude and Gemini will have a different sys\_id\): https://anoway1.service-now.com/sys\_generative\_ai\_config.do?sys\_id=479cdabf93b48310003afba6dd03d606
    2.  Go to the **Prompt Template** field and edit the prompt.
    3.  **Save** the record.

        **Note:** Verify that the user is in Now Assist for Customer Service Management \(CSM\) scope and the record is still in **Published** state.


**Related topics**  


[Analyze sentiments in Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/analyze-sentiments-in-now-assist-for-csm.md)

[Enable and configure the Sentiment Analysis](https://support.servicenow.com/kb?sys_kb_id=ec531aab47a48794b6d8aa25126d4322&id=kb_article_view)

