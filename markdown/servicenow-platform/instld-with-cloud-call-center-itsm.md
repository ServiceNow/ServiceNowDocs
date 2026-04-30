---
title: Components installed with ServiceNow Voice for ITSM
description: Several contact flows and operation handlers are installed with activation of the ServiceNow Voice for ITSM application \(sn\_cti\_itsm\_cnt\).
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ServiceNow Voice reference, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Components installed with ServiceNow Voice for ITSM

Several contact flows and operation handlers are installed with activation of the ServiceNow Voice for ITSM application \(sn\_cti\_itsm\_cnt\).

## Contact flows installed

These contact demo flows are a quick way to set up inbound and outbound flow logic required by Amazon Connect.

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Contact flow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ServiceNow ITSM Inbound Demo Flow

</td><td>

Contains the call tree for inbound calls.

 When a caller contacts the call center, using the voice or dual-tone multi frequency \(DTMF\) inputs from caller, the contact flow is invoked in the Amazon Connect instance based on the caller context.

 This contact flow contains nodes that act as integration points between Amazon services and the ServiceNow instance.

 Depending on the nodes defined in the contact flow, the corresponding operation handlers are triggered in the ServiceNow instance.

 The caller then gets the response that is defined in the operation handler.

 Both real-time transcription \(RTT\), and advanced work assignment \(AWA\) are supported when configured during setup.

</td></tr><tr><td>

ServiceNow ITSM Outbound Demo Flow

</td><td>

Contains the call tree for outbound calls. It specifies the whisper message that a caller hears before getting connecting to an agent.

 Real-time transcription \(RTT\) is supported when configured during setup.

</td></tr></tbody>
</table>## Operation handlers installed

Operation handlers are the bridge between the Amazon Connect instance and your ServiceNow instance.

|Operation handler|Description|
|-----------------|-----------|
|sn\_FallbackIntent|Captures the user input|
|manageIncident|Manages an existing incident|
|unlockAccount|Unlocks a user account|
|unlockAccount.DialogCodeHook|Validates incoming info related to account unlocking|
|announcements|Makes announcement for a caller|
|announcements.DialogCodeHook|Validates incoming info for announcement creation|
|manageIncident.DialogCodeHook|Initializes the Amazon Connect instance and validates incoming calls|
|createIncident|Creates an incident|
|createIncident.DialogCodeHook|Validates incoming info for incident creation|
|createITSMInteraction|Creates interaction records for inbound calls|
|fetchITSMInteraction|Gathers details to help create outbound interactions|

**Parent Topic:**[ServiceNow Voice reference](ccc-reference.md)

