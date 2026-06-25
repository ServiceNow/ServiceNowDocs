---
title: AI summarization of email interactions
description: Email Interaction uses AI to generate summaries of email threads, reducing the time agents spend reading full conversation histories. Summaries can be generated on demand.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/eaai-ai-summarization-email-interactions.html
release: australia
topic_type: concept
last_updated: "2026-05-11"
reading_time_minutes: 2
keywords: [AI summarization, email interactions, ServiceNow Otto]
breadcrumb: [Email Interaction, Email channel, Enable communication channels, Configure, Customer Service Management]
---

# AI summarization of email interactions

Email Interaction uses AI to generate summaries of email threads, reducing the time agents spend reading full conversation histories. Summaries can be generated on demand.

**Note:** Check your entitlements to determine whether you have access to AI summarization for email interactions.

## AI summarization capabilities

AI summarization for email interactions uses ServiceNow Otto generative AI capabilities to analyze email conversation threads, work notes, and comments, and generate summaries. This helps agents quickly grasp the essential information from lengthy email exchanges, reducing the time needed to understand customer issues and responding more efficiently.

The AI summarization feature processes email content, identifies key topics and action items, then presents this information in a structured format that agents can review briefly.

## How summaries are generated

The system generates a summary based on the full email activity stream of the interaction, including work notes when available. The summary is displayed in a summary card on the email interaction page.

When an agent is working on an email interaction and needs an on-demand summary, the agent selects **Summarize**. The system generates a summary of the full email activity stream and displays it in the **Interaction Summary** card on the interaction page.

**Note:** Currently, only agent-initiated summarization is supported.

## Summary storage and refresh

Summaries are generated on demand and aren't stored on the interaction record. Each time an agent selects **Summarize**, the system generates a new summary based on the current email thread.

A refresh option is available on the **Interaction Summary** card when new work notes are added after a summary has been generated. The refresh option for emails is not yet available.

## Summary components

The **Interaction Summary** card displays the following components based on the email thread content:

-   **Issue**

    A concise overview of the primary customer concern or request based on the email content, as shown in the **Interaction Summary** card.

-   **Key Actions Taken**

    Actions taken by the agent and customer throughout the email thread.

-   **Next Steps**

    Recommended or identified next steps based on the email conversation.


## AI limitations

When using AI summarization for email interactions, consider the following limitations:

-   AI-generated summaries may not capture all nuances of human communication and should be reviewed by agents for accuracy.
-   Complex technical discussions or specialized terminology may not be fully interpreted by the AI model.
-   Summaries are based on available email content and may not include context from other communication channels.
-   The quality of summaries depends on the clarity and completeness of the original email content.
-   Agents should use AI summaries as a starting point for evaluating email interactions while applying their professional judgment and reviewing original content when necessary.

**Related topics**  


[Using Email Interaction for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/using-email-interaction-customer-service-management.md)

[System properties for configuring Email Interaction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/system-properties-for-configuring-email-as-an-interaction.md)

