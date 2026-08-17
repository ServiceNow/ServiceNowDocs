---
title: Configuring ServiceNow Otto for Finance and Procurement
description: If you have the admin role, you can configure the ServiceNow Otto for Finance and Procurement application so that your fulfillers can use the agentic AI skills in Source-to-Pay Workspace Workspace and Core UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/now-assist-for-fsc-common/configure-now-assist-fsc.html
release: zurich
product: Now Assist for FSC Common
classification: now-assist-for-fsc-common
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [configuring generative AI for financial services operations, configuring generative AI for FSO]
breadcrumb: [ServiceNow Otto for Finance and Procurement, ServiceNow Otto applications for Finance and Supply Chain, Finance and Supply Chain]
---

# Configuring ServiceNow Otto for Finance and Procurement

If you have the admin role, you can configure the ServiceNow Otto for Finance and Procurement application so that your fulfillers can use the agentic AI skills in Source-to-Pay Workspace Workspace and Core UI.

## Before you begin

Role required: admin

## About this task

Use the AI Admin Hub to configure ServiceNow Otto for Finance and Procurement. This console contains everything that you need to install the plugins and configure the agentic AI skills. For additional information, see [Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-now-assist.md).

The following table lists the ServiceNow Otto for Finance and Procurement and skills that you can access from the AI Admin Hub.

|ServiceNow Otto for SPO skills|Description|
|------------------------------|-----------|
|Supplier summarization for fulfillers|Summarize supplier details and keep fulfillers informed about their overview, total spends, and performance.|
|Purchase order summarization for fulfillers|Summarize purchase orders and keep fulfillers informed on their status, progress, and required actions.|

\[Omitted image "now-assist-for-fsc.png"\] Alt text: AI skills for Common Finance and Supply Chain features section, showing the Purchase order summarization for fulfillers feature card.

## Procedure

1.  Install the ServiceNow Otto for Finance and Procurement \(sn\_fsc\_genai\) plugin.

    -   For information about the plugin dependencies and plugin activation order, see [Supporting information for ServiceNow Otto for Finance and Procurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/now-assist-for-fsc-common/now-assist-fsc-supporting-info.md).
    -   For information about the installation process, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).
2.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Skills**.

3.  Select the **AI Skills** tab.

4.  Expand the **Finance &amp; Supply Chain** workflow group and select **Common Finance and Supply Chain features**.

5.  Activate and configure the AI skills for Common Finance and Supply Chain features.

    |Skills|Action|
    |------|------|
    |Supplier summarization for fulfillers|Summarize supplier details and keep fulfillers informed about their overview, total spends, and performance.|
    |Purchase order summarization for fulfillers|On the Purchase order summarization for fulfillers skill card, select **Activate skill** to activate the skill.|

6.  Select **General Details** and review the details about the skill and select **Save and continue** to go to the next step in the Guided Setup.

7.  Follow the steps to configure and activate a skill using the Guided Setup.

8.  Select **Choose input** and review the base input table and input fields, and then select **Save and continue** to go to the next step in the Guided Setup.

9.  Select **Customize and test prompt** to test the prompt on a record.

10. Select **Save and continue** to go to the next step in the Guided Setup.

11. Select **Define Availability** and choose one of the following options.

<table id="choicetable_e25_bvj_1cc"><thead><tr><th align="left" id="d119657e370">

Option

</th><th align="left" id="d119657e373">

Description

</th></tr></thead><tbody><tr><td id="d119657e379">

**Skill is always available**

</td><td>

Skill is always available to users.

</td></tr><tr><td id="d119657e388">

**Customize skill availability**

</td><td>

The skill is available only when the certain conditions are met \(Default\).Use the condition builder to set your conditions.

</td></tr></tbody>
</table>12. Select **Save and continue** to go to the next step in the Guided Setup.

13. Choose **Select display** to determine where you'd like to display the skill.

<table id="choicetable_x1c_5b2_1cc"><thead><tr><th align="left" id="d119657e424">

Option

</th><th align="left" id="d119657e427">

Description

</th></tr></thead><tbody><tr><td id="d119657e433">

**In-product desktop**

</td><td>

The Purchase order summarization for fulfiller skillis displayed in the Source-to-Pay Workspace for Sourcing and Procurement Operations, Supplier Lifecycle Operations, and Accounts Payable Operations.

</td></tr><tr><td id="d119657e454">

**ServiceNow Otto panel**

</td><td>

AI skills are available in the ServiceNow Otto panel. Turn on multi-language support for user-entered text with Dynamic Translation in ServiceNow Otto applications. For more information, see [Configure multilingual service for Now Assist applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/enable-dynamic-translation-for-now-assist-applications.md).**Note:** If you don't see this option, you must activate the ServiceNow Otto panel. For more information, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/activate-now-assist-panel.md).

</td></tr></tbody>
</table>14. Select **Save and continue** to go to the next step.

15. Review your choices and select **Activate** to complete the configuration for the skill.

16. Select **Return to Common Finance &amp; Supply Chain features**.

    The skill is activated.


-   **[Customize a generative AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/now-assist-for-fsc-common/cust-now-assist-fsc-skill.md)**  
If you have the admin role, you can customize a ServiceNow Otto for Sourcing and Procurement Operations \(SPO\) skill so that fulfillers and requesters can use the generative AI skills in Source-to-Pay Workspace, Shopping Hub, and in Core UI.
-   **[Customize supplier summarization for fulfillers skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/now-assist-for-fsc-common/cust-na-fsc-supplier-skill.md)**  
If you have the admin role, you can customize the supplier summarization for fulfillers skill so that fulfillers can use the generative AI skills in Source-to-Pay Workspace to view relevant supplier information.

**Parent Topic:**[ServiceNow Otto for Finance and Procurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/now-assist-for-fsc-common/now-assist-fsc-common.md)

**Related topics**  


[Configure ServiceNow Otto for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/configure-now-assist-for-spo.md)

[Configure ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo-configuring.md)

[Configure ServiceNow Otto for Accounts Payable Operations \(APO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/configuring-now-assist-apo.md)

