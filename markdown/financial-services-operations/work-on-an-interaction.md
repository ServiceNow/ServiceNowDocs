---
title: Work on an interaction in Agentic Contact Center for Banking
description: Manage customer interactions in the Interaction page, from accepting incoming calls to resolving issues with AI-powered assistance. Customer service representatives \(CSRs\) can verify customer identity, use AI-generated insights, and complete interactions with automated wrap-up summaries.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Agentic Contact Center for Banking, Banking applications, Financial Services Operations \(FSO\)]
---

# Work on an interaction in Agentic Contact Center for Banking

Manage customer interactions in the Interaction page, from accepting incoming calls to resolving issues with AI-powered assistance. Customer service representatives \(CSRs\) can verify customer identity, use AI-generated insights, and complete interactions with automated wrap-up summaries.

## Before you begin

Role required: sn\_fso\_csr.business\_agent, sn\_fso\_csr.personal\_agent

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Initiate an interaction in the workspace.

    -   When a customer initiates a call, select **Accept** in the inbox item.
    -   Manually create a new interaction record in the workspace.
    A new interaction record is created and opens in a new tab in the workspace.

3.  Review the **Customer context summarization** to get an AI-generated snapshot of the customer's situation and sentiment when the call begins.

4.  After verifying the customer's details and identity, select **Verified** in the Interaction form to confirm.

5.  To open the Now Assist panel for agentic AI support for this interaction, select **Ask Now Assist**.

    **Note:** By default, **Ask Now Assist** is available when:

    -   The interaction **Type** is Phone.
    -   The **Consumer** or **Account** field is not empty.
    -   The interaction **State** is Work in Progress.
    -   The **Assigned to** value is not set to virtual agent.
    The Now Assist panel displays and the Banking CSR support AI agent analyzes the intent of the conversation, highlights any insights relevant to the customer, and offers next-step guidance.

    The chat is specific to this interaction record. If you navigate away, you can resume the chat by selecting **Ask Now Assist**.

    For more information, see [Request AI agent support in the Interaction page](../../fso-now-assist/task/request-ai-agent-interaction-workspace.md).

6.  After resolving the customer's issues, end the chat or call.

7.  Wrap up the interaction.

    When wrap-up codes are set up and the Wrap Up Completion Now Assist skill is configured, you can generate an AI-powered chat summary. This summary provides a record of what was discussed and any action items in the interaction.


## Result

The interaction is closed.

**Parent Topic:**[Financial Services](../../fso-common/concept/fso-overview.md)

**Related topics**  


[Interaction page for Agentic Contact Center for Banking](../concept/interaction-workspace-for-agentic-contact-center-for-banking.md)

[Summarize customer interaction context in the Interaction page](../../fso-now-assist/task/summarize-customer-context-fso.md)

[Request AI agent support in the Interaction page](../../fso-now-assist/task/request-ai-agent-interaction-workspace.md)

[Interaction wrap up](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/interaction-management/interaction-wrap-up-state.md)

[Use AI to generate wrap up code and notes summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ai-generated-wrap-up-codes-and-notes-summary.md)

