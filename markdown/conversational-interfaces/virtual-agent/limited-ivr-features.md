---
title: Unsupported Virtual Agent features in Conversational IVR
description: A few user input controls used in Virtual Agent Designer are unsupported in Conversational IVR - enabled topics.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrating Virtual Agent with Conversational IVR, Integrating Virtual Agent with Voice channels, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Unsupported Virtual Agent features in Conversational IVR

A few user input controls used in Virtual Agent Designer are unsupported in Conversational IVR - enabled topics.

## Unsupported Virtual Agent Designer controls

Within the Virtual Agent topic flow, there are a few controls that are not supported for Conversational IVR.

-   User input controls:
    -   Grouped Choice
    -   File Picker
-   Bot response controls:
    -   Image
    -   Link
    -   HTML
    -   Multi-response
    -   Script
    -   Card

        **Note:** The Card control is supported but Conversational IVR will not read all the parts or elements of the card, if the card's subtitle contains incident numbers, request numbers, and so on, such as `INC0001`, `RITM0001`, `HRC0001`. IVR is configured to read only the number in such cases.

    -   Table
    -   Video

Conversational IVR is designed to silently skip the execution of unsupported controls within the topic flow and to move to the next supported control for execution.

The system is designed to provide warnings when you pick an unsupported control for your topic flow while crating the topic. For example, you can trigger a warning message by adding File picker to your topic flow for a topic that has IVR enabled.

![Warning messages for unsupported controls used in creating topic flows for IVR enabled topics.](../images/ivr-unsupported-topic-control-wrng.png)

For information about the supported controls to be used for Conversational IVR, see [Input Collector user input control](va-ai-data-collector.md).

