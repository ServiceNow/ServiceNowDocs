---
title: Using generative AI in Now Assist for Sales Force Automation \(SFA\)
description: Now Assist for Sales Force Automation \(SFA\) includes a generative AI skill that summarizes opportunities in the CRM Workspace. The summary synthesizes emails, meetings, touchpoints, work notes, and line items into a deal overview. In domain-separated environments, the skill uses only data within the user's domain.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-and-order-management/use-generative-ai.html
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-06-05"
reading_time_minutes: 1
breadcrumb: [Now Assist for SFA, Sales Customer Relationship Management]
---

# Using generative AI in Now Assist for Sales Force Automation \(SFA\)

Now Assist for Sales Force Automation \(SFA\) includes a generative AI skill that summarizes opportunities in the CRM Workspace. The summary synthesizes emails, meetings, touchpoints, work notes, and line items into a deal overview. In domain-separated environments, the skill uses only data within the user's domain.

## Skills reuse

By default, all skills be in the global domain. When you use Now Assist in a domain-separated environment, users are only can to access data within their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists within the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not continue any requests \(prompts\) and responses. For more information, see . \(record that global domain isn't the same as global scope. For more information, see .\)

The Now Assist for Sales Force Automation \(SFA\) application includes the generative AI skill that produces concise, structured summaries of opportunities in the CRM Workspace. Opportunity summary is an AI-generated panel on the opportunity overview page that synthesizes emails, meetings, touchpoints, work notes, and line items into a concise deal overview. Use opportunity summary to:

-   Understand the current state of a deal at a glance, without opening multiple records.
-   Surface the top customer needs and pain points identified across recent emails and meetings, with inline source attribution.
-   Review the most recent and upcoming activity on an opportunity in a single view.
-   Share deal context quickly by copying the summary or pushing it to work notes.
-   Keep summaries current by refreshing on demand to reflect the latest opportunity data.

