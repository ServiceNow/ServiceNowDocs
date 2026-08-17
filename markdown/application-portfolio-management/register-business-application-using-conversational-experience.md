---
title: Register a business application conversationally
description: Use the conversational experience of ServiceNow Otto in Virtual Agent to register a business application from any application that supports Virtual Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/register-business-application-using-conversational-experience.html
release: australia
topic_type: task
last_updated: "2026-07-22"
reading_time_minutes: 3
breadcrumb: [Working with an application portfolio, Working with Portfolio list view, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Register a business application conversationally

Use the conversational experience of ServiceNow Otto in Virtual Agent to register a business application from any application that supports Virtual Agent.

## Before you begin

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

Ensure that the following tasks are completed:

-   Install an application that supports Virtual Agent.
-   Complete configuring the conversational experiences for Enterprise Architecture. For more information, see [Configure ServiceNow Otto for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/configure-now-assist-ea.md).

Role required: none

## About this task

In the application that supports Virtual Agent, for example Employee Service Center, start with a prompt to register a business application in the chat. Through a series of questions, Virtual Agent prompts you to provide information for the questions that you configured for a catalog item. ServiceNow Otto in Virtual Agent understands the context and maps the information that you provide in response to a question to an appropriate catalog item. In this case, the catalog item is a business application.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

2.  Select **Open chat window**.

3.  Enter an instruction to start the conversation with Virtual Agent.

    You can start with a basic instruction such as **Register a business application** or an elaborate instruction that includes the business application's information. The following examples show how each instruction is handled in the chat.

<table id="choicetable_ttr_fll_b2c"><thead><tr><th align="left" id="d108784e162">

Instruction

</th><th align="left" id="d108784e165">

Description

</th></tr></thead><tbody><tr><td id="d108784e171">

**Short: Register a business application**

</td><td>

Virtual Agent starts a conversation to ask more information from you about the business application, through a series of questions:

 -   What is the name of the business application?
-   What is the benefit or use of the business application?
-   Who is the IT owner of the business application?
-   Who is the owner of the business application?
-   What is the category of the business application?
-   What type of application is this?
 The information you provide is used to fill in the fields of the business application form.\[Omitted image "register-ba-virtual-agent.png"\] Alt text: Screenshot showing ServiceNow OttoVirtual Agent chat window showing a request for the registration of a business application.

</td></tr><tr><td id="d108784e218">

**Elaborate: Register the new business application XYZ, which is used for capturing application metrics. Specify Abel Tuter as both the business application owner and IT owner. Also, category of the business application is Business Intelligence – Reports and type of application is SaaS.**

</td><td>

Using the context that you provided, Virtual Agent automatically matches it to the relevant field on the business application form. It then instructs you to enter information of only those fields that you haven't provided.

\[Omitted image "register-ba-virtual-agent-elaborate.png"\] Alt text: Screenshot showing ServiceNow OttoVirtual Agent chat window showing a elaborate request for the registration of a business application.

</td></tr></tbody>
</table>4.  Review the information that Virtual Agent filled in for the business application form fields.

    You can choose to make changes or submit.


**Parent Topic:**[Working with an application portfolio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-application-portfolio.md)

**Related topics**  


[Exploring ServiceNow Otto for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/exploring-now-assist-for-ea.md)

[Configure ServiceNow Otto for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/configure-now-assist-ea.md)

[ServiceNow Otto for Enterprise Architecture \(EA\) access roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/sn-otto-access-roles.md)

