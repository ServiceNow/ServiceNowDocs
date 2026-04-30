---
title: Configure Invoice case summarization
description: Enable fulfiller to use the generative AI based invoice case summarization to quickly analyze the case and take necessary action.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-11-03"
reading_time_minutes: 1
breadcrumb: [Configure Now Assist for Accounts Payable Operations \(APO\), Now Assist for Accounts Payable Operations \(APO\), Accounts Payable Operations, Finance and Supply Chain]
---

# Configure Invoice case summarization

Enable fulfiller to use the generative AI based invoice case summarization to quickly analyze the case and take necessary action.

## Before you begin

Role required: admin

Install the Document Intelligence for Accounts Payable Operations Content Pack from the ServiceNow® Store for the invoice data extraction skill.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Features** to access the **Now Assist Features** tab of the Now Assist Admin console.

2.  Expand the **Finance and Supply Chain** workflow group and select **Accounts Payable Operations**.

3.  Activate and configure the skills for the APO application.

    |Skills|Action|
    |------|------|
    | | |
    |Invoice case summarization|On the Purchase order line mapping skill card, select **Activate skill**.|

4.  For Invoice case summarization skill:

    ![Invoice case summarization in Now Assist](../image/invoice-case-na.png)

    1.  Select **General Details**, review the details about the skill, and then select **Save and continue** to go to the next step.

    2.  Follow the steps to configure and activate a skill by using the Guided Setup.

    3.  Select **View Case Input**, review the base input table and input fields, and then select **Save and continue** to go to the next step.

    4.  To test the prompt on a record, select **Customize and test prompt**.

    5.  Select **Save and continue** to go to the next step.

    6.  Select **Define Availability** and choose one of the following options.

<table id="choicetable_rhm_hxq_1fc"><thead><tr><th align="left" id="d180914e231">

Option

</th><th align="left" id="d180914e234">

Description

</th></tr></thead><tbody><tr><td id="d180914e240">

**Skill is always available**

</td><td>

The skill is always available to users.

</td></tr><tr><td id="d180914e249">

**Customize skill availability**

</td><td>

The skill is available only when the certain conditions are met \(default\).Use the condition builder to set your conditions.

</td></tr></tbody>
</table>    1.  Select **Save and continue** to go to the next step.

    2.  Choose **Select display** to determine where you'd like to display the skill.

<table id="choicetable_fhc_qxq_1fc"><thead><tr><th align="left" id="d180914e285">

Option

</th><th align="left" id="d180914e288">

Description

</th></tr></thead><tbody><tr><td id="d180914e294">

**In-product desktop**

</td><td>

Now Assist skills are displayed on forms and workspaces.

</td></tr><tr><td id="d180914e305">

**Now Assist panel**

</td><td>

Now Assist skills are available in the Now Assist panel. Turn on multi-language support for user-entered text with Dynamic Translation in Now Assist applications. For more information, see [Configure multilingual service for Now Assist applications](https://www.servicenow.com/docs/access?context=enable-dynamic-translation-for-now-assist-applications&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).**Note:** If you don't see this option, you must activate the Now Assist panel. For more information, see [Activate Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

</td></tr></tbody>
</table>5.  Select **Save and continue** to go to the next step.

6.  Review your choices and select **Activate** to complete the configuration for the skill.

7.  Complete the setup by selecting **Done**.

    The skill is displayed in the Active skills section.


