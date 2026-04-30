---
title: Integrating ServiceNow Voice with ITSM
description: Route calls coming through the ServiceNow Voice to specific phone queues based on user preference, utterances, or any other ServiceNow data to optimize incident resolution.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integrating Voice with other applications, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Integrating ServiceNow Voice with ITSM

Route calls coming through the ServiceNow Voice to specific phone queues based on user preference, utterances, or any other ServiceNow data to optimize incident resolution.

## Sample ITSM contact flow

Use the inbound **\(ServiceNow ITSM Inbound Demo Flow\)** and outbound **\(ServiceNow ITSM Outbound Demo Flow\)** Amazon Connect ITSM sample contact flows that come with the Voice integration to get you up and running quickly. The sample flow allows you to deflect voice calls or route them based on the caller context to different queues. When a call comes through the ServiceNow Voice, the Amazon Connect application uses data dips to identify the caller and then deflect the call or route it to the right agent. For more information on integrating ServiceNow Voice with Amazon Connect see, [Integrate ServiceNow Voice with Amazon Connect](../task/integrate-ccc-amazonconnect.md).

Callers can access status updates or make updates to their records when they are authenticated.

## PIN-based authentication

Callers can use PIN-based authentication to access the phone channel. Managers can set or reset the PIN for the users who can also set or reset their phone PIN. For more information, see [Configure a phone PIN](set-pin-ccc.md#).

## Workforce Optimization for ITSM

Integrate Voice with Workforce Optimization for ITSM to visualize call metrics from Amazon Connect. The Voice uses [Advanced Work Assignment](../../../administer/advanced-work-assignment/concept/awa-overview.md) to display the call metrics and active calls along with all other Channel metrics in the Manager Workspace.

![Amazon Connect Phone Workforce Optimization for ITSM](../image/cloudcallcenter-amazonconnect-wfo-itsm.png "Amazon Connect Phone Workforce Optimization for ITSM")

-   **[Install ServiceNow Voice for ITSM](../task/install-ccc-itsm.md)**  
You can install the ServiceNow Voice for ITSM application \(sn\_cti\_itsm\_cnt\) if you have the admin role. This plugin installs the ITSM content for integration between ServiceNow Voice and a third-party phone system.
-   **[Real time transcriptions for ServiceNow Voice for IT Service Management](using-voice-rtt-itsm.md)**  
Agents can see a transcript of voice calls while interacting with customers. Real time transcription enable agents to better understand caller issues, and managers to gain insights into caller trends and agent training gaps.
-   **[Enable native voice control in Service Operations Workspace](../task/itsm-native-voice-record-page.md)**  
Enable the native voice control to allow the agents to manage the calls using the Interaction Controls Component and the Customer History tab component.

**Parent Topic:**[Integrating Voice with other applications](integrate-ccc-other-apps.md)

