---
title: Configure Disputes intake via Virtual Agent in Now Assist for Financial Services Operations \(FSO\)
description: If you have the admin role, you can configure Disputes intake via Virtual Agent in Now Assist for Financial Services Operations \(FSO\). This provides a conversational experience for your customers to submit card disputes.
locale: en-US
release: yokohama
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Now Assist for FSO, Now Assist for Financial Services Operations \(FSO\)]
---

# Configure Disputes intake via Virtual Agent in Now Assist for Financial Services Operations \(FSO\)

If you have the admin role, you can configure Disputes intake via Virtual Agent in Now Assist for Financial Services Operations \(FSO\). This provides a conversational experience for your customers to submit card disputes.

## Before you begin

Confirm that Financial Services Card Operations \(sn\_bom\_credit\_card\) is installed on your instance.

Role required: admin

## About this task

Use the Now Assist Admin console to configure Now Assist for FSO. This console contains what you need to install the plugins and configure the generative AI skills. For additional information, see [Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

**Note:**

Now LLM Service is currently the only provider for this Now Assist application's skills.

## Procedure

1.  Install the Now Assist for Financial Services Operations \(FSO\) plugin \(sn\_fso\_gen\_ai\).

    -   For information about the plugin dependencies and plugin activation order, see [Application information](../../fso-common/concept/supporting-information-for-now-assist-for-financial-services-operations-fso.md#section_ng1_bdj_mbc).
    -   For information about the installation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

3.  Select the **Customer** &gt; **FSO** workflow group.

4.  In the Banking section, select **View details**.

    ![Disputes intake via Virtual Agent is in the Customer > FSO workflow group, under the Banking section.](../image/now-assist-skills-fso-va.png)

5.  In the All available Banking skills section, in the Disputes intake via Virtual Agent skill panel, select **Conversational Experience**.

    Conversational experience will open in a new browser.

    ![Select Conversational Experience before activating the Disputes intake via Virtual Agent skill.](../image/disputes-va-conv-exp.png)

6.  In **Conversational experience** &gt; **Now Assist skills**, activate **Now Assist Topics**.

    **Note:** Disputes intake via Virtual Agent requires Now Assist Topics to function. You may activate the other Conversational experience skills if desired.

    In this setup, you can also define where the Virtual Agent is displayed, the chat window branding, chat experience, and so on. For more information, see [Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

7.  Return to the Banking browser window.

8.  In the Disputes intake via Virtual Agent skill tile, select **Activate skill**.

    ![Select Activate skill for Disputes intake via Virtual Agent to activate the skill.](../image/now-assist-fso-activate-disputes-intake-va.png)


## Result

A window displays confirming that the Disputes intake via Virtual Agent skill is active for Now Assist for FSO.

![A window displays to confirm that Disputes intake via Virtual Agent is active.](../image/now-assist-fso-disputes-intake-va-activated.png)

## What to do next

Select **Setup Conversational Experience** to review the configuration for Disputes intake via Virtual Agent.

Select **Return to Banking** to return to the Banking skills page.

You can choose which service provider to use for this skill [in the Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

