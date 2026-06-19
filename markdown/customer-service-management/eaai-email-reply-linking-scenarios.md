---
title: Email reply linking scenarios for closed interactions
description: Describes how Email Interaction links a customer email reply when the reply references a closed interaction. The system evaluates conditions in the order listed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/eaai-email-reply-linking-scenarios.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: reference
last_updated: "2026-05-11"
reading_time_minutes: 1
keywords: [email reply linking, closed interactions, routing scenarios]
breadcrumb: [Email Interaction for CSM reference, Reference, Customer Service Management]
---

# Email reply linking scenarios for closed interactions

Describes how Email Interaction links a customer email reply when the reply references a closed interaction. The system evaluates conditions in the order listed.

|Scenario|Condition|System action|
|--------|---------|-------------|
|One open interaction|A single open interaction is related to the closed interaction.|Links the email to the open interaction. No new interaction is created.|
|One open case|A single open case is associated with the closed interaction.|Links the email to the open case. No new interaction or case is created.|
|Multiple cases, one open|Multiple cases are linked to the closed interaction; only one is open.|Links the email to the open case. Closed cases remain unchanged.|
|Multiple open cases|Multiple open cases are linked to the closed interaction.|The AI skill retrieves each case's short description, latest five emails, and comments, and applies keyword matching. The email is linked to the case with the highest confidence score at or higher than 85%.|
|Multiple open cases, low confidence|Multiple open cases exist; the AI skill returns a confidence score lower than 85% for all cases, or the skill is inactive.|Email is linked to the most recently opened case as a fallback.|
|No open records|No open interactions or cases are associated with the closed interaction.|A new interaction is created. A reference to the original closed interaction is stored on the new interaction.|

## Linking behavior

-   The original closed interaction is not reopened, regardless of scenario.
-   No new interaction or case is created when a valid open record is identified.
-   Extended case types are included in the evaluation and standard cases.

