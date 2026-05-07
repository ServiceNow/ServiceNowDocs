---
title: How Proactive Triggers work
description: Explore example use cases and how information flows through the Proactive Triggers process.
locale: en-US
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Proactive Triggers, Proactive Triggers, Manage people and work, Conversational Interfaces]
---

# How Proactive Triggers work

Explore example use cases and how information flows through the Proactive Triggers process.

## Proactive Triggers use cases

Proactive Triggers are useful in various scenarios. Explore the following example use cases to determine how to use Proactive Triggers effectively for your organization.

-   An admin creates a Proactive Triggers rule that runs when a user views a Knowledge article containing the keyword “VPN” \(or any other keyword that has a matching Virtual Agent topic\). The admin configures the rule to run the VPN Connectivity Virtual Agent conversation, which proactively helps the user resolve the VPN issues.

-   An admin creates a Proactive Triggers rule that runs when a user views any catalog item with a short description that includes a specific keyword, such as “laptop.” The admin configures the rule to connect the user to a live agent, using the Live Agent Support topic, which proactively helps the user get assistance in ordering a laptop.

You can also use Proactive Triggers to engage with customers in more complex scenarios. Admin users can create multiple rules using different delay times and different user criteria to create a customized user experience. For more information about configuring more complex scenarios, see [Multiple Proactive Triggers rules and actions](multiple-rules-and-actions.md).

## Proactive Triggers process

1.  Whenever an end user navigates to a Proactive Triggers enabled page, Proactive Triggers reads the page URL or called API to determine if any Proactive Triggers rules should run.
2.  During this analysis, Proactive Triggers determines the Trigger Type source.

    |Web browsing \(client side\)|Trigger type|
    |----------------------------|------------|
    |Knowledge Base pages|Knowledge|
    |Service Catalog pages|Catalog Item|
    |Portal home pages|Portal Home|
    |All other portal pages|URL|

    |System API \(server side\)|Trigger type|
    |--------------------------|------------|
    |Search event on portal pages|Search Event|

3.  Next, Proactive Triggers evaluates all the Proactive Triggers rules for that Trigger Type one by one until a matching rule is found.

    **Note:** Rules are created with the required fields **Delay Time** and **Order**. During the rule matching process, rules are analyzed in ascending Order, according to the order number assigned. If the Delay Time is reached before the order number, the Delay Time takes precedent.

4.  After a Proactive rule has been matched, the rule's actions are evaluated one by one. This evaluation proceeds in ascending order, according to the **Order** field in the associated Proactive actions. As part of this process, the **Applies To** field is compared with the user visiting the page to determine if the action applies to this user.
5.  After Proactive Triggers identifies at least one rule and action that apply to the visiting user and the Delay Time has been met, a pop-up message appears directly on the web page. The contents of this message are configured by the admin for the matched action.
6.  If the user selects the pop-up message, the chat widget opens. If the matched action is of the type **Virtual Agent Topic**, the chat widget also runs the topic configured in that action.

