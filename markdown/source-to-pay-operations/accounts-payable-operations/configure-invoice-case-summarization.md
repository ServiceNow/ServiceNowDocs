---
title: Configure Invoice case summarization
description: Enable Accounts Payable fulfillers to use generative AI-powered invoice case summarization to quickly analyze invoice cases and determine next steps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/configure-invoice-case-summarization.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [APO, Accounts Payable Operations, invoice management, AP case]
breadcrumb: [Configure ServiceNow Otto for Accounts Payable Operations \(APO\), ServiceNow Otto for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# Configure Invoice case summarization

Enable Accounts Payable fulfillers to use generative AI-powered invoice case summarization to quickly analyze invoice cases and determine next steps.

## Before you begin

Role required: admin

Install the Document Intelligence for Accounts Payable Operations Content Pack from the ServiceNow® Store for the invoice data extraction skill.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Skills** and select the **AI Skills** tab of the AI Admin Hub.

2.  Expand the **Finance and Supply Chain** workflow group and select **Accounts Payable Operations**.

3.  Activate and configure the skills for the APO application.

    |Skills|Action|
    |------|------|
    | | |
    |Invoice case summarization|On the Purchase order line mapping skill card, select **Activate skill**.|

4.  For Invoice case summarization skill:

    \[Omitted image "invoice-case-na.png"\] Alt text: Invoice case summarization in ServiceNow Otto

    1.  Select **General Details**, review the details about the skill, and then select **Save and continue** to go to the next step.

    2.  Follow the steps to configure and activate a skill by using the Guided Setup.

    3.  Select **View Case Input**, review the base input table and input fields, and then select **Save and continue** to go to the next step.

    4.  To test the prompt on a record, select **Customize and test prompt**.

    5.  Select **Save and continue** to go to the next step.

    6.  Select **Define Availability** and choose one of the following options.

<table id="choicetable_rhm_hxq_1fc"><thead><tr><th align="left" id="d218090e251">

Option

</th><th align="left" id="d218090e254">

Description

</th></tr></thead><tbody><tr><td id="d218090e260">

**Skill is always available**

</td><td>

The skill is always available to users.

</td></tr><tr><td id="d218090e269">

**Customize skill availability**

</td><td>

The skill is available only when the certain conditions are met \(default\).Use the condition builder to set your conditions.

</td></tr></tbody>
</table>    1.  Select **Save and continue** to go to the next step.

    2.  Choose **Select display** to determine where you'd like to display the skill.

<table id="choicetable_fhc_qxq_1fc"><thead><tr><th align="left" id="d218090e305">

Option

</th><th align="left" id="d218090e308">

Description

</th></tr></thead><tbody><tr><td id="d218090e314">

**In-product desktop**

</td><td>

Now Assist skills are displayed on forms and workspaces.

</td></tr><tr><td id="d218090e325">

**ServiceNow Otto panel**

</td><td>

ServiceNow Otto skills are available in the ServiceNow Otto panel. Turn on multi-language support for user-entered text with Dynamic Translation in ServiceNow Otto applications. For more information, see [Configure multilingual service for ServiceNow Otto applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/enable-dynamic-translation-for-now-assist-applications.md).**Note:** If you don't see this option, you must activate the ServiceNow Otto panel. For more information, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md).

</td></tr></tbody>
</table>5.  Select **Save and continue** to go to the next step.

6.  Review your choices and select **Activate** to complete the configuration for the skill.

7.  Complete the setup by selecting **Done**.

    The skill is displayed in the Active skills section.


## Result

The Invoice case summarization skill is activated.

## What to do next

[Summarize a record by using ServiceNow Otto for Accounts Payable Operations \(APO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/now-assist-summarize-apo.md)

