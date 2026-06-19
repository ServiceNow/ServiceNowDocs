---
title: Create an agentic workflow for automating web tasks
description: Create an agentic workflow in AI Agent Studio so that AI agents can coordinate to automate web tasks that are dynamic in nature.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/enable-ai-experiences/na-ai-wa-configure-workflow.html
release: zurich
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: task
last_updated: "2025-09-02"
reading_time_minutes: 4
breadcrumb: [Add adaptive desktop action for web, Create AI agents, AI Desktop Actions, Enable AI experiences]
---

# Create an agentic workflow for automating web tasks

Create an agentic workflow in AI Agent Studio so that AI agents can coordinate to automate web tasks that are dynamic in nature.

## Before you begin

Set your application scope to Now Assist AI web agent.

Role required: sn\_aia.admin

## About this task

Agentic workflows automate processes with agentic AI. In AI Agent Studio, you must define an agentic workflow and connect it with an AI agent to execute web tasks. These goals can involve variable data or other factors that traditional automation can struggle with.

An AI agent named **Web Automation Agent** and agentic workflow named **Web Automation** are provided by default when you install AI Desktop Actions. You can create a different agentic workflow referencing this AI agent or AI agent that you created so that your users can find and use the agentic workflow in the Now Assist panel.

Verify that the enhanced chat is available in the Now Assist panel. The **Web view** pane is available only when enhanced chat is enabled. For more information, see [Enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/now-assist-panel-enhanced.md).

For more information, see [Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/configure-next-best-action-agent.md) and [Create an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/configure-use-case-ai-agents.md).

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

2.  Select the **Agentic workflows** tab.

    \[Omitted image "na-ai-wa-configure-workflow-topZ.png"\] Alt text: The Agentic workflows tab on the Manage agentic workflows and AI agents module in AI Agent Studio.

3.  Select **New** to open a guided setup.

    \[Omitted image "na-ai-wa-configure-workflow-guided-setupZ.png"\] Alt text: The guided setup for a New agentic workflow

4.  On the Define key requirements page, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Workflow Name**|Enter a descriptive name for the workflow. You can specify the name in the Now Assist panel.|
    |**Workflow description**|Enter a clear and precise description of the goal of the workflow \(for use by the LLM\).|
    |**List of steps**|Enter a numbered list of steps to achieve your goal \(for use by the LLM\).|
    |**Add AI agents that can perform these steps**|Open the modal by selecting **Add AI agent**. From the **AI Agent** drop-down list, search and select **Web Automation Agent** or the AI agent that you created.|
    |**Ask Now Assist to suggest AI agents**|Leave this field blank.|
    |**Unsupported model providers**|Leave this field blank.|

5.  Select **Generate details** in the same page, to open a modal where Now Assist can help compose instructions for the LLM, based on the text that you enter.

    \[Omitted image "na-ai-wa-configure-workflow-generateZ.png"\] Alt text: The modal to generate a description and list of steps. The text field contains a paragraph of example text that Now Assist can transform into appropriate input for the LLM.

6.  Select **Save and continue** to move to the next step.

7.  On the Define user access page, in the **User access** field, select which users can access the agentic workflow.

    -   Users with specified roles
    -   Authenticated users
    -   Public
    If you select the **Users with specific roles** option, the form opens a **Role** field containing a list of available roles.

8.  Select **Save and continue** to move to the next step.

    Saving and moving onto the next step triggers the creation of an ACL for your agentic workflow.

9.  On the Define data access page, in the **User identity type** field, select **Dynamic user** to determine what data agentic workflow has access to.

10. In the **Approved roles** field, select the required roles to restrict the data that this agentic workflow can access when it runs.

11. Select **Save and continue** to move to the next step.

12. On the Add triggers page, specify a trigger.

13. Select **Save and continue** to move to the next step.

14. On the Select channels and status page, enable the **Display** toggle on the **Engage via the Now Assist panel** card.

    \[Omitted image "na-ai-wa-configure-workflow-displayZ.png"\] Alt text: Select a UI display, the final step in the guided setup. The toggle switch is set to Display so that this workflow is available in the Now Assist panel.

15. Select **Save and test**.

    You're directed to the **Testing** tab of AI Agent Studio. For more information, see [Test an AI agent or agentic workflow for adaptive desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/na-ai-wa-test.md).


## Result

The agentic workflow you have created is available in the Now Assist panel to the users you have designated. For more information, see [Trigger an AI agent to execute adaptive path desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/na-ai-wa-access-using-nap.md).

