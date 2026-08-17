---
title: Configure ServiceNow Otto for Collaborative Work Management \(CWM\) \(CWM\)
description: If you have the admin role, you can configure the implementation for the ServiceNow Otto for CWM application. This lets your team members utilize generative AI skills in the CWM workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-business-management/now-assist-for-collaborative-work-management-cwm/configure-now-assist-for-collaborative-work-management.html
release: yokohama
product: Now Assist for Collaborative Work Management \(CWM\)
classification: now-assist-for-collaborative-work-management-cwm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Now Assist for CWM, Strategic Portfolio Management]
---

# Configure ServiceNow Otto for Collaborative Work Management \(CWM\) \(CWM\)

If you have the admin role, you can configure the implementation for the ServiceNow Otto for CWM application. This lets your team members utilize generative AI skills in the CWM workspace.

## Before you begin

-   The minimum version of CWM application that is required to support ServiceNow Otto for CWM features is v6.0.0 and later. If you're on earlier versions, upgrade your app through Application Manager. See [Update an application or plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/update-application-app-mgr.md).
-   Install the ServiceNow Otto for Collaborative Work Management \(CWM\) \(CWM\) plugin \(sn\_cwm\_ai\). See [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).
-   [Activate Now Assist panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/activate-now-assist-panel.md).

Role required: admin

## About this task

Use the AI Admin Hub console to configure ServiceNow Otto for SPM. All ServiceNow Otto for SPM skills are activated by default. If a skill isn't automatically activated or you want to update its configuration, follow the steps below.

Use the AI Admin Hub console to activate the following skills of ServiceNow Otto for CWM.

-   CWM Doc generation and insights
-   Acceptance criteria generation
-   Tasks generation

**Note:** Now LLM Service is the default provider for this Now Assist application's skills.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

    The **Now Assist Skills** tab of the AI Admin Hub console is displayed.

2.  From the **Technology** grouping, select **CWM**.

    The skills for CWM are displayed as tiles.

3.  For the skill that you want to activate, select **Activate skill**.

4.  Review the skill configuration settings from the following sections.

    To edit the inputs, switch your application scope to **Now Assist for Collaborative Work Management \(CWM\)**. For more information on these inputs, see .

    **Note:** The display options are available based on the skill.

    1.  Choose inputs: These are the skill settings for summarizing and refining selected content within a CWM Doc page.

        This section is not available for the Tasks generation skill.

    2.  Select **Save and continue**.
    3.  Define access: Review who has access to skills.
        -   Configure ACLs or role-based permissions to ensure who can view or edit the skills.
        -   Review role restrictions to skill.
    4.  Page inputs: These are the skill settings for summarizing the whole content of a CWM Doc page.
    5.  Select **Save and continue**.
    6.  Select display:
        -   In-product desktop: Enabling this option shows the skill within the CWM workspace.
        -   Now Assist panel: Enabling this option shows the skill within the Now Assist panel.
        -   Now Assist context menu: Enabling this option shows the skill within a form field in the CWM workspace.
    7.  Select **Save and continue**.
    8.  Review and activate: Review your selections for the skill.
5.  Select **Activate**.


## Result

The skill is successfully activated.

## What to do next

Return to the CWM skill grouping and repeat the process to activate any remaining skills.

If you have custom roles that require access to a skill, update the ACLs for those roles that require access. For more information, see [Implement access control in Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/aia-security-implementation.md).

**Related topics**  


[Supporting information for ServiceNow Otto for Collaborative Work Management \(CWM\) \(CWM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/now-assist-for-collaborative-work-management-cwm/supporting-information-now-assist-for-cwm.md)

[skill-inputs-now-assist-for-cwm]

