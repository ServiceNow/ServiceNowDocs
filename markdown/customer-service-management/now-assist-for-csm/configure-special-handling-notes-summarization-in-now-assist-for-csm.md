---
title: Configure special handling notes summarization in Now Assist for Customer Service Management \(CSM\)
description: Activate the Special Handling Notes summarization skill to enable Now Assist for CSM to generate concise summaries of special handling notes on the Case Insights section.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/now-assist-for-csm/configure-special-handling-notes-summarization-in-now-assist-for-csm.html
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-05-21"
reading_time_minutes: 2
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Activate Now Assist Skills, Configure, Now Assist for CSM, Customer Service Management]
---

# Configure special handling notes summarization in Now Assist for Customer Service Management \(CSM\)

Activate the Special Handling Notes summarization skill to enable Now Assist for CSM to generate concise summaries of special handling notes on the **Case Insights** section.

## Before you begin

-   The Now Assist for Customer Service Management \(CSM\) plugin is activated in your instance.
-   A valid Now Assist license is applied to your instance.

Role required: admin.

## About this task

The Special Handling Notes summarization skill uses generative AI to condense lengthy or multiple special handling notes on a customer into a brief, actionable summary. When activated, agents can view this summary directly on the **Case Insights** section, which helps agents understand customer-specific handling requirements before engaging with a customer.

## Procedure

1.  Navigate to **Admin** &gt; **Now Assist admin** &gt; **Skills**.

2.  Select the **Customer** workflow and **CSM** as the product.

3.  Search for the **Special handling notes summarization** skill.

4.  Select **Turn on**.

    The **Turn on Special Handling notes** panel opens.

5.  Configure user access.

    In the **Add user access** section, specify the individuals or groups that can use this skill. ACLs \(access control lists\) identify the users permitted to access the skill.

    1.  Review the **Decision type** column.

        The value is set to **Allow if** by default.

    2.  Review the **Roles** column.

        By default, the following roles are assigned:

        -   `sn_customerservice.consumer_agent`
        -   `sn_customerservice_agent`
    3.  To edit the roles, select the pencil icon at the end of the row and update the role assignments as needed.

6.  Set role restrictions for the skill.

    In the **Role restrictions to skill** section, define which data and resources \(for example, tables and APIs\) the skill can access when invoked. These restrictions apply whenever the skill is triggered.

    1.  Review the roles listed under **Roles**.

        By default, the following roles are populated:

        -   `sn_customerservice_agent`
        -   `sn_customerservice.consumer_agent`
    2.  Add or remove roles as required by your instance data access policy.

7.  Select **Turn on** to activate the Special handling notes summarization skill.


## Result

The Special Handling Notes summarization skill is activated. Agents working in the CSM Configurable Workspace can view AI-generated summaries of special handling notes on the **Case Insights** section, which supports more consistent customer interactions. Role restrictions control which users and data resources the skill can access.

## What to do next

After activating the skill, complete the following tasks:

-   Test the summarization output on a sample record that contains multiple or lengthy special handling notes.
-   Notify CSM agents that the feature is available and direct them to the **Case Insights** section to review summaries.
-   Monitor Now Assist usage analytics to track adoption of the skill.
-   To customize the skill, go to Now Assist Skill Kit and open the skill and create custom prompts. For more info, see 

