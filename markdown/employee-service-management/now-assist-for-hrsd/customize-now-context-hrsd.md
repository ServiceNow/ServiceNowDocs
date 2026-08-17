---
title: Configuring the Now Assist Context Menu for HR Service Delivery
description: Customize a Now Assist skill so that agents can use the generative AI skills in HR Agent Workspace and Core UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/now-assist-for-hrsd/customize-now-context-hrsd.html
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2026-07-16"
reading_time_minutes: 3
breadcrumb: [Configure Activity Response Generation for HR Case, Configure, ServiceNow Otto for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Configuring the Now Assist Context Menu for HR Service Delivery

Customize a Now Assist skill so that agents can use the generative AI skills in HR Agent Workspace and Core UI.

## Before you begin

Role required: sn\_hr\_core.admin

## About this task

The Now Assist context menu configuration is accessible through the Now Assist Experiences in Now Assist Admin console. After activating the relevant skills, users are prompted to visit the NACM Config for HR Case ARG. However, in the base system, configuration is already active. By default, it is configured to use extended tables for activity response generation skill that is provided in the base system. NACM Config for HR Case ARG is currently available only for activity response generation skill.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Experiences**.

2.  Select Now Assist context menu.

3.  Open the Configuration tab to view all the existing configurations.

4.  Find the configuration name NACM Config for HR Case ARG.

5.  Select Edit configuration.

6.  In the guided setup, go to General details step.

    1.  In the Name field, provide a customized name for the table.

    2.  In the Where do you want to trigger the context menu? option, select the Record form fields for table form use cases.

        The form fields are active for work notes and additional comments.

    Each experience has a guided setup with multiple steps. A check symbol next to each step indicates whether its setup is complete, partially complete, or incomplete. After configuring a step, select **Save and continue** to move forward, or **Back** to return to the previous step.

7.  In the Configure Experience step, configure the actions for the context menu trigger button and dialog.

    There are separate configurations for Work notes and Additional comments.

    1.  In the Trigger section, select the default action to generate automated responses when users selects the trigger for the first time without selecting any content.
    2.  In the Dialog section, select the refinement actions that act as follow-up actions that the users can take after the content is generated. For example Shorten, and Elaborate.
    3.  In the Actions for generated content, select actions that can be applied to the generated content to meet the user's specific needs.

        In the Preview you can see how the Now Assist context menu button will look like after configuration.

        By default, the Enable support for extended tables toggle is turned on and this configuration is shipped as active in the base system. This is to support sparkle on extended table on same field. Once the skill is active, this experience is available.

8.  In the Define access step, select the roles who can access this skill.

    By selecting specific roles, you're controlling who can use it. The roles you choose will also be available in the next step Select display.

    Default and Custom Roles:

    -   If no changes are made, the default role sn\_hr\_core.case\_writer will automatically appear in Define Access and Select Display.
    -   If custom roles were added before the upgrade, they are updated automatically by a script.
    -   If new roles are created after the upgrade, you can manually add them in both the Define Access and Select Display.

        **Note:** In the Select Display step, you can only choose roles that were added in the Define Access step. If you add a role in Define Access, you still must manually select it in Select Display to make it active.

9.  In the Select Display step, determine where to display the NACM Config for HR Case ARG.

    -   Select In-product desktop to show Case NACM Config for HR Case ARG in HR Agent Workspace and Core UI.
    -   Select roles for whom NACM Config for HR Case ARG will be displayed.
10. In Review and Activate step, select a record with the specific usage conditions from the drop down to test the configuration.

    1.  Select **Preview** to view the final output of the configuration.

    2.  Select **Activate** to activate Now Assist context menu for the skill.

    The Now Assist context menu has been successfully activated.

11. Select **Done**.


**Parent Topic:**[Configure Activity Response Generation for HR Case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-activity.md)

