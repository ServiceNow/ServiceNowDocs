---
title: Configure Activity Response Generation for HR Case
description: Set up the activity response generation skill in the AI Admin Hub console to enable automated responses in comments and work notes of an HR case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-activity.html
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2026-07-15"
reading_time_minutes: 2
breadcrumb: [Configure, ServiceNow Otto for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Configure Activity Response Generation for HR Case

Set up the activity response generation skill in the AI Admin Hub console to enable automated responses in comments and work notes of an HR case.

## Before you begin

Role required: sn\_hr\_core.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

2.  Select the **Employee** workflow, then select **HRSD**.

    This determines the product context for the skill. Workflow and product must match your configuration requirements.

3.  Select **Activate skill** on the Activity Response Generation for HR case skill.

    Each skill has a guided setup with multiple steps. A check symbol next to each step indicates whether its setup is complete, partially complete, or incomplete. After configuring a step, select **Save and continue** to move forward, or **Back** to return to the previous step.

4.  Select **General details** and edit name and description of the skill.

    Additional information regarding details of the skill are displayed, but can't be edited.

5.  Select **Choose Inputs** and review the input tables and fields to define the prompts that determine where data is pulled from.

    |Input|Description|
    |-----|-----------|
    |Input table|HR case|
    |Input fields|Description, Short Description, Additional comments, Work notes, State, Priority.|

6.  Select **Define availability** to customize how and when the skill capability is active and accessible.

    -   Select **Skill is always available** so no restrictions are placed on when a skill is available.
    -   Select **Customize skill availability** to define conditions and use the condition builder to configure fields and values.
7.  Select **Define access** to determine who can access this skill.

    By selecting specific roles, you’re controlling who can use it. The roles you choose will also be available in the next step Select display.

    Default and Custom Roles:

    -   If no changes are made, the default role sn\_hr\_core.case\_writer automatically appears in Define Access and Select Display.
    -   If custom roles were added before the upgrade, they’re updated automatically by a script.
    -   If new roles are created after the upgrade, you can manually add them in both the Define Access and Select Display.

        **Note:** In the Select Display step, you can only choose roles that were added in the Define Access step. If you add a role in Define Access, you still must manually select it in Select Display to make it active.

8.  In the Select display step, determine where the skill appears.

    Select In-product desktop to display activity response generation for HR case in all HRSD products. Then, select the roles for whom the skill will be displayed.

9.  After selecting **Review and activate** to examine changes, select **Activate** to turn on the skill and complete the configuration.

10. Select **Done**.


-   **[Configuring the Now Assist Context Menu for HR Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/customize-now-context-hrsd.md)**  
Customize a Now Assist skill so that agents can use the generative AI skills in HR Agent Workspace and Core UI.

**Parent Topic:**[Configure ServiceNow Otto for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/configure-now-assist-hr.md)

