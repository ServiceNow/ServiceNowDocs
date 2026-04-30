---
title: Exploring Conversational IVR with Amazon Connect
description: Use this application to build an integration with Amazon Connect. This allows your users to initiate an IVR \(Interactive Voice Response\) conversation with Virtual Agent. This integration also allows the user to connect with an agent using Advanced Work Assignment \(AWA\) over SoftPhone.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Conversational IVR with Amazon Connect, Integrating Virtual Agent with Voice channels, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Exploring Conversational IVR with Amazon Connect

Use this application to build an integration with Amazon Connect. This allows your users to initiate an IVR \(Interactive Voice Response\) conversation with Virtual Agent. This integration also allows the user to connect with an agent using Advanced Work Assignment \(AWA\) over SoftPhone.

## Conversational IVR with Amazon Connect overview

-   Use Virtual Agent topics as a Conversational IVR to enable deflection in Phone channels, providing consistent end-user experience.
-   Enable true-omnichannel flow including routing Phone to the Conversational VA-IVR.
-   In case of escalations, route calls smoothly to live agents using AWA via conversational infrastructure.

To get started, see [Install Conversational IVR with Amazon Connect](../task/install-va-ivr.md).

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

For information about supported controls, see [Input Collector user input control](../reference/va-ai-data-collector.md).

**Parent Topic:**[Conversational IVR with Amazon Connect](va-ivr-voice.md)

