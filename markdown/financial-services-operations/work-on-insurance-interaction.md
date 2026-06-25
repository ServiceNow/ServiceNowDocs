---
title: Work on an insurance interaction in Agentic Contact Center for Insurance
description: Manage insurance customer interactions in the Interaction page for Agentic Contact Center for Insurance. Customer service representatives \(CSRs\) can verify customer identity, use AI-generated insights, and complete interactions with automated wrap-up summaries.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/work-on-insurance-interaction.html
release: australia
topic_type: task
last_updated: "2026-05-13"
reading_time_minutes: 4
keywords: [work on an insurance interaction, manage insurance customer interactions, relevant details for this call, verify insurance customer identity, agentic contact center insurance ai-generated insights, agentic contact center insurance wrap-up summary, agentic contact center insurance interaction page, agentic contact center insurance csr interaction workflow, agentic contact center insurance create interaction record]
breadcrumb: [Using Agentic Contact Center for Insurance, Agentic Contact Center for Insurance, Insurance applications, Financial Services Operations \(FSO\)]
---

# Work on an insurance interaction in Agentic Contact Center for Insurance

Manage insurance customer interactions in the Interaction page for Agentic Contact Center for Insurance. Customer service representatives \(CSRs\) can verify customer identity, use AI-generated insights, and complete interactions with automated wrap-up summaries.

## Before you begin

Role required: sn\_ins\_csr.servicing\_agent, sn\_ins\_csr.claims\_agent

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Initiate an interaction in the workspace.

    -   When a customer initiates a call, select **Accept** in the inbox item.
    -   Manually create an interaction record in the workspace.
    A new interaction record is created and opens in a new tab in the workspace.

3.  Review the **Relevant details for this call** card to get an AI-generated snapshot of the customer's situation when the call begins.

    The card surfaces contextual information associated with the inquiry, such as the customer tenure, likely reason for calling, related contacts and cases, and the insurance product the customer is inquiring about. If the card is not visible, the customer's identity has not yet been verified, no call context is available, or the AI skill has not been activated.

    For more information, see [Summarize an insurance customer interaction in Agentic Contact Center for Insurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/summarize-insurance-customer-context.md).

    For a description of the skill, see [Using generative AI in Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/using-now-assist-for-financial-services-operations-fso.md).

4.  After verifying the customer's details and identity, select **Verified** in the Interaction form to confirm.

5.  To open the Now Assist panel for agentic AI support for this interaction, select **Ask Now Assist**.

    **Note:** By default, **Ask Now Assist** is available when:

    -   The interaction **Type** is Phone.
    -   The **Consumer** or **Account** field is not empty.
    -   The interaction **State** is Work in Progress.
    -   The **Assigned to** value is not set to virtual agent.
    The Now Assist panel displays and the Insurance CSR support AI agent analyzes the intent of the conversation, highlights insights relevant to the customer's insurance policies and claims, and offers next-step guidance.

    The chat is specific to this interaction record. If you navigate away, you can resume the chat by selecting **Ask Now Assist**.

    For more information, see [Request AI agent support in the Interaction page for Agentic Contact Center for Insurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/request-insurance-ai-agent-interaction-workspace.md).

6.  To open the Customer 360 page and review the customer's full insurance profile, select the customer's name in the customer details card.

    The Customer 360 page opens in a separate tab and displays the customer's policies, coverages, financial overview, and case history.

7.  After resolving the customer's issues, end the chat or call.

8.  Wrap up the interaction.

    When wrap-up codes are set up and the Wrap Up Completion Now Assist skill is configured, you can generate an AI-powered call summary. This summary provides a record of what was discussed and any action items from the interaction.


## Result

The interaction is closed.

**Related topics**  


[Interaction page for Agentic Contact Center for Insurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/interactionpage-agentic-contact-centre-for-insurance.md)

[Configure insurance customer interaction context summary skill in Now Assist for FSO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/configure-insurance-interaction-summary-skill.md)

[Summarize an insurance customer interaction in Agentic Contact Center for Insurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/summarize-insurance-customer-context.md)

[Request AI agent support in the Interaction page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/request-ai-agent-interaction-workspace.md)

[Interaction wrap up](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/interaction-wrap-up-state.md)

[Use AI to generate wrap up code and notes summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ai-generated-wrap-up-codes-and-notes-summary.md)

