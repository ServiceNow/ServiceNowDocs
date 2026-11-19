---
title: Work with the Inquiry resolution provider
description: Use the Inquiry resolution provider agent to generate resolutions to invoice inquiry cases that are raised by suppliers and employees.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/source-to-pay-operations/accounts-payable-operations/apo-ai-agent-use-case-trigger.html
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Resolve supplier questions workflow]
breadcrumb: [Inquiry resolution provider AI agent, Using AI agents in Now Assist for Accounts Payable Operations, ServiceNow Otto for Accounts Payable Operations \(APO\), Accounts Payable Operations, Finance and Supply Chain]
---

# Work with the Inquiry resolution provider

Use the Inquiry resolution provider agent to generate resolutions to invoice inquiry cases that are raised by suppliers and employees.

## Before you begin

Verify that the scope is set to Now Assist for Accounts Payable Operations.

Role required: now\_assist\_panel\_user, admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

    The **Manage agentic workflows and AI agents** page appears.

2.  Select **AI agents**.

3.  Use the search icon \[Omitted image "List\_SearchIcon.png"\] Alt text: Search icon and select **Inquiry resolution provider**.

    If you want to modify this AI agent, you can refer to [Modify an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/modify-ai-agent.md). Adjust the settings for your specific needs, and activate the duplicated version of the agentic workflow.\[Omitted image "apo-agent-ai.png"\] Alt text: Invoice resolution provider

4.  Review the information in the **Define the specialty** page, and then select **Continue**.

    The **Define the specialty** page is read-only.

5.  Review the information in the **Add tools and information** page, and then select **Continue**.

    The **Add tools and information** page is read-only.

6.  Select **Define trigger** &gt;**Resolution provider trigger** &gt; **Status** &gt; **Active**.

    The Define trigger page is shown below.\[Omitted image "apo-define-trigger.png"\] Alt text: Define trigger

7.  Select **Continue**.

8.  In the **Toggle display** page, optionally you can enable the **Display** option to display AI agent output in the Now Assist panel.\[Omitted image "apo-toggle.png"\] Alt text: Toggle display

9.  Select **Save and test**.

10. Navigate to **Test AI reasoning** page to begin testing your agent.

    The agent executes the testing in AI Agent Studio.


## Execute Invoice resolution provider agent

## Example

Enter the objective of the task as Help me resolve invoice inquiry INVC0001001 and start test. The AI agent starts to execute and provides the resolution plan as shown below. \[Omitted image "apo-invoice-agent.png"\] Alt text: Resolution provider agent

**Related topics**  


[Case resolution using Inquiry resolution provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/accounts-payable-operations/case-resolution-using-agent.md)

