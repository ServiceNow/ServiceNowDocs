---
title: Tutorial: Route interactions by context
description: Learn how you can configure Advanced Work Assignment to route conversations to agents according to the context of the conversation.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure reasons for rejecting work items, Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Tutorial: Route interactions by context

Learn how you can configure Advanced Work Assignment to route conversations to agents according to the context of the conversation.

Activate the Customer Service Management Demo Data \(com.snc.customerservice.demo\) plugin.

A basic understanding of context variables is required. For more information on context variables, see [Virtual Agent scripts](../../virtual-agent/concept/virtual-agent-scripts.md).

The **What can we help you with?** record producer is available by default with the Customer Service Management Demo Data \(com.snc.customerservice.demo\) plugin. In the record producer, chat requesters can specify one of three issue categories that they need help with:

-   Product
-   Billing
-   Order

Whichever category they select passes a value through the *liveagent\_csp\_category* context variable. Learn how to create queues that route conversations to agents according to the values passed through this context variable.

