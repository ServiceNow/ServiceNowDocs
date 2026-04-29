---
title: Recommended Actions in the chat interaction record
description: The Recommended Actions feature is available by default in the contextual side panel for chat interaction records.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Recommended Actions for Service, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Recommended Actions in the chat interaction record

The Recommended Actions feature is available by default in the contextual side panel for chat interaction records.

This feature appears as the first tab in the contextual side panel and is available for interactions of type chat.

The Recommended Actions feature is enabled by default for new \(zboot\) customers. This feature replaces Agent Assist, which is disabled from the contextual side panel.

The Recommended Actions feature includes two tabs:

-   Recommendations: displays relevant actions based on the context of the chat interaction record.
-   Search: displays relevant search results based on the short description of the chat interaction record.

## hideAgentAssistShowRA UX page property

Enabling Recommended Actions for chat interaction records is controlled by the **hideAgentAssistShowRA** UX page property, which is only available for new customers.

Existing customers that want to disable Agent Assist in the contextual side panel and enable Recommended Actions can create this UX page property.

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Experiences**.
2.  Select CSM/FSM Configurable Workspace.
3.  Select **New** in the UX Page Properties related list.
4.  Create the property with the following values:
    1.  Name: hideAgentAssistShowRA
    2.  Type: true \| false
5.  Set the property to true.
6.  Select **Save**.

## Recommended Actions component contextSysId property

The Recommended Actions \(RA\) component includes the contextSysId property, which determines the rules and data sources that are evaluated to provide recommendations and search results. This property is automatically set to the default context for case records and displays accurate recommendations and search results on the Front-line case page.

This change to the contextSysId property only applies to new customer instances where the Recommended Actions component is added to the Front-line case page. Existing customers are not impacted.

