---
title: \(Legacy\) Exploring Conversational IVR with Amazon Connect
description: Use this application to build an integration with Amazon Connect. This allows your users to initiate an IVR \(Interactive Voice Response\) conversation with Virtual Agent. This integration also allows the user to connect with an agent using Advanced Work Assignment \(AWA\) over SoftPhone.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/exploring-conv-ivr-amazon-connect.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Conversational IVR with Amazon Connect, Integrate VA for NLU with voice channels, Virtual Agent channel integrations, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Exploring Conversational IVR with Amazon Connect

Use this application to build an integration with Amazon Connect. This allows your users to initiate an IVR \(Interactive Voice Response\) conversation with Virtual Agent. This integration also allows the user to connect with an agent using Advanced Work Assignment \(AWA\) over SoftPhone.

## Conversational IVR with Amazon Connect overview

-   Use Virtual Agent topics as a Conversational IVR to enable deflection in Phone channels, providing consistent end-user experience.
-   Enable true-omnichannel flow including routing Phone to the Conversational VA-IVR.
-   In case of escalations, route calls smoothly to live agents using AWA via conversational infrastructure.

To get started, see [\(Legacy\) Install Conversational IVR with Amazon Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/install-va-ivr.md).

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

\[Omitted image "ivr-unsupported-topic-control-wrng.png"\] Alt text: Warning messages for unsupported controls used in creating topic flows for IVR enabled topics.

For information about supported controls, see [Input Collector user input control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-ai-data-collector.md).

**Parent Topic:**[\(Legacy\) Conversational IVR with Amazon Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-ivr-voice.md)

