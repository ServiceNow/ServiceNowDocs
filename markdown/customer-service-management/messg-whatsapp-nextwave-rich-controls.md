---
title: Use rich messaging controls in WhatsApp on NextWave
description: Use Request Location, List Picker, and Typing Indicator controls in WhatsApp conversations on the NextWave off-Glide architecture.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/messg-whatsapp-nextwave-rich-controls.html
release: brazil
topic_type: task
last_updated: "2026-09-18"
reading_time_minutes: 1
keywords: [WhatsApp, rich messaging, Request Location, List Picker, Typing Indicator, NextWave]
breadcrumb: [WhatsApp on NextWave, Integrating with consumer messaging apps, Integrate, Customer Service Management]
---

# Use rich messaging controls in WhatsApp on NextWave

Use Request Location, List Picker, and Typing Indicator controls in WhatsApp conversations on the NextWave off-Glide architecture.

## Before you begin

Role required: **sn\_customerservice\_agent**

The WhatsApp Direct Integration channel must be configured and active on your instance.

## About this task

The WhatsApp Cloud API supports rich messaging controls that go beyond basic text. These controls are available on NextWave off-Glide with functional parity to the Glide-based implementation.

## Procedure

1.  Request Location
2.  During a conversation, use the Request Location control to prompt the customer to share their location.

    The customer receives a location-sharing prompt in WhatsApp. When the customer shares their location, the data appears as a location pin in the agent interface within the interaction record.

3.  List Picker
4.  Configure a List Picker control to present a set of selectable options to the customer during a conversation.

    The List Picker renders in the customer's WhatsApp app as a native selection interface. Customer selections are captured and stored in the interaction record.

5.  Typing Indicator
6.  The Typing Indicator displays automatically in the customer's WhatsApp app when an agent is typing a response.

    No manual configuration is required for the Typing Indicator. When an agent types in the CRM Workspace, the indicator appears on the customer side through the NextWave off-Glide pipeline.


## Result

Rich messaging controls operate through the NextWave off-Glide pipeline with functional parity to the Glide-based implementation. Location data, selection data, and interaction history are preserved in the interaction record.

