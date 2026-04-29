---
title: Notifications for resolved cases
description: Customers receive notifications about resolved cases that are automatically closed if no action is taken.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automatically close customer service cases, Administer, Customer Service Management]
---

# Notifications for resolved cases

Customers receive notifications about resolved cases that are automatically closed if no action is taken.

When an agent proposes a solution for a customer service case, the customer has a time window in which to accept or reject the solution. If the customer doesn’t take action within this window, the case is automatically closed.

The system administrator can configure the settings for the notifications that are sent to the customer. The default settings include two notifications that are sent at 5 days and 10 days after a case has been resolved.

-   After 5 days, the customer receives a reminder message about the resolved case on the Customer Service Portal: **This case is pending solution acceptance. It will be auto closed if you do not take action.**
-   If the customer doesn’t take any action after 10 days, the system automatically closes the case and adds the following message to the case: **This case was auto closed.**

This feature uses the **Auto Close Resolved Cases** Flow Designer flow. For more information, see [Automatically close customer service cases](auto-close-customer-service-case.md).

**Note:** The **Auto Close Resolved Cases** flow isn’t active by default.

