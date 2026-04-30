---
title: Configure Now Assist for Collaborative Work Management \(CWM\)
description: If you have the admin role, you can configure the implementation for the Now Assist for CWM application so that your team members can utilize generative AI skills in the CWM workspace.
locale: en-US
release: xanadu
product: Now Assist for Collaborative Work Management \(CWM\)
classification: now-assist-for-collaborative-work-management-cwm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Now Assist for CWM, Strategic Portfolio Management]
---

# Configure Now Assist for Collaborative Work Management \(CWM\)

If you have the admin role, you can configure the implementation for the Now Assist for CWM application so that your team members can utilize generative AI skills in the CWM workspace.

## Before you begin

-   The minimum version of CWM application that is required to support Now Assist for CWM features is v6.0.0 and later. If you're on earlier versions, upgrade your app through Application Manager. See [Update an application or plugin](https://www.servicenow.com/docs/access?context=update-application-app-mgr&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
-   Install the Now Assist for Collaborative Work Management \(CWM\) plugin \(sn\_cwm\_ai\). See [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
-   [Turn on the Now Assist panel](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

Role required: admin

## About this task

Use the Now Assist Admin console to activate the following skills of Now Assist for CWM.

-   Docs summarization in Collaborative Work Management
-   Tasks generation

**Note:** Now LLM Service is the default provider for this Now Assist application's skills.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

    The **Now Assist Skills** tab of the Now Assist Admin console is displayed.

2.  From the **Technology** grouping, select **CWM**.

    The skills for CWM are displayed as tiles.

3.  For the skill that you want to activate, select **Activate skill**.

4.  Review the skill configuration settings from the following sections.

    -   Choose inputs: These are the skill settings for summarizing and refining selected content within a CWM Doc page.

        This section is not available for the Tasks generation skill.

    -   Select **Save and continue**.
    -   Page inputs: These are the skill settings for summarizing the whole content of a CWM Doc page.

        This section is not available for the Tasks generation skill.

        To edit the inputs, switch your application scope to **Now Assist for Collaborative Work Management \(CWM\)**.

    -   Select **Save and continue**.
    -   Select display:

        -   **In-product desktop**: Enabling this option shows the skill within the CWM workspace.
        -   **Now Assist panel**: Enabling this option shows the skill within the Now Assist panel.
        **Note:** The display options are available based on the skill.

    -   Select **Save and continue**.
    -   Review and activate: Review your selections for the skill.
5.  Select **Activate**.


## Result

The skill is successfully activated.

## What to do next

Return to the CWM skill grouping and repeat the process to activate any remaining skills.

**Related topics**  


[Supporting information for Now Assist for Collaborative Work Management \(CWM\)](../reference/supporting-information-now-assist-for-cwm.md)

[skill-inputs-now-assist-for-cwm]

