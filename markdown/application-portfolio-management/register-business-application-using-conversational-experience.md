---
title: Register a business application by using the conversational experience
description: Use the conversational experience of Now Assist in Virtual Agent to register a business application from any application that supports Virtual Agent.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use Now Assist, Now Assist for Enterprise Architecture \(EA\), Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Register a business application by using the conversational experience

Use the conversational experience of Now Assist in Virtual Agent to register a business application from any application that supports Virtual Agent.

## Before you begin

Ensure that the following tasks are completed:

-   Install an application that supports Virtual Agent.
-   Complete configuring the conversational experiences for Enterprise Architecture. For more information, see [Configure Now Assist for Enterprise Architecture \(EA\)](configure-now-assist-ea.md).

Role required: none

## About this task

In the application that supports Virtual Agent, for example Employee Service Center, start with a prompt to register a business application in the chat. Through a series of questions, Virtual Agent prompts you to provide information for the questions that you configured for a catalog item. Now Assist in Virtual Agent understands the context and maps the information that you provide in response to a question to an appropriate catalog item, in this case, a business application.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

2.  Select **Open chat window**.

3.  Enter an instruction to start the conversation with Virtual Agent.

    You can start with a basic instruction such as **Register a business application** or an elaborate instruction that includes the business application's information. The following examples show how each instruction is handled in the chat.

<table id="choicetable_ttr_fll_b2c"><thead><tr><th align="left" id="d95037e152">

Instruction

</th><th align="left" id="d95037e155">

Description

</th></tr></thead><tbody><tr><td id="d95037e161">

**Short: Register a business application**

</td><td>

Virtual Agent starts a conversation to ask more information from you about the business application, through a series of questions:

 -   What is the name of the business application?
-   What is the benefit or use of the business application?
-   Who is the IT owner of the business application?
-   Who is the owner of the business application?
-   What is the category of the business application?
-   What type of application is this?
 The information you provide is used to fill in the fields of the business application form. You can skip answering a question that is related to non-required fields by entering **skip**.![Screenshot showing Now AssistVirtual Agent chat window showing a request for the registration of a business application.](../image/register-ba-virtual-agent.png)

</td></tr><tr><td id="d95037e211">

**Elaborate: Register the new business application XYZ, which is used for capturing application metrics. Specify Abel Tuter as both the business application owner and IT owner. Also, category of the business application is Business Intelligence – Reports and type of application is SaaS.**

</td><td>

Using the context that you provided, Virtual Agent automatically matches it to the relevant field on the business application form. It then instructs you to enter information of only those fields that you haven't provided.

You can skip answering a question that is related to non-required fields by entering **skip**.![Screenshot showing Now AssistVirtual Agent chat window showing a elaborate request for the registration of a business application.](../image/register-ba-virtual-agent-elaborate.png)

</td></tr></tbody>
</table>4.  Review the information that Virtual Agent filled in for the business application form fields.

    You can choose to make changes or submit.


**Parent Topic:**[Using Now Assist for Enterprise Architecture \(EA\)](../concept/using-now-assist-for-ea.md)

