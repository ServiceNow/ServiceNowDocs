---
title: Email reply linking for closed interactions
description: When a customer replies to an email associated with a closed interaction, Email Interaction automatically links the reply to the correct open case or interaction without creating a duplicate interaction or requiring agent intervention.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/email-reply-routing-closed-interactions.html
release: australia
topic_type: concept
last_updated: "2026-05-11"
reading_time_minutes: 3
keywords: [email reply routing, closed interactions, email routing]
breadcrumb: [Using Email Interaction for CSM, Customer communication, Use, Customer Service Management]
---

# Email reply linking for closed interactions

When a customer replies to an email associated with a closed interaction, Email Interaction automatically links the reply to the correct open case or interaction without creating a duplicate interaction or requiring agent intervention.

The closed interaction is not reopened as part of this process.

## How the system processes the reply

When the system receives an inbound email that references a closed interaction, it evaluates related records in the following order:

1.  The system checks for open interactions related to the closed interaction. If exactly one open interaction exists, the reply is linked to it.
2.  If no open interaction exists, the system checks for open cases. If exactly one open case is associated with the closed interaction, the reply is linked to that case.
3.  If multiple open cases are associated with the closed interaction, the system uses an AI skill to match the reply to the most relevant case. The skill evaluates each case's short description, comments, and the latest five emails, and applies keyword matching. The skill returns the case with the highest confidence score.
4.  If the highest confidence score is 85% or above, the reply is linked to the matched case. If all scores are below 85%, or the AI skill is not active, the reply is linked to the most recently opened case.

    **Note:** The Contextual Email Matching skill must be activated for AI-based case matching to work. For activation steps, see [Activate contextual email matching for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/activate-contextual-email-matching-csm.md).

5.  If no open interactions or cases exist, the system creates an interaction and stores a reference to the original closed interaction.

## Case types

The routing logic applies to both standard cases and extended case types. All records in the case table hierarchy that are associated with the closed interaction are included in the evaluation.

## Email threading

The system uses watermarks and reference IDs embedded in outbound email threads to identify whether an inbound email is a reply to an existing thread. Only emails identified as replies to an existing thread follow this routing logic.

## Agent notification

When a reply is linked to an open case, the agent assigned to that case receives a notification via the bell icon in the CSM Configurable Workspace. Notifications are sent regardless of which valid open state the case is in. The reply appears in the case activity stream.

For a complete list of routing scenarios and system actions, see [Email reply linking scenarios for closed interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/eaai-email-reply-linking-scenarios.md).

**Related topics**  


[Email reply linking scenarios for closed interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/eaai-email-reply-linking-scenarios.md)

[Using Email Interaction for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/using-email-interaction-customer-service-management.md)

[System properties for configuring Email Interaction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/system-properties-for-configuring-email-as-an-interaction.md)

