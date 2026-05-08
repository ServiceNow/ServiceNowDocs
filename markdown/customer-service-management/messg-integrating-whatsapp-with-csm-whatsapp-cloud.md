---
title: Integrating WhatsApp with Customer Service Management using the WhatsApp Cloud API
description: Use WhatsApp messaging with Customer Service Management to enable direct communication with customers through WhatsApp using the WhatsApp Cloud API.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integrating with consumer messaging apps, Integrate, Customer Service Management]
---

# Integrating WhatsApp with Customer Service Management using the WhatsApp Cloud API

Use WhatsApp messaging with Customer Service Management to enable direct communication with customers through WhatsApp using the WhatsApp Cloud API.

This WhatsApp direct integration connects to Meta’s WhatsApp business platform and enables agents to provide real‑time customer support with rich media, interactive controls, and full CSM workflow integration.

The WhatsApp channel supports both automated conversations through Virtual Agent and live agent interactions through Agent Workspace, providing a complete customer service experience.

## WhatsApp messaging capabilities

WhatsApp messaging capabilities in Customer Service Management enable rich, interactive customer conversations beyond basic text messaging. Agents can exchange media files, send structured interactive controls, request customer inputs, and deliver formatted messages that improve clarity and reduce friction.

## Rich and interactive messaging features

WhatsApp supports the following messaging features and rich interactive controls:

-   Text messaging
-   Rich media \(images, videos, audio files, documents\)
-   Typing indicators
-   Location sharing
-   List pickers
-   Opt-in and consent

<table id="table_vlk_ykh_shc"><thead><tr><th>

Rich controls

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Typing indicators

</td><td>

Real-time visual feedback shows when agents or customers are composing messages, keeping both parties informed about conversation activity.Agent-side capabilities:

-   Automatically displayed to customer when agent types in Agent Workspace
-   Appears as "typing..." status in customer's WhatsApp
-   Provides immediate feedback that agent is responding

</td></tr><tr><td>

Message status indicators

</td><td>

WhatsApp automatically handles message delivery and read status indicators according to WhatsApp's standard behavior. The application displays these statuses in the interaction timeline.Status indicators \(for users\):

-   Sent: Single gray checkmark \(message sent to WhatsApp server\)
-   Delivered: Double gray checkmarks \(message delivered to agent’s device\)
-   Read: Double blue checkmarks \(agent viewed message\)

Status indicator \(for agent\):

Sent: Single gray checkmark \(message sent to user’s device\)

</td></tr><tr><td>

Link previews

</td><td>

URLs in messages automatically generate rich previews with images, titles, and descriptions.

</td></tr><tr><td>

Customer-initiated conversations

</td><td>

These conversations begin when the customer sends the first message to your business. WhatsApp applies specific rules for messages sent within this interaction window.Messaging window:

-   Opens when customer sends first message
-   Remains open for 24 hours from last customer message
-   Resets to 24 hours with each new customer message
-   Agent can send any messages within this window

Characteristics:

-   No restrictions on message content
-   Supports all message types and interactive features
-   Most common conversation type for customer serviceOpens when customer sends first message

</td></tr><tr><td>

Agent-initiated conversations

</td><td>

These conversations begin when agent proactively messages the customer. WhatsApp enables outbound initiation only under certain conditions.Requirements:

-   Customer must have active channel user profile in the application
-   Customer must have opted in to receive messages
-   Customer's phone number must be valid and registered on WhatsApp
-   Must be within 24 hours of customer's last message

</td></tr><tr><td>

System-initiated conversations

</td><td>

These conversations begin when an automated workflow sends a WhatsApp message to the customer.Requirements:

-   Customer must have opted in
-   Must be within 24 hours of customer's last message

</td></tr><tr><td>

Opt-in and consent

</td><td>

The integration captures and records customer opt-in and opt-out messages to track communication consent.

</td></tr></tbody>
</table>## End users and roles

The users with the roles listed in the following table can use the Conversational Integration with WhatsApp \(WhatsApp Cloud API\) application.

|Role|Tasks|
|----|-----|
|admin|Configure and manage the WhatsApp Cloud API integration, including connection settings, routing rules, system properties, and security configurations.|
|agent\_workspace\_user|Accept an ongoing WhatsApp chat conversation with a customer through the WhatsApp service channel in Advanced Work Assignment.|
|sn\_customerservice\_manager|View details of a WhatsApp chat conversation by using interaction records of type Messaging and subtype WhatsApp.|
|sn\_customerservice.consumer, sn\_customerservice.customer|Initiate WhatsApp chat conversations with a Virtual Agent or live agent so that you can search for articles in Communities and Knowledge Management, access service catalogs, and create a customer service case.|

**Related topics**  


[System properties for configuring WhatsApp \(WhatsApp Cloud API\)](direct-cloud-api-system-property-configuration.md)

[bundle-convint.messg-direct-whatsapp-configure]

[bundle-convint.messg-direct-whatsapp-using]

