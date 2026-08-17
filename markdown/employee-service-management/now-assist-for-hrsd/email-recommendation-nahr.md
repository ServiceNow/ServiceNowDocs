---
title: Generate an email reply recommendation using ServiceNow Otto for HRSD
description: Generate an email reply that is based on the case and email context by using the ServiceNow Otto icon. With email reply recommendations, agents can create quick emails or responses, helping minimize errors and ramp up productivity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/now-assist-for-hrsd/email-recommendation-nahr.html
release: zurich
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Use generative AI skills, ServiceNow Otto for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Generate an email reply recommendation using ServiceNow Otto for HRSD

Generate an email reply that is based on the case and email context by using the ServiceNow Otto icon. With email reply recommendations, agents can create quick emails or responses, helping minimize errors and ramp up productivity.

## Before you begin

[Configure ServiceNow Otto for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-hrsd/configure-now-assist-hr.md).

Role required: sn\_hr\_gen\_ai.admin

## About this task

An agent can do these actions by using the ServiceNow Otto icon:

-   Generate a recommended email reply that is based on the case and email context.
-   Generate recommended email for new, forwarded, and finishing draft emails.
-   Refine the recommendation by elaborating or shortening the response.
-   Availability of email template recommendations while composing an email.

**Note:** The email reply recommendation skill can be found in the **HRSD** tab under the **Employee** group in AI Admin Hub.

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

You can make a copy of this skill to configure it to meet your business needs. For more information, see [Make a copy of AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/make-a-copy-of-a-now-assist-skill.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Agent Workspace for HRSD** and open an HR case that supports the email reply recommendation.

2.  Choose how to compose an email.

<table id="choicetable_tbz_hyv_bcc"><thead><tr><th align="left" id="d201868e151">

Method

</th><th align="left" id="d201868e154">

Description

</th></tr></thead><tbody><tr><td id="d201868e160">

**Compose email from More actions**

</td><td>

1.  Select **Compose email**.
2.  Write six or more words and then select the words that you just wrote to see the ServiceNow Otto icon \[Omitted image "icon-ai-sparkle.png"\] Alt text: Sparkle icon for Now Assist.
3.  Select the ServiceNow Otto icon \[Omitted image "icon-ai-sparkle.png"\] Alt text: Sparkle icon for Now Assist. to generate a response.
4.  Select **Refine** to shorten or elaborate the content.
5.  Get a recommendation that is based on the existing context.


</td></tr><tr><td id="d201868e211">

**Compose an email from Activity stream**

</td><td>

1.  In the activity stream, select an existing email that you want to reply to.
2.  Position your cursor within the email message window to see the ServiceNow Otto icon \[Omitted image "icon-ai-sparkle.png"\] Alt text: Sparkle icon for Now Assist..
3.  Select the ServiceNow Otto icon \[Omitted image "icon-ai-sparkle.png"\] Alt text: Sparkle icon for Now Assist. to receive a recommendation that is based on the existing context.


</td></tr></tbody>
</table>3.  In the email message window, either type a response, or leave blank, and then select the ServiceNow Otto \[Omitted image "icon-ai-sparkle.png"\] Alt text: Sparkle icon for Now Assist..

<table id="choicetable_e5x_3yv_bcc"><thead><tr><th align="left" id="d201868e268">

Email message window

</th><th align="left" id="d201868e271">

ServiceNow Otto icon

</th></tr></thead><tbody><tr><td id="d201868e280">

**Typed response**

</td><td>

Provides the option to refine your response:-   Elaborate
-   Shorten


</td></tr><tr><td id="d201868e297">

**Left blank**

</td><td>

Generates a recommended email reply that is based on the context of the email up to this point.

</td></tr><tr><td id="d201868e306">

**Use template**

</td><td>

Shows email template recommendations while composing an email.

</td></tr></tbody>
</table>4.  Update the selected text with refined text by selecting **Replace**.

5.  Review the generated email reply and select **Refine** to modify the response, or select **Insert** to paste the response into the chat message window.

6.  Select **Send Email** or discard the draft if you don’t like the recommendation.


**Parent Topic:**[Using ServiceNow Otto for HR Service Delivery \(HRSD\) in Agent Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-hrsd/use-now-assist-hr.md)

**Related topics**  


[Summarize a chat conversation using ServiceNow Otto for HR Service Delivery \(HRSD\)]()

[Summarize a Sidebar discussion by using ServiceNow Otto for HRSD]()

[Generate a chat reply recommendation by using ServiceNow Otto for HRSD]()

[Generate a knowledge article from HR Agent Workspace with ServiceNow Otto for HRSD]()

[Generate a knowledge article from multiple cases]()

[Summarize an HR case using ServiceNow Otto for HRSD]()

[Summarize an ER case using ServiceNow Otto for HRSD]()

[Summarize an ER case interview using ServiceNow Otto for HRSD]()

[Generate resolution notes using ServiceNow Otto for HRSD]()

[View employee summary reports]()

[Summarize actions while transferring an HR case]()

[Use Knowledge Graph in ServiceNow Otto for HRSD]()

[Use ServiceNow Otto for HRSD – Galileo Inside to answer HR-related questions]()

[Use the ServiceNow Otto panel in HR Agent Workspace]()

[Submit an HR request with Gen AI Virtual Agent]()

[ServiceNow Otto for HR Service Delivery \(HRSD\) integration with Enterprise Service Management Integrations Framework]()

[Analyze sentiments in ServiceNow Otto for HR Service Delivery \(HRSD\)]()

