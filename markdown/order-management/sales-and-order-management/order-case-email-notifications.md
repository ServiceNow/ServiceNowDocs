---
title: Email notifications for order cases
description: The manage order operations AI agent sends automated emails to your B2B customers when an order case is opened from a Business Portal chat conversation and when the order case is closed with a successful resolution. The Manage Order Operations application includes two default email templates that you can customize.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-and-order-management/order-case-email-notifications.html
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-05-19"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Now Assist for Order Management, Sales Customer Relationship Management]
---

# Email notifications for order cases

The manage order operations AI agent sends automated emails to your B2B customers when an order case is opened from a Business Portal chat conversation and when the order case is closed with a successful resolution. The Manage Order Operations application includes two default email templates that you can customize.

The manage order operations AI agent uses default email templates to keep customers informed at key points in the order case life cycle when the customer initiates an order exception request from the chat assistant on the Business Portal.

**Note:** Email notifications aren't sent for order cases that the AI voice agent creates. If your customer creates an order case by using the voice assistant, the order case agent provides the case number over the call.

|Email template name|When the email is sent|What the email includes|
|-------------------|----------------------|-----------------------|
|ordercase.opened.for.customer|When the manage order operations AI agent opens a new order case for the customer from a Business Portal chat conversation.|The order case number and a link that the customer can use to view the case on the Business Portal.|
|order.exception.case.closed|When the order case is closed and resolved successfully.|The order case number, the resolution details, and the quote details when a quote was generated for the case.|

To customize the subject, content, or formatting of these default email templates, see [Apply a template to an email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_ApplyATemplateToAnEmailNotif.md).

The application scope must be set to Manage Order Operations. You can change the application scope using the application picker \[Omitted image "globe-outline-24.svg"\] Alt text: in the Unified Navigation bar.

**Parent Topic:**[Configuring Now Assist for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/now-assist-for-order-management-configuring.md)

**Related topics**  


[Email templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/c_EmailTemplates.md)

