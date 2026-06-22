---
title: Usage insights for call events enabled using Interaction Controls Component \(ICC\)
description: Usage Insights provides event tracking for voice call events in ICC enabled interactions. Admins and managers can review detailed call events to verify correct event actions and diagnose issues without accessing console logs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/usage-insight-for-icc-enabled-call-events.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: concept
last_updated: "2026-04-30"
reading_time_minutes: 1
breadcrumb: [ICC for voice calls, Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# Usage insights for call events enabled using Interaction Controls Component \(ICC\)

Usage Insights provides event tracking for voice call events in ICC enabled interactions. Admins and managers can review detailed call events to verify correct event actions and diagnose issues without accessing console logs.

## Usage insights for call events overview

When an agent performs a call action from their Workspace, such as making an outbound call, receiving a call, muting a participant, starting a recording, or initiating a coaching session, the ICC component triggers a corresponding event. ServiceNow Platform Analytics captures each event with its payload and displays both in the **Usage Insights** dashboard.

**Note:** Usage Insights is accessible under Platform Analytics in any ServiceNow instance where the feature is enabled.

\[Omitted image "usage-insight-dashboard.png"\] Alt text: Usage Insight dashboard

The **Usage Insights** dashboard displays all applications by default. To view the ICC events, filter by CSM/FSM Configurable Workspace. You can browse by the following views:

-   **Users**

    Lists all agents who have triggered tracked events, displayed as hashed IDs. See [Usage Insights dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ued-ec.md).

-   **Sessions**

    Shows individual agent sessions with a chronological list of events.

-   **Events**

    Provides an aggregate view of all registered events with occurrence and active user counts.

-   **Pages**

    Displays page level activity within the workspace.


All out-of-box call events are prefixed with ‘NVC\*’. This prefix makes it easy to search and filter a specific category of events from the **Events** tab, such as: NVC\_HandleRecording, NVC\_MuteParticipants, NVC\_StartMonitoring etc.

**Note:** NVC or Native Voice Control are call capabilities made available for CCaaS users integrating with ServiceNow Voice via Interaction Controls Component \(ICC\).

Each event entry for usage insights includes a complete payload. The following table describes the common payload fields.

|Field|Description|
|-----|-----------|
|participant\_id|Identifies the agent or customer associated with the event.|
|event\_type|Type of action that occurred, such as mute, unmute, or record.|
|name|Name of the event, such as mute or handle\_recording.|
|interaction sys\_id|The sys\_id of the corresponding interaction record in the ServiceNow instance.|
|external\_id|An identifier from the external CCaaS provider associated with this interaction.|

Enable call events tracking by configuring the Usage Insights capability. See: [Enable Usage Insights for Interaction Controls Component \(ICC\) enabled call events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/enable-usage-insights-for-icc-call-events.md).

