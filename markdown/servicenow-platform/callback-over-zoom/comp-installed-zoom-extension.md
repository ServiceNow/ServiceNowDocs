---
title: Components installed with Zoom extension for Omnichannel Callback
description: Several types of components are installed with the Zoom extension for Omnichannel Callback application.
locale: en-US
release: yokohama
product: Callback over Zoom
classification: callback-over-zoom
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Install Zoom extension for Omnichannel Callback, Zoom extension for Omnichannel Callback, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Components installed with Zoom extension for Omnichannel Callback

Several types of components are installed with the Zoom extension for Omnichannel Callback application.

## Script includes

|Script include|Description|
|--------------|-----------|
|ZoomCallDatabase|Contains database-related functions.|
|ZoomCallDriver|Implements extension point for sn\_omni\_callback.VideoCallDriver.|
|ZoomCallEventHandler|Overrides the functions of ZoomCallEventHandlerSNC.|
|ZoomCallEventHandlerSNC|Contains utility functions for handling the transcript completed events.|
|ZoomCallTranscriptProcessor|Contains utility functions to process the Zoom transcript.|
|ZoomCallUtils|Overrides the functions of ZoomCallUtilsSNC.|
|ZoomCallUtilsSNC|Contains the utility functions for Zoom callback.|

## Business rules

<table id="table_ump_c33_bwb"><thead><tr><th>

 

</th><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Close interaction \(Zoom Callback\)

</td><td>

Notify Conference Call\[notify\_conference\_call\]

</td><td>

Closes the interaction after the Zoom meetings ends. Both the agent and the requester must join the call to close the interaction.

</td></tr><tr><td>

Create Notify Conference call record

</td><td>

Callback\[sys\_cs\_callback\]

</td><td>

Creates a notify conference call record when the Zoom callback is created.

</td></tr><tr><td>

Recording Completed \(Zoom Callback\)

</td><td>

Notify Recording\[notify\_recording\]

</td><td>

Stores the recording URL in the interaction when the recording is completed.

</td></tr><tr><td>

Update Zoom Host when agent is assigned

</td><td>

Interaction\[interaction\]

</td><td>

Makes the agent the host when the interaction is accepted by the agent.

</td></tr></tbody>
</table>