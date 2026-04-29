---
title: Automating system responses to inbound email
description: Save time from responding to emails manually when you configure your instance to send replies, create incidents, or update records automatically in response to inbound emails.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Inbound email, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Automating system responses to inbound email

Save time from responding to emails manually when you configure your instance to send replies, create incidents, or update records automatically in response to inbound emails.

You can define system responses to inbound emails in two ways:

-   Create an inbound email flow in Workflow Studio
-   Script an [inbound email action](c_InboundEmailActions.md)

## Inbound email trigger in Workflow Studio

With the inbound email trigger in Workflow Studio, you can create flows that define the automated processes that your instance takes when it receives an email.

Inbound email flows take priority over inbound email actions. If you create flows with inbound email triggers, emails are first processed by the inbound email triggers before they are processed by inbound email actions.

The following diagram shows the processing order for inbound emails. When an email is sent to your instance, the system first classifies the email as a reply, forward, or new email. Then the system runs the inbound email through an inbound email flow. If the flow issues stop processing, the email is finished being processed. If the flow does not issue stop processing, the system tries to match the email to another inbound email flow. If at any point the email does not match with an inbound email flow, the system matches the email to an inbound email action instead.

![Processing order for inbound emails](../image/inbound-email-diagram.png "Processing order for inbound emails")

The benefits to automating system responses to inbound emails in Workflow Studio are:

-   Provides an easy and accessible interface that uses natural language.
-   Consolidates configuration and runtime information into a single environment so process owners and developers can create, operate, and troubleshoot flows from a single interface.
-   Reduces upgrade costs, with upgrade-safe ServiceNow AI Platform logic replacing complex custom script.
-   Reduces development costs by providing a library of reusable actions.

For more information on creating inbound email flows in Workflow Studio, see [Workflow Studio flow trigger types](https://www.servicenow.com/docs/access?context=flow-triggers&version=australia&pubname=australia-build-workflows&ft:locale=en-US) or follow the steps in [Create a flow with an inbound email trigger](https://www.servicenow.com/docs/access?context=create-inbound-email-flow&version=australia&pubname=australia-build-workflows&ft:locale=en-US). To view or manage your inbound email flows, navigate to **Flow Designer** &gt; **Inbound Email Flows**.

