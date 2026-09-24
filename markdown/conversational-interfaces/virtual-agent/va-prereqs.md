---
title: Prerequisites for enhanced chat
description: Before configuring enhanced chat for ServiceNow Otto for Virtual Agent, your environment must meet the requirements for your deployment channel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/va-prereqs.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Virtual Agent, LLM]
breadcrumb: [Enhanced chat, Chat experiences, Explore, Virtual Agent, Conversational Interfaces]
---

# Prerequisites for enhanced chat

Before configuring enhanced chat for ServiceNow Otto for Virtual Agent, your environment must meet the requirements for your deployment channel.

Requirements differ depending on whether you're deploying enhanced chat in a Service Portal or a mobile app.

## Service Portal

Enhanced chat in a portal includes a resizable chat window and an integrated search experience. To support search, your portal must have AI Search enabled. If you only need the chat experience without search, AI Search is not required, but your portal must include the default chat button widget. The full-page experience is an optional addition to enhanced chat. Both configurations require specific portal widgets to be in place. If you have customized the Faceted Search widget or the Typeahead Search widget, reconcile those customizations with the latest widget versions before you begin configuration.

## Mobile app

Enhanced chat in a mobile app supports three components: a mobile search widget, a chat launcher, and a custom app built with the Mobile SDK. Prerequisites and available capabilities vary by component. The mobile search widget supports the full-page experience only and requires a mobile search configuration. The chat launcher and custom app support native Virtual Agent with ServiceNow Otto for Virtual Agent responses.

**Note:** The AI Search experience is not available in custom apps.

For component-specific prerequisites, see [Portal prerequisites for enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/prerequisites-enhanced-chat.md) and [Mobile app prerequisites for enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/mobile-prereqs-enhanced-chat.md).

