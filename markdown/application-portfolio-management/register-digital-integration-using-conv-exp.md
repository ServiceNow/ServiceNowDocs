---
title: Register a digital integration conversationally
description: Use the conversational experience of ServiceNow Otto in Virtual Agent to register a digital integration from any application that supports Virtual Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/register-digital-integration-using-conv-exp.html
release: australia
topic_type: task
last_updated: "2026-07-22"
reading_time_minutes: 3
breadcrumb: [Working with digital integrations, Working with digital integration management in Enterprise Architecture Workspace, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Register a digital integration conversationally

Use the conversational experience of ServiceNow Otto in Virtual Agent to register a digital integration from any application that supports Virtual Agent.

## Before you begin

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

Ensure that the following tasks are completed:

-   Install an application that supports Virtual Agent.
-   Complete configuring the conversational experiences for Enterprise Architecture. For more information, see [Configure ServiceNow Otto for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/configure-now-assist-ea.md).

Role required: none

## About this task

In the application that supports Virtual Agent, for example Employee Service Center, start with a prompt to register a business application in the chat. Through a series of questions, Virtual Agent prompts you to provide information for the questions that you configured for a catalog item. ServiceNow Otto in Virtual Agent understands the context and maps the information that you provide to an appropriate catalog item. In this case, the catalog item is a business application.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

2.  Select **Open chat window**.

3.  Enter an instruction to start the conversation with Virtual Agent.

    You can start with a basic instruction such as **Request a digital integration** or an elaborate instruction that includes the digital integration information. The following examples show how each instruction is handled in the chat.

<table id="choicetable_ttr_fll_b2c"><thead><tr><th align="left" id="d38029e162">

Instruction

</th><th align="left" id="d38029e165">

Description

</th></tr></thead><tbody><tr><td id="d38029e171">

**Short: Request a digital integration**

</td><td>

Virtual Agent starts a conversation to ask more information from you about the business application, through a series of questions:

 -   What is the name of the business application for which you want to subscribe?
-   What is the business application you're requesting for?
-   Is this a new provider digital interface?
-   \[Required\] What is the name of the Provider Digital Interface?
-   Who is the IT Owner for this request?
-   What type of business do you own?
-   What type of subscriber are you?
-   Can you please describe the digital integration you would like to enter?
 The information you provide is used to fill in the fields of the digital integration form. \[Omitted image "register-digital-integration.png"\] Alt text: Screenshot showing ServiceNow OttoVirtual Agent chat window showing a request for the requesting a digital integration.

</td></tr><tr><td id="d38029e224">

**Elaborate: Request the new digital integration for the subscriber business application BuyIt and provider business application is Case Management.**

</td><td>

Using the context that you provided, Virtual Agent automatically matches it to the relevant field on the business application form. It then instructs you to enter information of only those fields that you haven't provided.

\[Omitted image "request-digital-integration-details.png"\] Alt text: Screenshot showing ServiceNow OttoVirtual Agent chat window showing a elaborate request for the requesting a digital integration.

</td></tr></tbody>
</table>4.  Review the information that Virtual Agent filled in for the digital integration form fields.

    You can choose to make changes or submit.


**Parent Topic:**[Working with digital integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-digital-integrations.md)

**Related topics**  


[Exploring ServiceNow Otto for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/exploring-now-assist-for-ea.md)

[Configure ServiceNow Otto for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/configure-now-assist-ea.md)

[ServiceNow Otto for Enterprise Architecture \(EA\) access roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/sn-otto-access-roles.md)

