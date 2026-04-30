---
title: Components installed with ServiceNow Voice for CSM
description: Several contact flows and operation handlers are installed with Cloud Call Center for CSM application \(sn\_cti\_csm\_cnt\).
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [ServiceNow Voice reference, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Components installed with ServiceNow Voice for CSM

Several contact flows and operation handlers are installed with Cloud Call Center for CSM application \(sn\_cti\_csm\_cnt\).

## Contact flows installed

|Contact flow|Description|
|------------|-----------|
|ServiceNow CSM Inbound Demo Flow|Contains the call tree for inbound calls. When a caller contacts the call center, using the voice or dual-tone multi frequency \(DTMF\) inputs from caller, the contact flow is invoked in the Amazon Connect instance based on the caller context. This contact flow contains nodes that act as integration points between Amazon services and the ServiceNow instance. Based on the nodes defined in the contact flow, the corresponding operation handlers are triggered in the ServiceNow instance. The caller then gets the response that is defined in the operation handler.|
|ServiceNow CSM Outbound Demo Flow|Contains the call tree for outbound calls. It specifies the whisper message that a caller hears before getting connecting to an agent.|
|ServiceNow CSM Transfer to Agent Flow|The call is relocated to another persona using call transfer functionality. A new PhoneLog is created with each transfer. The PhoneLog also includes any attachments associated with the interaction. Call transfers can be done with either incoming and outgoing calls.|
|ServiceNow CSM Transfer to Queue Flow|The inbound call is relocated to a queue using call transfer functionality. A new PhoneLog is created with each transfer. The PhoneLog also includes any attachments associated with the interaction. Call transfers can be done with either incoming and outgoing calls.|

## Operation handlers installed

|Operation handler|Description|
|-----------------|-----------|
|$csm.connect.s3.event|Receives and processes events from S3 buckets where connect audio, transcript and analysis data is created and stored and tries to associate with interaction and openframe call log records. This is CSM operation handler for the new data model with conversation as metadata|
|$csm.connect.kinesis.event|Handler to process CTR events from Kinesis stream for CSM integration with VA Conversations|
|speakToCSMAgent|Enables customer contacts and consumers to speak with a live agent.|
|createCSMCase|Enables customer contacts and consumers to create a customer service case.|
|manageCSMCase|Enables customer contacts and consumers to update an existing case.|
|csmAnnouncements|Makes announcements for a caller.|
|createCSMInteraction|Creates an interaction record in the ServiceNow instance for the incoming calls.|
|updateCSMInteraction|Updates an existing interaction record in the ServiceNow instance for the incoming calls.|
|fetchCSMInteraction|Fetches interaction and processes sn\_cti\_csm\_cnt.enable\_ims\_update sys property for creating conversation.|

**Parent Topic:**[ServiceNow Voice reference](ccc-reference.md)

