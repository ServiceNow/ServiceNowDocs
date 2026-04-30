---
title: Tutorial: Automatically assign work to agents by skill
description: Learn how you can configure Advanced Work Assignment to automatically route cases to agents who speak German. Use this tutorial as a guideline to help you understand how you can route work items to agents according to their designated skills.Create a "German" skill.Create an assignment rule that routes cases according to skills.Create a queue where you can route work to agents who have the German skill.Define who is eligible to receive cases from the German Cases queue.Activate the skill determination business rule to tag skills for your work items.Create a skill determination rule to tag the German skill to incoming cases from German speakers.
locale: en-US
release: yokohama
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure agent assignment rules, Work assignments, Configure, Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Tutorial: Automatically assign work to agents by skill

Learn how you can configure Advanced Work Assignment to automatically route cases to agents who speak German. Use this tutorial as a guideline to help you understand how you can route work items to agents according to their designated skills.

Before you begin:

-   Activate the Skills Management \(com.snc.skills\_management\) plugin.
-   A basic understanding of the [Skills Management](../../../product/skills-management/reference/skills-management.md) feature is required.
-   To have skills automatically assigned to cases, consider activating the Skill Determination \(com.snc.skill\_determination\) plugin.
-   Create a group of users who work in customer support.
-   Assign the awa\_agent and workspace\_agent roles to the customer support group.

![Video link](../../conversational-interfaces/image/icon-video-link.png) [Advanced Work Assignment \(AWA\) Tutorial: Automatically assign work to agents by skill](https://www.youtube.com/watch?v=2epAFf8yAT0) Watch this video for a visual representation of the following tutorial example.

**Parent Topic:**[Configure agent assignment rules](../task/awa-create-assignment-rule.md)

## Create a skill

Create a "German" skill.

### Before you begin

Role required: skill\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **Skills** &gt; **All Skills**, and then click **New**.

2.  Enter the following information in the fields listed:

    -   **Name**: `German`
    -   **Active**: Selected
3.  Select **Submit**.


## Create an assignment rule that auto assigns agents' work

Create an assignment rule that routes cases according to skills.

### Before you begin

Role required: awa\_admin or admin

### Procedure

1.  Navigate to the assignment rules settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up assignment rules**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Assignment Rules**.
2.  Select **New**.

3.  Enter the following information in the fields listed:

    -   **Name**: `Case Assignment Rule with Skills`
    -   **Assign by**: `Most Capacity`
    -   **Enable auto-assign work items**: Selected

        **Note:** Selecting this option automatically accepts chat interactions on behalf of agents. The **Display options** field appears and you can select either **Inbox card** or **Inbox card and workspace tab**.

    -   **Enable skills**: Selected
    -   **Evaluate skill level**: Cleared
    -   **Enforce mandatory skills**: Selected
4.  Select **Submit**.


## Create a queue

Create a queue where you can route work to agents who have the German skill.

### Before you begin

Role required: awa\_admin or admin

### Procedure

1.  Navigate to the queue settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up queues**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Queues**.
2.  Select **New**.

3.  Enter the following information in the fields listed:

    -   **Name**: `German Case Queue`
    -   **Service channel**: `Case`
4.  Select **Submit**.


## Define assignment eligibility

Define who is eligible to receive cases from the German Cases queue.

### Before you begin

Role required: awa\_admin or admin

### Procedure

1.  Navigate to the queue settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up queues**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Queues**.
2.  Select the German Cases queue.

3.  On the form, go to the Assignment Eligibility related link and select **New**.

4.  In the **Agent assignment rule** field, select **Case Assignment Rule with Skills**.

5.  In the **Groups** field, select your customer support group.

6.  Select **Submit**.


## Enable skill determination

Activate the skill determination business rule to tag skills for your work items.

### Before you begin

Role required: awa\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **System Definitions** &gt; **Business Rules**.

2.  Select the **Skill determination for cases** record.

3.  On the form, select the **Active** field.

4.  Select **Update**.


## Define a skill determination rule

Create a skill determination rule to tag the German skill to incoming cases from German speakers.

### Before you begin

Role required: awa\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **Skills** &gt; **Skill Determination Rules**, and then select **New**.

2.  Enter the following information in the fields listed:

    -   **Name**: `Skill determination for German cases`
    -   **Active**: `true`
    -   **Source table**: **Case \[sn\_customerservice\_case\]**
    -   **Condition**: **Opened by.language is German**

        **Note:** Search for the `Show related fields` option when defining the conditions to get the Opened by.language option.

    -   **Skills**: German
3.  Select **Submit**.


### Result

Cases that need German speakers are routed to users in Customer Service and Support who have the German skill.

