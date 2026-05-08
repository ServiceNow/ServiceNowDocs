---
title: Work with the Inquiry resolution provider
description: Use the Inquiry resolution provider agent to generate resolutions to invoice inquiry cases that are raised by suppliers and employees.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Resolve supplier questions workflow]
breadcrumb: [Inquiry resolution provider AI agent, Using AI agents in Now Assist for Accounts Payable Operations, Now Assist for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# Work with the Inquiry resolution provider

Use the Inquiry resolution provider agent to generate resolutions to invoice inquiry cases that are raised by suppliers and employees.

## Before you begin

Set the scope to Now Assist for Accounts Payable Operations.

Role required: now\_assist\_panel\_user, admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

    The **Manage agentic workflows and AI agents** page appears.

2.  Select **AI agents**.

3.  Use the search icon ![Search icon](../../../common/image/List_SearchIcon.png) and select **Inquiry resolution provider**.

    To modify this AI agent, refer to Modify an AI agent. Adjust the settings for your specific needs and activate the duplicated version of the agentic workflow after you duplicate it.![Invoice resolution provider](../image/apo-agent-ai.png)

4.  Review the information in the **Define the specialty** page, and then select **Continue**.

    The **Define the specialty** page is read-only.

5.  Review the information in the **Add tools and information** page, and then select **Continue**.

    The **Add tools and information** page is read-only.

6.  Select **Define trigger** &gt;**Resolution provider trigger** &gt; **Status** &gt; **Active**.

    The Define trigger page appears.![Define trigger](../image/apo-define-trigger.png)

7.  Select **Continue**.

8.  In the **Toggle display** page, enable the **Display** option to display AI agent output in the Now Assist panel.![Toggle display](../image/apo-toggle.png)

9.  Select **Save and test**.

    **Note:**

    If you're upgrading from previous versions to the latest version of APO, the flow name updates to Invoice case - AI agent: Inquiry resolution provider - SysID.

10. In the Inquiry resolution provider flow, select the trigger and set the **Run trigger** to run once.

11. Select **Done** and **Activate** the flow.

12. Navigate to **Test AI reasoning** page to begin testing your agent.

    The agent executes the testing in AI Agent Studio.


## Execute Invoice resolution provider agent

## Example

Enter the objective of the task as `Help me resolve invoice inquiry INVC0001001` and start test. The AI agent starts to execute and provides the resolution plan. ![Resolution provider agent](../image/apo-invoice-agent.png)

**Related topics**  


[Case resolution using Inquiry resolution provider](case-resolution-using-agent.md)

