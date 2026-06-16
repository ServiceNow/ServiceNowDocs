---
title: Openframe release notes
description: Version history for the CSM Openframe application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-openframe.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Customer Service Management release notes, ServiceNow Store release notes]
---

# Openframe release notes

Version history for the CSM Openframe application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 29.4.0 - June 2026 \(Australia\)**

    Changed in this release: Updated OpenFrame App to v29.4.0.

-   **Version 29.3.1 - May 2026**

    Fixed in this release: Agent presence now syncs correctly to the softphone on initial page load. Previously, the agent's availability state was not applied during initialization, requiring a manual status change to restore sync with CCaaS.

-   **Version 29.3.0 - April 2026 \(Australia\)**

    New in this Release: A new "deviceSettings" capability is available on the Global Call page. Agents can use it to manage speaker and microphone settings for the softphone.

-   **Version 29.2.0 - March 2026 \(Australia\)**
    -   Fixed in this Release:
        -   Resolved a JavaScript vulnerability that allowed client-side sanitization to be bypassed.
        -   Resolved an issue where click-to-dial was creating multiple outbound interactions.
-   **Version 27.2.3 - February 2026 \(Yokohama\)**

    Fixed in this Release: Improvements for Interaction creation and update when using domain separation for OpenFrame REST API

-   **Version 28.2.0 - January 2026**
    -   New in this Release:
        -   OpenFrameAPI - SetICContext includes the following new context for setting the outbound queue selection feature:
            -   setICContext\("idleState"\) - displays the queue selection UI when enabled
            -   setICContext\("agentSettings"\) - sets the default queue option for the agent
        -   Enhanced click-to-dial feature includes outbound queue selection capability when the feature is enabled
-   **Version 28.1.0 - December 2025**

    No updates.

-   **Version 27.2.2 - November 2025**

    Fixed in this Release: Resolved - Partial error handling/logging for failed interaction record retrieval.

-   **Version 28.0.0 - August 2025**
    -   New in this release:
        -   OpenFrame support for Global call list for Interaction Controls Component \(ICC\)
            -   Allows agents to open a non-Interaction tab with call controls available in the Global call list
            -   Allows agents to open Interactions directly from the Global call list via "Open interaction" link
            -   Allows agents to handle phone Interactions with call controls from a non-supported Configurable Workspace
        -   OpenFrame support for call resiliency
            -   Allows CCaaS to deliver phone calls without creating Interactions
        -   OpenFrame support for callback functionality
            -   Allows agents to use Callback Actions \(Call number, Close callback and Retry call\) to manage the lifecycle of callbacks
-   **Version 27.2.1 - July 2025**
    -   Fixed in this Release:
        -   Backward Compatibility: Supports both targetAddress and phoneNumber for an outboundCallInitiated event payload.
        -   Resolved: Phone Log not being created for outgoing calls.
-   **Version 26.11.1 - May 2025**
    -   Fixed in this Release:
        -   Enhanced Interaction Creation and Update: Improved partial error handling when using click-to-call for outbound calls.
        -   Resolved Duplicate Phone Log Issue: Fixed an issue where the PATCH voiceInteraction API was creating duplicate Phone Logs when multiple call IDs were passed as input. This issue could occur in the following scenarios:
            -   Existing Phone Logs have multiple records with the same Call ID, and the latest values are passed via the PATCH API.
            -   New Phone Logs are already created with the same call ID.
-   **Version 26.10.2 - March 2025**
    -   Fixed in this Release:
        -   Improved Interaction creation performance when using click-to-call for outbound calls.
        -   Resolved issue where the Outbound Interaction was not displaying while using click-to-call from a Consumer record.
        -   Aligned OpenFrame events naming convention for event name as per best practice.
        -   Resolved issue when POST voiceInteractionCreationAPI was not creating phone log record.
        -   Resolved issue when PATCH voiceInteraction API was not setting Phone Log and Interaction correctly. This can occur when:
            -   existing Phone Log does not get updated with the latest values passed via PATCH API
            -   new Phone Logs are created with empty field values
            -   short description does not get updated
            -   Interaction does not go to "Closed Complete" status even when PATCH API is invoked with state = closed\_complete
-   **Version 26.10.0 - February 2025**
    -   New in this release:
        -   OpenFrame API
            -   POST REST API to create phone interaction for inbound call via conversation model
            -   PATCH REST API to create phone interaction for inbound call via conversation model
            -   REST API for making outbound phone call
            -   REST API for transfer work item back to the same queue
            -   REST API for creating phone log
            -   REST API for phone log creation for transfer flows
            -   REST API to notify external integration application that User Session is being Extending
            -   OpenFrame getAWAAgentPresence to include available\_to\_receive\_work\_items flag as a parameter
            -   OpenFrame setPresenceIndicator to include available\_to\_receive\_work\_items flag as part of the parameter
    -   OpenFrame Events
        -   OpenFrame cancel transfer event
        -   OpenFrame Wrap-up Event
    -   OpenFrame Configuration
        -   New feature flag name ICC on OpenFrame Config to be passed to a third-party platform
        -   When ICC feature flag on OpenFrame Config is enabled, update the idle state macroponent id
        -   Demo data to include a test OpenFrame Configuration to point to a test Interaction Controls Component \(ICC\) application.
    -   OpenFrame Integration to Interaction Controls Component \(ICC\) - ICC is the new component for a native call controls interface embedded in Agent Workspace. This framework is used by Contact Center platform for voice connector.
        -   Create state context in OpenFrame to read the state of idle and active call state
        -   Create the state context in OpenFrame to read the state of transfer
        -   Provide iframe sandbox parameters to allow iframe access to security features and to enable additional iframe restrictions
        -   Extenstion point to hide the conversation panel when real-time transcription is turned on/off
        -   Extension point to to create and get phone log segments
        -   Click to Dial on CSM Workspace with ICC enabled
    -   Logging and Debugging
        -   Batch the logs on the client side based on the debugging-enabled users
        -   REST API to send client-side batched logs to the server-side
        -   New debug enablement configuration for server-side logging
        -   New ICC Action Logging to OpenFrame component
        -   New openframeLog payload to take in logger\_enabled\_users and the current user details
        -   New server-side logger as a component to the controller to collect the logs from active call UI.
-   **Version 26.6.6 - November 2024**
    -   New in this release:
        -   OpenFrame Client API:
            -   on OpenFrame Accepted Event, a new parameter is introduced for "Auto Accept"
            -   iframe show &amp; hide API to allow for showing or hiding an iFrame within OpenFrame
            -   openFrameAPI.toastMessage can be use to provide warning, error, or info message on Workspace
            -   openFrameAPI.log allows for the client to log different type of warning, error, or info messages in client log
-   **Version 26.3.10 - August 2024**
    -   New APIs in this release
        -   Init function now includes configuration details
            -   Configuration SysID
            -   Configuration Name
            -   Instance URL
            -   OpenFrame Configuration allow for other icons not just phone
            -   OpenFrame can get presence status from user and update third party platform user status
        -   OpenFrame moves from Family to Store Release
-   **Version 26.3.8 - August 2024**

    The interface to integrate external communication systems \(Contact Center Platforms\) with ServiceNow. This plugin brings a UI frame that is accessible and available anywhere on the ServiceNow Platform.


