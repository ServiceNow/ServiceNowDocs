---
title: Configuring Now Assist for Financial Services Operations \(FSO\)
description: If you have the admin role, you can configure the Now Assist for Financial Services Operations \(FSO\) application so that your agents can use the generative AI skills in Financial Services Workspace and Core UI.
locale: en-US
release: xanadu
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
keywords: [configuring generative AI for financial services operations, configuring generative AI for FSO]
breadcrumb: [Now Assist for Financial Services Operations \(FSO\), Financial Services Operations \(FSO\)]
---

# Configuring Now Assist for Financial Services Operations \(FSO\)

If you have the admin role, you can configure the Now Assist for Financial Services Operations \(FSO\) application so that your agents can use the generative AI skills in Financial Services Workspace and Core UI.

## Before you begin

Role required: admin

## About this task

Use the Now Assist Admin console to configure Now Assist for FSO. This console contains everything that you need to install the plugins and configure the generative AI skills. For additional information, see [Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

The following table lists the features and skills that you can access from the Now Assist Admin console.

|Area|Skills|
|----|------|
|Banking|Dispute case summarization|
|Insurance|Claim case summarization|

**Note:**

Now LLM Service is currently the only provider for this Now Assist application's skills.

## Procedure

1.  Install the Now Assist for Financial Services Operations \(FSO\) plugin \(sn\_fso\_gen\_ai\).

    -   For information about the plugin dependencies and plugin activation order, see [Application information](../concept/supporting-information-for-now-assist-for-financial-services-operations-fso.md#section_ng1_bdj_mbc).
    -   For information about the installation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Features** to access the **Now Assist Features** tab of the Now Assist Admin console.

3.  Select the **Customer** workflow group.

4.  In the **Select product** drop-down list, select **FSO**.

    ![Now Assist for FSO skills are in the Customer workflow group. Selecting FSO in the Select product drop-down list displays the available skills.](../image/now-assist-fso-select-product.png)

5.  On the feature card that is associated with the skill you would like to activate, select **View details**.

6.  In the All available skills section, select **Activate skill**.

7.  Review the inputs for the selected skill.

    The input table fields are read-only.

    For information about the inputs for each skill, see [Skill inputs for Now Assist for Financial Services Operations \(FSO\)](../concept/skill-inputs-and-triggers-for-now-assist-for-financial-services-operations-fso.md).

8.  After you review the inputs for the selected skill, select **Save and continue** to go to the next step.

    You can return to a previous step by using the **Back** button.

9.  Select where you would like to display the skill.

    -   **In-product**: When selected, the Now Assist skills are displayed on forms and workspaces.

        For the skills that appear in-product, select the down arrow to identify the roles that can use the skill.

    -   **Now Assist panel**: When selected, Now Assist skills are available in the Now Assist panel. If you don't see this option, you must activate the Now Assist panel. For more information, see [Turn on the Now Assist panel](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

        For the skills that appear in the Now Assist panel, select the down arrow to identify the roles that can use the skill.

10. After you configure the display for the selected skill, select **Save and continue** to go to the next step.

11. Review your choices and select **Activate** to complete the configuration.

    Your skill is configured.


## What to do next

Configure security for your configured Now Assist for FSO skills. See [Configuring security](configuring-security-in-now-assist-for-fso.md) for more information.

