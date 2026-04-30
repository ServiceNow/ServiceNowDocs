---
title: Configure resolution notes generation for Now Assist for HRSD
description: Configure the resolution notes generation skill to create concise summaries of case resolutions and enable agents to use the Now Assist context menu to elaborate or shorten the notes.
locale: en-US
release: yokohama
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2025-11-28"
reading_time_minutes: 3
breadcrumb: [Configure, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Configure resolution notes generation for Now Assist for HRSD

Configure the resolution notes generation skill to create concise summaries of case resolutions and enable agents to use the Now Assist context menu to elaborate or shorten the notes.

## Before you begin

Role required: sn\_hr\_core.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

2.  Select **Employee**, then select **HRSD**.

3.  Select **Activate skill** on the **Resolution notes generation** tile.

    Each skill has a guided setup with multiple steps. A check symbol next to each step indicates whether its setup is complete, partially complete, or incomplete. After configuring a step, select **Save and continue** to move forward, or **Back** to return to a previous step.

4.  Select the state in which the skill activates, then select **Save and continue**.

5.  Select **Choose Input** and review the tables and fields to define the prompts that determine where data is pulled from.

    You can modify the rule conditions to determine when the input template is used. Additional data sources can be added via related tables as well.

6.  NASK.

7.  Select **Define availability** to customize how and when the skill capability is active and accessible.

    -   Select **Skill is always available** so no restrictions are placed on when a skill is available.
    -   Select **Customize skill availability** to define conditions and use the condition builder to configure fields and values.
8.  Select **Define access** to determine who can access this skill.

9.  Select **Display** to determine where the skill appears.

    -   Select **In-product desktop** to display Now Assist skills on forms and workspaces. Then, select the roles for whom the skill will be displayed.
    -   Select **Now Assist panel** to display Now Assist skills in the Now Assist panel.
10. After selecting **Review and activate** to examine changes, select **Activate** to turn on the skill and complete the configuration.

11. In the Successfully activated pop-up window, select **Go to Now Assist context menu**.

12. Review the details.

13. Review the actions for the context menu trigger button and dialog.

14. In the Define access window, define who has access to the skill.

15. In the Select display window, enable **In-product desktop**.

16. Select **Review and activate** to examine changes, then select **Activate**.


**Parent Topic:**[Configure Now Assist for HR Service Delivery \(HRSD\)](configure-now-assist-hr.md)

**Related topics**  


[Skill inputs and triggers for Now Assist for HR Service Delivery \(HRSD\)](../concept/now-assist-hrsd-skill-inputs.md)

[RCA approvals for Now Assist for HR Service Delivery \(HRSD\)](run-rca-now-assist-hrsd.md)

[Restrict Now Assist capabilities for employee relations cases](restrict-now-assist-skills-er-cases.md)

[Configure sensitivity detection](config-na-sd-filters.md)

[Configure Gen AI Virtual Agent for HRSD](use-genai-ec.md)

[Configure the Now Assist for HRSD Virtual Agent topics](config-va-topics.md)

[Configure HCM agents for HR Service Delivery AI Agent Collection](configure-hcm-agents.md)

[Configure Now Assist AI Helper – Galileo Inside](configuring-galileo-inside.md)

