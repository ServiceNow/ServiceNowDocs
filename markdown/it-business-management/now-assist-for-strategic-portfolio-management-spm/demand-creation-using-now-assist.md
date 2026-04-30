---
title: Create demands by using the conversational experience
description: Use the conversational experience of Now Assist in Virtual Agent to create a demand from any application that supports Virtual Agent.
locale: en-US
release: yokohama
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [Create a demand,]
breadcrumb: [Using Now Assist for Strategic Portfolio Management \(SPM\), Now Assist for Strategic Portfolio Management \(SPM\), Strategic Portfolio Management]
---

# Create demands by using the conversational experience

Use the conversational experience of Now Assist in Virtual Agent to create a demand from any application that supports Virtual Agent.

## Before you begin

Ensure that the following tasks are completed:

-   Install an application that supports Virtual Agent, for example Employee Service Center.
-   [Enable conversational demand creation using Now Assist in Virtual Agent](configure-conversational-demand-creation-experience.md)

Role required: none

## About this task

Creating demands using Now Assist 

In Employee Service Center, start with a prompt to create a demand in the chat. Through a series of questions, Virtual Agent prompts you to provide information for the questions that you configured for a catalog item. Now Assist in Virtual Agent understands the context and maps the information that you provide in response to a question to an appropriate catalog item, in this case, a demand.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

2.  Select **Open chat window**.

3.  Enter an instruction to start the conversation with Virtual Agent.

    You can start with a basic instruction such as **Create demand** or an elaborate instruction that includes the demand's information. The following examples show how each instruction is handled in the chat.

<table id="table_msb_5jw_hbc"><thead><tr><th>

Instruction

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short: **Create demand**

</td><td>

Virtual Agent starts a conversation to ask more information from you about the demand through a series of questions:-   What is the name of your demand?
-   What is the reason for this demand?
-   What are the risks associated with performing this demand?
The information you provide is used to fill in the fields of the Demand form. You can skip answering a question that is related to non-required fields by entering **skip**.

</td></tr><tr><td>

Elaborate: **Create a demand with the name Upgrade MyApp and business justification as upgrade and risk of not performing as milestones will be missed.**

</td><td>

Using the context that you provided, Virtual Agent automatically matches it to the relevant field on the Demand form.

 It then instructs you to enter information of only those fields that you haven't provided, such as the risk associated with performing the demand, assumption, and others.

 You can skip answering a question that is related to non-required fields by entering **skip**.

</td></tr></tbody>
</table>4.  Review the information that Virtual Agent filled in for the Demand form fields.

    You can choose to make changes or submit.

5.  Add attachments for the demand.

    The information that you provided is submitted to create a demand. Virtual Agent creates a demand and provides the information such as its number, short description, and state.

    The conversation is now complete.


**Parent Topic:**[Using Now Assist for Strategic Portfolio Management \(SPM\)](../concept/using-now-assist-for-spm.md)

**Related topics**  


[Using Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

