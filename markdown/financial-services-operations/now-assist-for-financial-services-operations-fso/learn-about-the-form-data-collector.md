---
title: Form Data Collector
description: Learn about the Form Data Collector application that is used to assist with populating case form fields during a customer's interaction with a Virtual Agent chatbot.
locale: en-US
release: yokohama
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring Now Assist for FSO, Now Assist for Financial Services Operations \(FSO\)]
---

# Form Data Collector

Learn about the Form Data Collector application that is used to assist with populating case form fields during a customer's interaction with a Virtual Agent chatbot.

## Viewing the Form Data Collector flow

To view the Form Data Collector flow:

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.
2.  In the search field, enter `Conv Form Ask Sequential Questions`.
3.  In the list, select the **Conv Form Ask Sequential Questions**.

## Summary of the Form Data Collector flow

1.  The flow takes the input parameters that are listed in the following table.

    |Name|Description|
    |----|-----------|
    |Table name|Name of the table.|
    |Conversation context|Context of the Virtual Agent conversation.|
    |Sys ID|Identifier of the table.|
    |View|Table view.|

2.  The form fields are retrieved from the table and view inputs.
3.  The flow iterates through each field in the table.
    1.  The field type is determined when a field is found.

        The following field types are supported:

        -   Boolean
        -   Date
        -   Currency
        -   String
        -   Choice
        -   Glide list
        -   Reference
    2.  Using the Form Data Collector capability, the Now LLM Service is called to determine if the question can be answered using the conversation history, or if a new question should be asked to the customer.

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

**Parent Topic:**[Exploring Now Assist for Financial Services Operations \(FSO\)](../../fso-common/concept/exploring-now-assist-for-financial-services-operations-fso.md)

