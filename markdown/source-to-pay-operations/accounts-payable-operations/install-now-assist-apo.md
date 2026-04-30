---
title: Install Now Assist for Accounts Payable Operations \(APO\)
description: Install the APO plugin \[sn\_ap\_gen\_ai\] so that an accounts payable \(AP\) fulfiller can use the generative AI skills in Source-to-Pay Workspace and in Core UI.
locale: en-US
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure Now Assist for Accounts Payable Operations \(APO\), Now Assist for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# Install Now Assist for Accounts Payable Operations \(APO\)

Install the APO plugin \[sn\_ap\_gen\_ai\] so that an accounts payable \(AP\) fulfiller can use the generative AI skills in Source-to-Pay Workspace and in Core UI.

## Before you begin

Role required: admin

Install the Document Intelligence for Accounts Payable Operations Content Pack from the ServiceNow® Store for the invoice data extraction skill.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Features** to access the **Now Assist Features** tab of the Now Assist Admin console.

2.  Expand the **Finance and Supply Chain** workflow group and select **Accounts Payable Operations**.

    The APO features are grouped under the **Finance and Supply Chain** workflow group. Each feature has its associated skills.

3.  Activate and configure the skills for the APO application.

    |Skills|Action|
    |------|------|
    |Purchase order line mapping|To activate the skill, on the Purchase order line mapping skill card, select **Turn on**.|
    |Invoice case summarization|On the Purchase order line mapping skill card, select **Activate skill**.|
    |Invoice data extraction|On the Invoice data extraction mapping skill card, select **Activate skill**.|

4.  For Invoice case summarization skill:

    ![Invoice case summarization in Now Assist](../image/invoice-case-na.png)

    1.  Select **General Details**, review the details about the skill, and then select **Save and continue** to go to the next step.

    2.  Follow the steps to configure and activate a skill by using the Guided Setup.

    3.  Select **View Case Input**, review the base input table and input fields, and then select **Save and continue** to go to the next step.

    4.  To test the prompt on a record, select **Customize and test prompt**.

    5.  Select **Save and continue** to go to the next step.

    6.  Select **Define Availability** and choose one of the following options.

<table id="choicetable_rhm_hxq_1fc"><thead><tr><th align="left" id="d142378e261">

Option

</th><th align="left" id="d142378e264">

Description

</th></tr></thead><tbody><tr><td id="d142378e270">

**Skill is always available**

</td><td>

The skill is always available to users.

</td></tr><tr><td id="d142378e279">

**Customize skill availability**

</td><td>

The skill is available only when the certain conditions are met \(default\).Use the condition builder to set your conditions.

</td></tr></tbody>
</table>    1.  Select **Save and continue** to go to the next step.

    2.  Choose **Select display** to determine where you'd like to display the skill.

<table id="choicetable_fhc_qxq_1fc"><thead><tr><th align="left" id="d142378e315">

Option

</th><th align="left" id="d142378e318">

Description

</th></tr></thead><tbody><tr><td id="d142378e324">

**In-product desktop**

</td><td>

Now Assist skills are displayed on forms and workspaces.

</td></tr><tr><td id="d142378e335">

**Now Assist panel**

</td><td>

Now Assist skills are available in the Now Assist panel. Turn on multi-language support for user-entered text with Dynamic Translation in Now Assist applications. For more information, see [Configure multilingual service for Now Assist applications](https://www.servicenow.com/docs/access?context=enable-dynamic-translation-for-now-assist-applications&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).**Note:** If you don't see this option, you must activate the Now Assist panel. For more information, see [Activate the Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

</td></tr></tbody>
</table>5.  Select **Save and continue** to go to the next step.

6.  Review your choices and select **Activate** to complete the configuration for the skill.

7.  Complete the setup by selecting **Done**.

    The skill is displayed in the Active skills section.

8.  In case of Invoice data extraction for the APO specialists feature card, select **Activate skill**.

    1.  In the **Create Usecase** step, select the **Invoice Processing - GenAI** use case.![Invoice processing using generativeAI](../image/invoice-processing-genai.png)

    2.  Select **Make a copy** to create a copy of the use case.

        For more information on the fields, test outputs, and integrations in the use case, see [Set up a use case for Now Assist in Document Intelligence](https://www.servicenow.com/docs/access?context=set-up-use-case-for-now-assist-document-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

        **Note:** When you create a copy of the generative AI use case in Now Assist console, then "DocIntel Extract Values Flow - copied GenAI use case name-Invoice processing-GenAI integration" use case is created automatically in the flow designer. For more information on configuring the use case, see [Configuring the invoice ingestion flows using Accounts Payable Operations integration with Document Intelligence](../concept/config-apo-docintel-integration.md).

    3.  Select **Save and continue** to go to the next step.

    4.  In the **Review and activate** step, select **Activate**.

    The Invoice data extraction skill is activated.

9.  On the Purchase order line mapping summarization for the APO specialists feature card, select **Turn on**.

    The generative AI skill auto-generates mappings between invoice lines and purchase order lines.


**Related topics**  


[Upgrade Accounts Payable Operations](upgrade.md)

[Install Accounts Payable Operations integration with Document Intelligence](../concept/apm-integration-docintel.md)

[Invoice Case Management](../concept/acc-pay-case-mgmt-overview.md)

