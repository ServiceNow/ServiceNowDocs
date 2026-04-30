---
title: Configure Now Assist for Legal Service Delivery \(LSD\)
description: If you have the admin role, you can configure the Now Assist for Legal Service Delivery \(LSD\) application so that legal users or request fulfillers can use the generative AI skills from Legal Counsel Center and Core UI.
locale: en-US
release: xanadu
product: Now Assist for Legal Service Delivery
classification: now-assist-for-legal-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
keywords: [Now Assist, generative AI]
breadcrumb: [Now Assist for Legal Service Delivery \(LSD\), Legal Service Delivery, Employee Service Management]
---

# Configure Now Assist for Legal Service Delivery \(LSD\)

If you have the admin role, you can configure the Now Assist for Legal Service Delivery \(LSD\) application so that legal users or request fulfillers can use the generative AI skills from Legal Counsel Center and Core UI.

## Before you begin

Ensure you have installed Legal Counsel Center \(sn\_lg\_cf\_workspace\) - Version 1.5.1 or a later version.

Role required: admin

## About this task

Use the Now Assist Admin console to configure the Now Assist for Legal Service Delivery \(LSD\) application. This console contains everything that you need to install the plugins and configure the generative AI skills. For additional information, see [Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

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
</table>The legal request summarization and legal matter summarization skills are available in the base system with the required configurations. To create a customized skill, you must create a copy of the skill that is in the base system before you modify the configuration. The parent skill is automatically deactivated when you activate your new customized skill. For more information, see [Customize a summarization skill in Now Assist for Legal Service Delivery \(LSD\)](../task/now-assist-lsd-customize-skill.md).

**Note:**

Now LLM Service is currently the only provider for this Now Assist application's skills.

## Procedure

1.  Install the Now Assist for Legal Service Delivery \(LSD\) plugin \(sn\_lg\_gen\_ai\).

    -   For information about the plugin dependencies and plugin activation order, see [Application information](now-assist-lsd-support-info.md#lsd-application-info).
    -   For information about the installation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

3.  Navigate to **Employee** &gt; **LSD**.

4.  On the tile for your skill, select **Activate skill**.

5.  In the General details step, view the fields.

6.  After viewing the details for the selected skill, select **Save and continue** to go to the next step.

7.  Customize the Now Assist context menu configuration.

    Customize the Now Assist context menu configuration to control which options should appear and how they are displayed in the Now Assist summarization.

    **Note:** Selecting the Enable Extended Tables check box applies the Now Assist context menu configuration to all the extended tables of the legal request and legal matter.

    For more information about the Now Assist context menu summarization, see .

8.  After you customize the Now Assist context menu, select **Save and continue** to go to the next step.

    You can return to a previous step by using the **Back** button.

9.  Select the inputs for the selected skill.

    For information about the inputs for each skill, see [Skill inputs for Now Assist for Legal Service Delivery \(LSD\)](now-assist-lsd-skill-inputs.md).![Choose input data screen for skills.](../image/lsd-na-lr-summary-skill-inputs.png)

10. After you configure the inputs for the selected skill, select **Save and continue** to go to the next step.

    You can return to a previous step by using the **Back** button.

11. Customize the prompt output.

    Review and test the prompt for each input template configuration.

12. After you customize the prompt output, select **Save and continue** to go to the next step.

    You can return to a previous step by using the **Back** button.

13. Define the availability of the skill.

    You can configure the skill to be always available to users or you can select the conditions that your users must meet before the skill is available. Selecting **Customize skill availability** displays a condition builder.

14. After you configure the skill availability, select **Save and continue** to go to the next step.

15. Select where you would like to display the skill.

<table id="choicetable_zsg_1gb_1dc"><thead><tr><th align="left" id="d391742e412">

Action

</th><th align="left" id="d391742e415">

Steps

</th></tr></thead><tbody><tr><td id="d391742e421">

**In-product**

</td><td>

When selected, the Now Assist skills are displayed on workspaces.For the skills that appear in-product, select the down arrow to identify the roles that can use the skill.

</td></tr><tr><td id="d391742e435">

**Now Assist panel**

</td><td>

When selected, the Now Assist skills are available in the Now Assist panel. If you don't see this option, you must activate the Now Assist panel. For more information, see [Turn on the Now Assist panel](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).For the skills that appear in the Now Assist panel, select the down arrow to identify the roles that can use the skill.

</td></tr></tbody>
</table>16. After you configure the display for the selected skill, select **Save and continue** to go to the next step.

17. Review your choices and select **Activate** to complete the configuration.

    Your skill is configured.

18. Configure the variables of the practice areas that you want to be considered as inputs for the legal request or matter summarization.

    For more information, see [Configure variables for Now Assist summarization](../task/configure-variables-for-now-assist-summarization.md).


