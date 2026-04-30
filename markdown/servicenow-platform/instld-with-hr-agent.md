---
title: Components installed with ServiceNow Voice for HR Agent Workspace
description: Several contact flows and operation handlers are installed with ServiceNow Voice for HR Agent Workspace.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ServiceNow Voice reference, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Components installed with ServiceNow Voice for HR Agent Workspace

Several contact flows and operation handlers are installed with ServiceNow Voice for HR Agent Workspace.

## Contact flows installed

|Contact flow|Description|
|------------|-----------|
|ServiceNow HR Inbound Demo Flow|Contains the call tree for inbound calls. When a caller contacts the call center, using the voice or dual-tone multi frequency \(DTMF\) inputs from caller, the contact flow is invoked in the Amazon Connect instance based on the caller context. This contact flow contains nodes that act as integration points between Amazon services and the ServiceNow instance. Based on the nodes defined in the contact flow, the corresponding operation handlers are triggered in the ServiceNow instance. The caller then gets the response that is defined in the operation handler.|
|ServiceNow HR Outbound Demo Flow|Contains the call tree for outbound calls. It specifies the whisper message that a caller hears before getting connecting to an agent.|

## Operation handlers installed

Operation handlers are reusable code components that get executed on the ServiceNow instance. They work on the request/response message exchange pattern.

|Operation handler|Description|
|-----------------|-----------|
|createHRInteraction|Creates an interaction record in the ServiceNow instance for the incoming calls.|
|fetchHRInteraction|Fetches interaction and processes sn\_cti\_hr\_cnt.enable\_ims\_update sys property for creating conversation.|

**Parent Topic:**[ServiceNow Voice reference](ccc-reference.md)

