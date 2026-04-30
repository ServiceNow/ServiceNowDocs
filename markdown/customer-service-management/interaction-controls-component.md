---
title: Interaction Controls Component
description: Interaction Controls Component \(ICC\) is a component that allows for a native call controls interface embedded in Agent Workspace.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# Interaction Controls Component

Interaction Controls Component \(ICC\) is a component that allows for a native call controls interface embedded in Agent Workspace.

-   Create state context in OpenFrame to read the state of idle and active call state
-   Create the state context in OpenFrame to read the state of transfer
-   Provide iframe sandbox parameters to allow iframe access to security features and to enable additional iframe restrictions
-   Create an extension point implementation to hide the conversation panel when real-time transcription is turned on/off
-   Create an extension point implementation to create and get phone log segments
-   Implement Click to Dial on CSM Workspace with ICC enabled
-   Seismic event emitted to the Polaris shell via Active call component when any action clicked related to the transfer component
-   Screen pop for Interaction should be available on Dialpad and Click-to-call outbound call
-   sn\_openframe.create\_interaction will be ignored when using ICC. All inbound and outbound calls will have interactions created.

Use Interaction Controls Component \(ICC\) and OpenFrame to integrate with the voice channel for contact centers. For more information, see [Interaction Controls Component \(ICC\) for voice calls](contact-center-integration-with-icc.md).

