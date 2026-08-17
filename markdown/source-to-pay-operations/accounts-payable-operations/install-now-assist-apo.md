---
title: Install ServiceNow Otto for Accounts Payable Operations \(APO\)
description: Install the APO plugin \[sn\_ap\_gen\_ai\] to give AP fulfillers access to generative AI skills in Source-to-Pay Workspace and Core UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/install-now-assist-apo.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [APO, Accounts Payable Operations, generative AI, Accounts Payable Workspace]
breadcrumb: [Configure ServiceNow Otto for Accounts Payable Operations \(APO\), ServiceNow Otto for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# Install ServiceNow Otto for Accounts Payable Operations \(APO\)

Install the APO plugin \[sn\_ap\_gen\_ai\] to give AP fulfillers access to generative AI skills in Source-to-Pay Workspace and Core UI.

## Before you begin

Role required: admin

Install the Document Intelligence for Accounts Payable Operations Content Pack from the ServiceNow® Store for the invoice data extraction skill.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Skills** and select the AI skills in the AI Admin Hub console.

2.  Expand the **Finance and Supply Chain** workflow group and select **Accounts Payable Operations**.

    The APO features are grouped under the **Finance and Supply Chain** workflow group. Each feature has its associated skills.

3.  Activate and configure the skills for the APO application.

    |Skills|Action|
    |------|------|
    |Purchase order line mapping|To activate the skill, on the Purchase order line mapping skill card, select **Turn on**.|
    |Invoice case summarization|On the Purchase order line mapping skill card, select **Activate skill**.|
    |Invoice data extraction|On the Invoice data extraction mapping skill card, select **Activate skill**.|
    |Invoice inquiry solution generator|On the Invoice data extraction mapping skill card, select **Turn on**.|
    |Sentiment analysis for invoice case|On the Sentiment analysis for invoice case skill card, select **Activate skill**.|
    |Accounts payable document classification|On the Accounts payable document classification skill card, select **Activate skill**.|
    |Relevant invoice finder|On the Relevant invoice finder skill card, select **Turn on**.|
    |Email response for invoice case|Automatically turns on.|
    |Email response for invoice task|Automatically turns on.|

4.  For Invoice case summarization skill:

    \[Omitted image "invoice-case-na.png"\] Alt text: Invoice case summarization in ServiceNow Otto

    1.  Select **General Details**, review the details about the skill, and then select **Save and continue** to go to the next step.

    2.  Follow the steps to configure and activate a skill by using the Guided Setup.

    3.  Select **View Case Input**, review the base input table and input fields, and then select **Save and continue** to go to the next step.

    4.  To test the prompt on a record, select **Customize and test prompt**.

    5.  Select **Save and continue** to go to the next step.

    6.  Select **Define Availability** and choose one of the following options.

<table id="choicetable_rhm_hxq_1fc"><thead><tr><th align="left" id="d191169e357">

Option

</th><th align="left" id="d191169e360">

Description

</th></tr></thead><tbody><tr><td id="d191169e366">

**Skill is always available**

</td><td>

The skill is always available to users.

</td></tr><tr><td id="d191169e375">

**Customize skill availability**

</td><td>

The skill is available only when the certain conditions are met \(default\).Use the condition builder to set your conditions.

</td></tr></tbody>
</table>    1.  Select **Save and continue** to go to the next step.

    2.  Choose **Select display** to determine where you'd like to display the skill.

<table id="choicetable_fhc_qxq_1fc"><thead><tr><th align="left" id="d191169e411">

Option

</th><th align="left" id="d191169e414">

Description

</th></tr></thead><tbody><tr><td id="d191169e420">

**In-product desktop**

</td><td>

AI skills are displayed on forms and workspaces.

</td></tr><tr><td id="d191169e429">

**panel**

</td><td>

AI skills are available in the ServiceNow Otto Panel. Turn on multi-language support for user-entered text with Dynamic Translation in ServiceNow Otto applications. For more information, see [Configure multilingual service for ServiceNow Otto applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/enable-dynamic-translation-for-now-assist-applications.md).**Note:** If you don't see this option, you must activate the ServiceNow Otto panel. For more information, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md).

</td></tr></tbody>
</table>5.  Select **Save and continue** to go to the next step.

6.  Review your choices and select **Activate** to complete the configuration for the skill.

7.  Complete the setup by selecting **Done**.

    The skill is displayed in the Active skills section.

8.  In case of Invoice data extraction for the APO specialists feature card, select **Activate skill**.

    1.  In the **Create Usecase** step, select the **Invoice Processing - GenAI** use case.\[Omitted image "invoice-processing-genai.png"\] Alt text: Invoice processing using generativeAI

    2.  Select **Make a copy** to create a copy of the use case.

        For more information on the fields, test outputs, and integrations in the use case, see [Set up a use case for Now Assist in Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/set-up-use-case-for-now-assist-document-intelligence.md).

        **Note:** When you create a copy of the generative AI use case in AI Admin Hub, then "DocIntel Extract Values Flow - copied GenAI use case name-Invoice processing-GenAI integration" use case is created automatically in the flow designer. For more information on configuring the use case, see [Configuring the invoice ingestion flows using Accounts Payable Operations integration with Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/config-apo-docintel-integration.md).

    3.  Select **Save and continue** to go to the next step.

    4.  In the **Review and activate** step, select **Activate**.

    The Invoice data extraction skill is activated.

9.  On the Purchase order line mapping summarization for the APO specialists feature card, select **Turn on**.


## Result

The generative AI skill auto-generates mappings between invoice lines and purchase order lines.

