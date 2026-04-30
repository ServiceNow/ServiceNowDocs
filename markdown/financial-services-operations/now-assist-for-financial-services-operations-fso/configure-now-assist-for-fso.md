---
title: Configure case summarization in Now Assist for Financial Services Operations \(FSO\)
description: If you have the admin role, you can configure the Now Assist for Financial Services Operations \(FSO\) application so that your agents can use case summarization skills in Financial Services Workspace and Core UI.
locale: en-US
release: zurich
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [configuring generative AI for financial services operations, configuring generative AI for FSO]
breadcrumb: [Configure, Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Configure case summarization in Now Assist for Financial Services Operations \(FSO\)

If you have the admin role, you can configure the Now Assist for Financial Services Operations \(FSO\) application so that your agents can use case summarization skills in Financial Services Workspace and Core UI.

## Before you begin

Role required: admin

## About this task

Use the Now Assist Admin console to configure Now Assist for FSO. This console contains what you need to install the plugins and configure the generative AI skills. For additional information, see [Overview tab in Now Assist Admin](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

The following table lists the case summarization skills that you can access from the Now Assist Admin console.

|Area|Skills|
|----|------|
|Banking|Dispute case summarization|
|Insurance|Claim case summarization|

**Note:**

Now LLM Service is currently the only provider for this Now Assist application's skills.

## Procedure

1.  Install the Now Assist for Financial Services Operations \(FSO\) plugin \(sn\_fso\_gen\_ai\).

    -   For information about the plugin dependencies and plugin activation order, see [Application information](../concept/supporting-information-for-now-assist-for-financial-services-operations-fso.md#section_ng1_bdj_mbc).
    -   For information about the installation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

3.  Select the **Customer** &gt; **FSO** workflow group.

4.  On the tile for your skill, select **Activate skill**.

5.  Review the inputs for the selected skill.

    The input table fields are read-only.

    For information about the inputs for each skill, see [Skill inputs for Now Assist for Financial Services Operations \(FSO\)](../concept/skill-inputs-and-triggers-for-now-assist-for-financial-services-operations-fso.md).

6.  After you review the inputs for the selected skill, select **Save and continue** to go to the next step.

    You can return to a previous step by using the **Back** button.

7.  Select where you would like to display the skill.

    -   **In-product**: When selected, the Now Assist skills are displayed on forms and workspaces.

        For the skills that appear in-product, select the down arrow to define the roles that can use the skill.

    -   **Now Assist panel**: When selected, the Now Assist skills are available in the Now Assist panel. If you don't see this option, you must activate the Now Assist panel. For more information, see [Activate the Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

        For the skills that appear in the Now Assist panel, select the down arrow to define the roles that can use the skill.

8.  After you configure the display for the selected skill, select **Save and continue** to go to the next step.

9.  Review your choices and select **Activate** to complete the configuration.


## Result

A message appears confirming the summarization skill has been successfully activated. Select **Return to Banking** to return to the Banking skills screen.

## What to do next

You can choose which service provider to use for this skill [in the Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

