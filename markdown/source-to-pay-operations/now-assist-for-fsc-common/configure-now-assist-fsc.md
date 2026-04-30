---
title: Configuring Now Assist for Common Finance and Supply Chain features
description: If you have the admin role, you can configure the Now Assist for Common Finance and Supply Chain features application so that your fulfillers can use the agentic AI skills in Source-to-Pay Workspace Workspace and Core UI.
locale: en-US
release: yokohama
product: Now Assist for FSC Common
classification: now-assist-for-fsc-common
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
keywords: [configuring generative AI for financial services operations, configuring generative AI for FSO]
breadcrumb: [Now Assist for Common Finance and Supply Chain features, Now Assist for Finance and Supply Chain, Finance and Supply Chain]
---

# Configuring Now Assist for Common Finance and Supply Chain features

If you have the admin role, you can configure the Now Assist for Common Finance and Supply Chain features application so that your fulfillers can use the agentic AI skills in Source-to-Pay Workspace Workspace and Core UI.

## Before you begin

Role required: admin

## About this task

Use the Now Assist Admin console to configure Now Assist for Common Finance and Supply Chain features. This console contains everything that you need to install the plugins and configure the agentic AI skills. For additional information, see [Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

The following table lists the Now Assist for Common Finance and Supply Chain features and skills that you can access from the Now Assist Admin console.

|Now Assist for SPO skills|Description|
|-------------------------|-----------|
|Purchase order summarization for fulfillers|Summarize purchase orders and keep fulfillers informed on their status, progress, and required actions.|

![Now Assist skills for Common Finance and Supply Chain features section, showing the Purchase order summarization for fulfillers feature card.](../image/now-assist-for-fsc.png "Now Assist skills for Common Finance and Supply Chain features")

## Procedure

1.  Install the Now Assist for FSC Common \(sn\_fsc\_genai\) plugin.

    -   For information about the plugin dependencies and plugin activation order, see [Supporting information for Now Assist for Common Finance and Supply Chain features](../concept/now-assist-fsc-supporting-info.md).
    -   For information about the installation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

3.  Expand the **Finance &amp; Supply Chain** workflow group and select **Common Finance and Supply Chain features**.

4.  Activate and configure the skills for Now Assist for Common Finance and Supply Chain features.

    |Skills|Action|
    |------|------|
    |Purchase order summarization for fulfillers|On the Purchase order summarization for fulfillers skill card, select **Activate skill** to activate the skill.|

5.  Select **General Details** and review the details about the skill and select **Save and continue** to go to the next step in the Guided Setup.

6.  Follow the steps to configure and activate a skill using the Guided Setup.

7.  Select **Choose input** and review the base input table and input fields, and then select **Save and continue** to go to the next step in the Guided Setup.

8.  Select **Customize and test prompt** to test the prompt on a record.

9.  Select **Save and continue** to go to the next step in the Guided Setup.

10. Select **Define Availability** and choose one of the following options.

<table id="choicetable_e25_bvj_1cc"><thead><tr><th align="left" id="d102801e337">

Option

</th><th align="left" id="d102801e340">

Description

</th></tr></thead><tbody><tr><td id="d102801e346">

**Skill is always available**

</td><td>

Skill is always available to users.

</td></tr><tr><td id="d102801e355">

**Customize skill availability**

</td><td>

The skill is available only when the certain conditions are met \(Default\).Use the condition builder to set your conditions.

</td></tr></tbody>
</table>11. Select **Save and continue** to go to the next step in the Guided Setup.

12. Choose **Select display** to determine where you'd like to display the skill.

<table id="choicetable_x1c_5b2_1cc"><thead><tr><th align="left" id="d102801e391">

Option

</th><th align="left" id="d102801e394">

Description

</th></tr></thead><tbody><tr><td id="d102801e400">

**In-product desktop**

</td><td>

The Purchase order summarization for fulfiller skillis displayed in the Source-to-Pay Workspace for Sourcing and Procurement Operations, Supplier Lifecycle Operations, and Accounts Payable Operations.

</td></tr><tr><td id="d102801e421">

**Now Assist panel**

</td><td>

Now Assist skills are available in the Now Assist panel. Turn on multi-language support for user-entered text with Dynamic Translation in Now Assist applications. For more information, see [Configure multilingual service for Now Assist applications](https://www.servicenow.com/docs/access?context=enable-dynamic-translation-for-now-assist-applications&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).**Note:** If you don't see this option, you must activate the Now Assist panel. For more information, see [Activate Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

</td></tr></tbody>
</table>13. Select **Save and continue** to go to the next step.

14. Review your choices and select **Activate** to complete the configuration for the skill.

15. Select **Return to Common Finance &amp; Supply Chain features**.

    The skill is activated.


-   **[Customize a Now Assist for Common Finance and Supply Chain features skill](cust-now-assist-fsc-skill.md)**  
If you have the admin role, you can customize a Now Assist for Sourcing and Procurement Operations \(SPO\) skill so that fulfillers and requesters can use the generative AI skills in Source-to-Pay Workspace, Shopping Hub, and in Core UI.
-   **[Skill inputs for Now Assist for Common Finance and Supply Chain features](../reference/input-triggers-now-assist-fsc.md)**  
You can configure some of the inputs for a generative AI skill. Inputs permit you to determine how and when a skill is used.
-   **[Customize supplier summarization for fulfillers skill](cust-na-fsc-supplier-skill.md)**  
If you have the admin role, you can customize the supplier summarization for fulfillers skill so that fulfillers can use the generative AI skills in Source-to-Pay Workspace to view relevant supplier information.

**Parent Topic:**[Now Assist for Common Finance and Supply Chain features](../concept/now-assist-fsc-common.md)

