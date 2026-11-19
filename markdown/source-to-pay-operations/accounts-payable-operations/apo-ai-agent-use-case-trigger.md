---
title: Work with the inquiry resolution provider agent
description: Use the inquiry resolution provider agent to generate resolutions to invoice inquiry cases raised by suppliers and employees.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/accounts-payable-operations/apo-ai-agent-use-case-trigger.html
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Resolve supplier questions workflow, APO, Accounts Payable Operations, Inquiry resolution provider, supplier, AI Agent Studio, invoice inquiry case, Test AI reasoning, APO admin]
breadcrumb: [Inquiry resolution provider AI agent, Use AI agents in ServiceNow Otto for Accounts Payable Operations \(APO\), ServiceNow Otto for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# Work with the inquiry resolution provider agent

Use the inquiry resolution provider agent to generate resolutions to invoice inquiry cases raised by suppliers and employees.

## Before you begin

Set the scope to Now Assist for Accounts Payable Operations.

Role required: now\_assist\_panel\_user, admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

    The **Manage agentic workflows and AI agents** page appears.

2.  Select **AI agents**.

3.  Use the search icon \[Omitted image "List\_SearchIcon.png"\] Alt text: Search icon and select **Inquiry resolution provider**.

    To modify this AI agent, refer to [Modify an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/modify-ai-agent.md). Adjust the settings for your specific needs and activate the duplicated version of the agentic workflow after you duplicate it.\[Omitted image "apo-agent-ai.png"\] Alt text: Invoice resolution provider

4.  Review the information in the **Define the specialty** page, and then select **Continue**.

    The **Define the specialty** page is read-only.

5.  Review the information in the **Add tools and information** page, and then select **Continue**.

    The **Add tools and information** page is read-only.

6.  Select **Add trigger** &gt;**Resolution provider trigger** &gt; **Toggle the Trigger is ON** &gt; **Save**.

    \[Omitted image "apo-define-trigger.png"\] Alt text: Add trigger

7.  Select **Continue**.

8.  In the **Select channels and status** page, toggle the **Engage via ServiceNow Otto chat assistants** to **Allow** display AI agent output in the ServiceNow Otto panel.\[Omitted image "apo-toggle.png"\] Alt text: Toggle display

9.  Select **Save and test**.

    **Note:**

    If you're upgrading from previous versions to the latest version of APO, then see [Inquiry resolution provider AI agent- Unable to activate agent's trigger \[KB3007048\].](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3007048)

10. In the Inquiry resolution provider flow, select the trigger and set the **Run trigger** to run once.

11. Select **Done** and **Activate** the flow.

12. Navigate to **Test AI reasoning** page to begin testing your agent.

    The agent executes the testing in AI Agent Studio.


## Result

The Inquiry resolution provider agent is activated.

## Execute Invoice resolution provider agent

## Example

Enter the objective of the task as `Help me resolve invoice inquiry INVC0001001` and start test. The AI agent starts to execute and provides the resolution plan. \[Omitted image "apo-invoice-agent.png"\] Alt text: Resolution provider agent

**Related topics**  


[Case resolution using inquiry resolution provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/case-resolution-using-agent.md)

