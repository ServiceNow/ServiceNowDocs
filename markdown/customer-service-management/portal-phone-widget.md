---
title: Use Voice call widget for portal communication
description: The voice call widget enables users to manage voice calls initiated from the portal interface or Engagement Messenger. The widget maintains call state across tabs and page navigation, displaying call controls and connection status.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/portal-phone-widget.html
release: australia
topic_type: concept
last_updated: "2026-08-20"
reading_time_minutes: 2
keywords: [voice call widget, voice calls, portal, Engagement Messenger, WebRTC, call management]
breadcrumb: [Configure Voice, Configure omnichannel, Configure, Customer Service Management]
---

# Use Voice call widget for portal communication

The voice call widget enables users to manage voice calls initiated from the portal interface or Engagement Messenger. The widget maintains call state across tabs and page navigation, displaying call controls and connection status.

WebRTC \(Web Real-Time Communication\) enables voice communication directly between browsers. When integrated into ServiceNow, it allows users to initiate calls from portal pages or Engagement Messenger. Users can make calls without switching applications or relying on external communication platforms.

The voice call widget appears at the bottom-left corner of the page when a call is initiated.

## Enable WebRTC for voice calls

To enable the voice call capability on ServiceNow, first create an AI voice assistant to enable natural, conversational voice interactions between users and AI voice agents. For configuration steps, see [Create an AI voice assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-an-ai-voice-service.md).

**Note:** The WebRTC application includes out-of-box configurations for client-side WebRTC calling. While manual configuration is optional, the provided setup eliminates the need for additional customization.

Select the **Web Real-Time Communication \(WebRTC\)** tab to connect the voice assistant to mobile, web, and external applications.

1.  Select **Web applications**.
2.  Follow the on-screen instructions to configure WebRTC for ServiceNow Portal or Engagement Messenger. For detailed configuration steps, see [Create an AI voice assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-an-ai-voice-service.md).

Contact your administrator for help configuring and enabling the voice call widget on your selected web application.

## Customer support using voice call widget workflow

The following workflow shows an interaction between the Portal user and the AI Voice agent.

Sarah, an e-commerce customer, needs help while completing an activity in the portal, such as reviewing product information or managing items in a shopping cart. Sarah starts a call from the voice call widget, and the system connects Sarah to an AI Voice agent that provides support. During the call, Sarah can continue moving through the portal, and the active session remains connected until the issue is resolved.

\[Omitted image "portal-phone-workflow-MMASSET0022359.png"\] Alt text: Customer support workflow using the voice call widget.

The voice call widget includes the following key capabilities:

<table id="table_zml_5nt_zjc"><thead><tr><th>

Feature

</th><th>

Web applications

</th><th>

Behavior and use case

</th></tr></thead><tbody><tr><td>

Call timer

</td><td>

-   ServiceNow Portal
-   Engagement Messenger

</td><td>

Elapsed time during an active call so users can track call duration.

</td></tr><tr><td>

Mute audio control

</td><td>

-   ServiceNow Portal
-   Engagement Messenger

</td><td>

Mute or unmute audio during an active call to manage background noise. If mute fails, the widget displays an alert.

</td></tr><tr><td>

End call control

</td><td>

-   ServiceNow Portal
-   Engagement Messenger

</td><td>

End the current call from the widget. If the call cannot be ended, the widget displays an alert.

</td></tr><tr><td>

Call state indicators

</td><td>

-   ServiceNow Portal
-   Engagement Messenger

</td><td>

Current call state, such as connecting, connected, or connection failed, so users can understand call status and retry when needed.

</td></tr><tr><td>

Cross-tab persistence

</td><td>

ServiceNow Portal

</td><td>

Call state across multiple browser tabs. If the portal is opened in a second tab, an alert indicates that the call is active elsewhere and helps prevent duplicate calls.

</td></tr><tr><td>

Page navigation persistence

</td><td>

ServiceNow Portal

</td><td>

Active calls remain connected when users navigate between portal pages.**Note:** Refreshing the page or reloading WebRTC application disrupts the connectivity.

</td></tr></tbody>
</table>