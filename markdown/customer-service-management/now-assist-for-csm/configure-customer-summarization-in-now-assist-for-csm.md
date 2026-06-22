---
title: Configure Customer summarization in Now Assist for CSM
description: Turn on the Customer summarization skill in Now Assist for CSM and configure user access and role restrictions to control who can use the skill and what data it can access.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/now-assist-for-csm/configure-customer-summarization-in-now-assist-for-csm.html
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-05-21"
reading_time_minutes: 2
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Activate Now Assist Skills, Configure, Now Assist for CSM, Customer Service Management]
---

# Configure Customer summarization in Now Assist for CSM

Turn on the Customer summarization skill in Now Assist for CSM and configure user access and role restrictions to control who can use the skill and what data it can access.

## Before you begin

Before turning on the Customer summarization skill, verify that the following prerequisites are met:

-   You have the admin role.
-   The Now Assist for Customer Service Management \(CSM\) plugin is activated in your instance.
-   A valid Now Assist for CSM license is applied to your instance.

Role required: admin

## About this task

When turning on the Customer summarization skill in CSM, you can specify who has access to the skill and add role restrictions to help avoid unauthorized data access.

## Procedure

1.  Navigate to **Admin** &gt; **Now Assist admin** &gt; **Skills**.

2.  Select the **Customer** workflow.

3.  Search for the **Customer summarization** skill.

4.  Select **Turn on**.

    The Turn on Customer summarization panel opens.

5.  Configure user access in the **Add user access** section.

    This section specifies the individuals or groups that can use the skill. ACLs \(access control lists\) identify the users permitted to access the skill.

    1.  Review the **Decision type** column.

        The value is set to **Allow if** by default.

    2.  Review the **Roles** column.

        By default, the following roles are assigned:

        -   `sn_customerservice.consumer_agent`
        -   `sn_customerservice_agent`
    3.  Edit the roles by selecting the pencil icon and updating the role assignments as needed.

6.  Set role restrictions for the skill in the **Role restrictions to skill** section.

    This section defines which data and resources, such as tables and APIs, the skill can access when invoked. These restrictions apply whenever the skill is triggered.

    1.  Review the roles listed under **Roles**.

        By default, the following roles are assigned:

        -   `sn_customerservice_agent`
        -   `sn_customerservice.consumer_agent`
    2.  Add or remove roles as required by your instance data access policy.

7.  Select **Turn on** to activate the Customer summarization skill.

    To discard your changes instead, select **Cancel**.


## Result

The Customer summarization skill is turned on. Agents can use the skill in the **Case insights** card. Role restrictions take effect after saving, controlling which users and data resources the skill can access.

## What to do next

-   Confirm that the skill status shows as **Active** on the skill card.
-   Test the summarization output on a sample record.
-   Notify Now Assist for CSM agents that the feature is available.
-   To customize the skill, go to Now Assist Skill Kit and open the skill and create custom prompts. For more info, see [Create a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/create-prompt-template.md)

