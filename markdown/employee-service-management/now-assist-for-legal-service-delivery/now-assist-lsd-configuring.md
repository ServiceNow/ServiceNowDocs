---
title: Configure Now Assist for Legal Service Delivery \(LSD\)
description: If you have the admin role, you can configure the Now Assist for Legal Service Delivery \(LSD\) application so that legal users or request fulfillers can use the generative AI skills from Legal Counsel Center, Core UI, and Employee Center.
locale: en-US
release: australia
product: Now Assist for Legal Service Delivery
classification: now-assist-for-legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, generative AI]
breadcrumb: [Now Assist for Legal Service Delivery \(LSD\), Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Configure Now Assist for Legal Service Delivery \(LSD\)

If you have the admin role, you can configure the Now Assist for Legal Service Delivery \(LSD\) application so that legal users or request fulfillers can use the generative AI skills from Legal Counsel Center, Core UI, and Employee Center.

## Before you begin

Confirm you have installed Legal Counsel Center \(sn\_lg\_cf\_workspace\) - Version 1.5.1 or a later version.

Role required: admin

## About this task

**Important:** These Now Assist skills are now turned on by default. The skills will be automatically available to appropriate role users for the application. This change simply activates the skills and does not touch the roles that are needed to use them. The new default behavior works as follows:

-   **New customers**

    When you install a Now Assist product, designated skills are turned on automatically.

-   **Existing customers who are upgrading \(starting with Zurich Patch 4\)**

    Any previously unconfigured skill is turned on automatically \(the skill was never turned on, then off again\).

    There is no change to Now Assist skills that are currently enabled and customized.

    Previously configured skills that were turned on, then off, remain inactive.


The legal request summarization and legal matter summarization skills are available in the base system with the required configurations. To customized the skill, you must create a copy of the skill that is in the base system before you modify the configuration. Activating a customized skill with the same base input table as the original skill automatically deactivates the original skill. For more information, see [Customize a summarization skill in Now Assist for Legal Service Delivery \(LSD\)](../task/now-assist-lsd-customize-skill.md).

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/exploring-large-language-models.md).

The following table lists the features and skills that you can access from the Now Assist Admin console.

<table id="table_ipf_bbd_wyb"><thead><tr><th>

LSD features

</th><th>

Skills

</th></tr></thead><tbody><tr><td>

Legal Request and Matter

</td><td>

-   Legal request summarization
-   Legal matter summarization

</td></tr></tbody>
</table>## Procedure

1.  Install the Legal Service Delivery - Prime plugin \(sn\_lg\_ai\_prime\).

    -   For information about the plugin dependencies and plugin activation order, see [Application information](now-assist-lsd-support-info.md#lsd-application-info).
    -   For information about the installation process, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).
2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

3.  Navigate to **Employee** &gt; **LSD**.

4.  On the tile for your skill, select **Activate skill** if it is deactivated.

    The Now Assist skill is activated.

5.  Define who can access the skilland the data.

    1.  Select **Edit** from the options icon \(![Options icon.](../../contract-mgmt-pro/image/cmpro-na-three-dot-icon.png)\) of the active skill.

    2.  Navigate to **Define access** to determine who can access the skill.

        By selecting specific roles, you're controlling who can use it. The roles you choose will also be available in the next step **Select display**.

        Default and Custom Roles:

        -   If custom roles were added before the upgrade, they’ll be updated automatically by a script.
        -   If new roles are created after the upgrade, you’ll need to manually add them in both the **Define Access** and **Select Display**.

            **Note:** In the **Select Display** step, you can only choose roles that were added in the **Define Access** step. If you add a role in **Define Access**, you still need to manually select it in **Select Display** to make it active.

    3.  In the **Role restrictions to skill** section, grant data access to additional roles.

        For more information, see [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-role-masking.md).

    4.  Select **Save and continue** to go to the next step.

    5.  Complete remaining configurations and select **Done**.


## Result

You can deactivate the skill by selecting **Deactivate** from the options icon \(![Options icon.](../../contract-mgmt-pro/image/cmpro-na-three-dot-icon.png)\) of the active skill.

