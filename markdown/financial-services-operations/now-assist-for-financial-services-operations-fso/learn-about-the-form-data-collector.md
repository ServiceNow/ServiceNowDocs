---
title: Form Data Collector
description: Learn about the Form Data Collector. This application is used to assist with populating case form fields during a customer's interaction with a Virtual Agent chatbot.
locale: en-US
release: australia
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore, Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Form Data Collector

Learn about the Form Data Collector. This application is used to assist with populating case form fields during a customer's interaction with a Virtual Agent chatbot.

## Viewing the Form Data Collector flow

To view the Form Data Collector flow:

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.
2.  In the search field, type Conv Form Ask Sequential Questions.
3.  Select the **Conv Form Ask Sequential Questions** topic block in the list.

## Summary of the Form Data Collector flow

1.  The flow takes the following input parameters:

    |Name|Description|
    |----|-----------|
    |Table name|The name of the table.|
    |Conversation context|The context of the Virtual Agent conversation.|
    |Sys ID|The identifier of the table.|
    |View|The table view.|

2.  The form fields are retrieved from the table and view inputs.
3.  The flow iterates through each field in the table.
    1.  Determine the field type when a field is found.

        The following field types are supported:

        -   Boolean
        -   Date
        -   Currency
        -   String
        -   Choice
        -   Glide list
        -   Reference
    2.  Using the Form Data Collector capability, call Now LLM to determine if the question can be answered using the conversation history, or if a new question should be asked to the customer.

<table id="table_pct_dkm_b2c"><tbody><tr><td>

Question can be answered using conversation history

</td><td>

Update the case record \(created by the Virtual Agent topic\) with data from the customer's response.

</td></tr><tr><td>

Question cannot be answered using conversation history

</td><td>

Generate a question in a conversational format using Now LLM and present it to the customer.

</td></tr></tbody>
</table>4.  When there are no more fields, the flow returns the response output and the record field value pair.

**Note:** Only UI policies are supported for field iteration in a form. Client scripts are currently not supported.

## Questions Displayed in Disputes intake via Virtual Agent

Disputes intake via Virtual Agent displays the same questions, dispute category options, and dispute reason options presented in the Disputes playbook.

## Bypassed questions from LLM processing

The Form Data Collector in Disputes intake via Virtual Agent will bypass the following questions from LLM processing during the conversation. These questions require direct customer input to ensure that the correct dispute category and reason code are selected.

-   Select dispute reason
-   Select dispute category
-   What best describes your issue?
-   Please provide additional details about the issue.
-   Was the transaction processed within the Intra-European Economic Area?
-   What best describes your billing issue?
-   Which of these is incorrect?
-   Did you receive a refund instead of having the transaction reversed?
-   Did you attempt to make this transaction?
-   Is the card in your possession?
-   Do you see an extra transaction related to your original purchase?
-   Did you make this transaction while commuting?
-   What best describes your billing issue?

