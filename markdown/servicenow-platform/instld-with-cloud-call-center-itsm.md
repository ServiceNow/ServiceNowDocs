---
title: Components installed with ServiceNow Voice for ITSM
description: Several contact flows and operation handlers are installed with activation of the ServiceNow Voice for ITSM application \(sn\_cti\_itsm\_cnt\).
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ServiceNow Voice reference, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Components installed with ServiceNow Voice for ITSM

Several contact flows and operation handlers are installed with activation of the ServiceNow Voice for ITSM application \(sn\_cti\_itsm\_cnt\).

## Contact flows installed

|Contact flow|Description|
|------------|-----------|
|ServiceNow ITSM Inbound Demo Flow|Contains the call tree for inbound calls. When a caller contacts the call center, using the voice or dual-tone multi frequency \(DTMF\) inputs from caller, the contact flow is invoked in the Amazon Connect instance based on the caller context. This contact flow contains nodes that act as integration points between Amazon services and the ServiceNow instance. Based on the nodes defined in the contact flow, the corresponding operation handlers are triggered in the ServiceNow instance. The caller then gets the response that is defined in the operation handler.|
|ServiceNow ITSM Outbound Demo Flow|Contains the call tree for outbound calls. It specifies the whisper message that a caller hears before getting connecting to an agent.|
|include rtt| |
|awa routing| |

## Operation handlers installed

|Operation handler|Description|
|-----------------|-----------|
|sn\_FallbackIntent|Captures the user input|
|manageIncident|Manages an existing incident|
|unlockAccount|Unlocks a user account|
|announcements|Makes announcement for a caller|
|manageIncident.DialogCodeHook|Initializes the Amazon Connect instance and validates incoming calls|
|createIncident|Creates an incident|
|createITSMInteraction|Creates an interaction|
|fetchITSMInteraction|Fetches the details of an interaction|

**Parent Topic:**[ServiceNow Voice reference](ccc-reference.md)

