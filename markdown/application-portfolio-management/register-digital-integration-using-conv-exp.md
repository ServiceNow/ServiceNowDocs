---
title: Register a digital integration by using the conversational experience
description: Use the conversational experience of Now Assist in Virtual Agent to register a digital integration from any application that supports Virtual Agent.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use Now Assist, Now Assist for Enterprise Architecture \(EA\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Register a digital integration by using the conversational experience

Use the conversational experience of Now Assist in Virtual Agent to register a digital integration from any application that supports Virtual Agent.

## Before you begin

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

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

    You can start with a basic instruction such as **Request a business application** or an elaborate instruction that includes the digital integration information. The following examples show how each instruction is handled in the chat.

<table id="choicetable_ttr_fll_b2c"><thead><tr><th align="left" id="d37249e162">

Instruction

</th><th align="left" id="d37249e165">

Description

</th></tr></thead><tbody><tr><td id="d37249e171">

**Short: Request a digital integration**

</td><td>

Virtual Agent starts a conversation to ask more information from you about the business application, through a series of questions:

 -   What is the name of the business application for which you want to subscribe?
-   What is the business application you are requesting for?
-   Is this a new provider digital interface?
-   \[Required\] What is the name of the Provider Digital Interface?
-   Who is the IT Owner for this request?
-   What type of business do you own?
-   What type of subscriber are you?
-   Can you please describe the digital integration you would like to enter?
 The information you provide is used to fill in the fields of the digital integration form. You can skip answering a question that is related to non-required fields by entering **skip**.![Screenshot showing Now AssistVirtual Agent chat window showing a request for the requesting a digital integration.](../image/register-digital-integration.png)

</td></tr><tr><td id="d37249e227">

**Elaborate: Request the new digital integration for the subscriber business application BuyIt and provider business application is Case Management.**

</td><td>

Using the context that you provided, Virtual Agent automatically matches it to the relevant field on the business application form. It then instructs you to enter information of only those fields that you haven't provided.

You can skip answering a question that is related to non-required fields by entering **skip**.

![Screenshot showing Now AssistVirtual Agent chat window showing a elaborate request for the requesting a digital integration.](../image/request-digital-integration-details.png)

</td></tr></tbody>
</table>4.  Review the information that Virtual Agent filled in for the digital integration form fields.

    You can choose to make changes or submit.


**Parent Topic:**[Using Now Assist for Enterprise Architecture \(EA\)](../concept/using-now-assist-for-ea.md)

