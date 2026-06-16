---
title: ServiceNow Voice with Amazon Connect release notes
description: Version history for the ServiceNow Voice with Amazon Connect application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-servicenow-voice-amazon-connect.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 7
breadcrumb: [ServiceNow Voice, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# ServiceNow Voice with Amazon Connect release notes

Version history for the ServiceNow Voice with Amazon Connect application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 5.3.0 - June 2026**
    -   New in the release: SAML 2.0 SSO with third-party identity providers — Agents can now sign in to Amazon Connect via SAML 2.0 SSO using third-party IdPs such as Okta or Ping Federate
    -   Fixed in the release:
        -   More reliable call recordings — Voice recording playback and recording links in phone logs are now consistent across deployment environments.
        -   Smoother transfer experience — Real-time text messages and the Inbox alert card \(with Interaction Call Controls\) behave correctly during agent-to-agent transfers.
        -   Improved agent setup and device selection — Device Settings reliably lists available audio devices, and the AWA Routing toggle stays in sync with the setup guide.
-   **Version 5.2.3 - May 2026**
    -   New in the release:
        -   Improved handling of abandoned calls via Amazon EventBridge — When a call is placed and ended before the connection is made, the event is now detected and processed in real time using Amazon EventBridge. The interaction record is updated to a Closed Abandoned state and the Inbox Alert Card is removed for agents using AWA routing.
        -   VDI Support - Contact center agents in virtualized desktop environments can now access full ServiceNow Voice with Amazon Connect functionality, delivering a consistent, high-quality voice experience for remote and hybrid workforces.
        -   Outbound Call – Alphanumeric Keypad Input Support - Users can now enter alphabetic characters when dialing outbound calls, mapping letter inputs to their corresponding keypad digits.
-   **Version 5.2.0 - April 2026**
    -   New in the release:
        -   Device Settings Management — When interaction controls are enabled, agents can now manage speaker, microphone, and ringer device selections directly from the agent settings panel.
        -   Improved handling of abandoned calls via Amazon EventBridge — When a call is placed and ended before the connection is made, this event is now detected and processed in real time using Amazon EventBridge. The interaction record is updated to a Closed Abandoned state and the Inbox Alert Card is removed for agents using AWA routing.
    -   Fixed in the release: Optimized After Call Work \(ACW\) timeout retrieval — When interaction controls are enabled, ACW timeout configuration is now cached and only refreshed periodically, reducing unnecessary server calls during agent login.
-   **Version 5.1.0 - March 2026**

    Release notes: Minor bug fixes.

-   **Version 5.0.0 - February 2026**
    -   New in this Release:
        -   Integrated Amazon Connect with ServiceNow native voice controls in Interaction page.
            -   Call controls includes hold, mute, disconnect, and transfer
            -   Agent Login and Logout controls for Amazon Connect
            -   Global call list provide agent access to call controls outside of supported Workspace
            -   Inbound and outbound call flows with automatic Interaction creation.
            -   Agent presence bi-directional sync with Amazon Connect
    -   Fixed in this Release: Interaction state is now set to "Closed Abandoned" when the customer disconnects the call before engaging with an Agent.  Previously, the state was set to "Closed Complete"
-   **Version 4.7.7 - September 2025**

    Fixed in this release: The "agentResponse is not defined" error no longer occurs for conversations of type sn\_openframe\_phone\_log.

-   **Version 4.7.5 - August 2025**
    -   Fixed in this release:
        -   Setup Guide updates to resolve the issue with Lex Bot import failing during the creation step
        -   A new lex.json.zip file to create LEX V2 bots
        -   Upgrade to Node.js V22
-   **Version 4.7.3 - January 2025**

    Fix in this release: When manager monitors an interaction on the Call Analysis tab, the Assignment Group will not be changed when the manager exits the interaction.

-   **Version 4.5.7 - January 2025**

    Fix in this release: Previously the interaction was assigned to the manager when the manager monitored the interaction in the call analysis tab. With this update, the interaction will stay assigned to the agent to preserve agent ownership of the interaction.

-   **Version 4.7.0 - November 2024**

    New in this release: Call summarization: Support for outbound call and support when real time transcript is not available.

-   **Version 4.5.5 - November 2024**

    Fixed in this release: If a second agent joins the call and then disconnects from a call while the first agent is still on the call, the assigned\_to of the interaction does not get overwritten.

-   **Version 4.6.0 - August 2024**
    -   Fixed minor issues
    -   Minor improvements
-   **Version 4.5.3 - April 2024**

    Minor fixes.

-   **Version 4.0.5 - March 2024**

    Fixed: Japanese language support for Real Time Transcription is now available.

-   **Version 4.5.1 - March 2024**

    Fixed: Japanese language support for Real Time Transcription is available.

-   **Version 4.5.0 - February 2024**
    -   New:
        -   Voice calls from Amazon Connect can now be routed by ServiceNow Advanced Work Assignment \(AWA\)
        -   The setup guide includes an option for Amazon Connect Contact Contact Flows to use AWA Voice Routing
-   **Version 4.0.4 - January 2024**

    Fixed: This version now uses the latest version of Amazon Connect Streams API. This update enables customers to continue using CCP integration after Google Chrome blocks third-party cookies in 2024. Please note that Google Chrome requires you to authorize cookies on the browser to use CCP. For more information, refer to the AWS documentation: https://docs.aws.amazon.com/connect/latest/adminguide/3pcookies.html.

-   **Version 4.0.3 - December 2023**

    Fixed: This version allows Node.js to be upgraded to Node.js v18 to support AWS Lambda.

-   **Version 4.0.2 - August 2023**
    -   Changes:
        -   Supporting Real Time Transcription.
        -   Support agent to agent call transfers.
        -   Support agent to queue call transfers.
        -   Changes done to support Outbound Calls \(manual dial\).
-   **Version 3.1.3 - February 2023**

    Fixed: minor changes.

-   **Version 3.1.0 - August 2022**

    Fixed: Minor bug fixes for i18n.

-   **Version 3.0.0 - March 2022**

    New: Amazon Connect for Cloud Call center is now ServiceNow Voice with Amazon Connect.

-   **Version 2.0.5 - February 2022**

    New: Amazon Connect for Cloud Call center is now ServiceNow Voice with Amazon Connect.

-   **Version 2.0.3 - August 2021**
    -   New:
        -   Updated cloud formation template to support Lambda with node.js 14.x version runtime.
        -   Support for Phone Channel Analytics using AWA work items and Workforce Optimization \(starting Paris\)Outbound calling support with Flow Templates to quickly run outbound calling
        -   Surfacing Transcription, Recording, and Customer Sentiment Analysis in Workspace
        -   Support for Instance Parameters to configure each amazon connect instance with custom parameters when first registering an Instance.
    -   Changed:
        -   While first registering the connect instance, you can provide a ccpHost and ccpURL if the amazon connect domain for your instance is not the latest one.
        -   Support for upcoming aws domain change to "my.connect.aws"
        -   Updated setup guide Home step to point to Documentation website for latest video
    -   Fixed: Issues with Setup Guide when glide.ui.escape\_all\_script is set to false
-   **Version 2.0.2 - February 2021**
    -   New:
        -   Support for Phone Channel Analytics using AWA work items and Workforce Optimization \(starting Paris\)
        -   Outbound calling support with Flow Templates to quickly run outbound calling
        -   Surfacing Transcription, Recording, and Customer Sentiment Analysis in Workspace Support for Instance Parameters to configure each amazon connect instance with custom parameters when first registering an Instance.
    -   Changed: While first registering the connect instance, you can provide a ccpHost and ccpURL if the amazon connect domain for your instance is not the latest one. Support for upcoming aws domain change to "my.connect.aws" Updated setup guide Home step to point to Documentation website for latest video
    -   Fixed: Issues with Setup Guide when glide.ui.escape\_all\_script is set to false
-   **Version 2.0.1 - December 2020**
    -   New:
        -   Support for Phone Channel Analytics using AWA work items and Workforce Optimization \(starting Paris\)
        -   Outbound calling support with Flow Templates to quickly run outbound calling
        -   Surfacing Transcription, Recording, and Customer Sentiment Analysis in Workspace
        -   Support for Instance Parameters to configure each amazon connect instance with custom parameters when first registering an Instance.
    -   Changed:
        -   While first registering the connect instance, you can provide a ccpHost and ccpURL if the Amazon Connect domain for your instance is not the latest one.
        -   Support for upcoming AWS domain change to 'my.connect.aws'
    -   Fixed: Issues with Setup Guide when glide.ui.escape\_all\_script is set to false
-   **Version 2.0.0 - October 2020**
    -   New:
        -   Support for Phone Channel Analytics using AWA work items and Workforce Optimization \(starting Paris\)
        -   Outbound calling support with Flow Templates to quickly run outbound calling
        -   Surfacing Transcription, Recording, and Customer Sentiment Analysis in Workspace
-   **Version 1.1.1 - July 2020**

    Fixed: Fixed an issue with the interactionId not being set for unknown callers.

-   **Version 1.0.1 - April 2020**

    Works in concert with the Cloud Call Center Core and Cloud Call Center for ITSM apps to enable new employee experiences, unlock productivity for agents, and provide management with insights and coaching opportunities.


