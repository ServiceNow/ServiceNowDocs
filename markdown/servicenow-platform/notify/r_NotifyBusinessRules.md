---
title: Business rules installed with Notify
description: Notify adds the following business rules.
locale: en-US
release: australia
product: Notify
classification: notify
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Components installed with Notify, Notify reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Business rules installed with Notify

Notify adds the following business rules.

|Business rule|Table|Description|
|-------------|-----|-----------|
|No Call Workflows for Shortcodes|\[notify\_group\]|Checks and displays an error if the call is being triggered by a short code.|
|Update Participant Duration|\[notify\_participant\]|Updates participant duration when it becomes inactive.|
|Check if Notify call exists and active|\[notify\_participant\_session\]|Checks if Notify call has valid reference record and updates it if the call is inactive currently.|
|Update Last Active On|\[notify\_participant\]|Sets the last active before insertion/update of Notify participant.|
|Show info msg about selection in choice|\[notify\_group\_selector\_choice\]|Displays a message if either Notify group or conference provider is not selected.|
|Validate values in the choice|\[notify\_group\_selector\_choice\]|Checks if either of Notify group or conference provider is filled.|
|Set scratchpad values|\[notify\_group\_selector\_choice\]|Checks if conference provider is available by iterating through service provider list.|
|Show message for empty choices|\[notify\_group\_selector\]|Displays an info message if there are no choices for the provider selector.|
|Clear fields when Manual Selection is set|\[notify\_group\_selector\]|Clears out some fields when manual selection is set in Notify group selector table.|
|Update Participant Duration|\[notify\_participant\_session\]|Calculates the duration of participant on conference call.|
|Update session muted state|\[notify\_participant\]|Sets the value of mute and expelled to true once the conference call participant becomes inactive.|
|Update conference call|\[notify\_participant\]|Sets the state of conference call based on the participant leaving or joining the call.|
|Validate Order field value|\[notify\_group\_selector\]|Validates order field value to be unique amongst all provider selectors.|
|Restrict Workflows For only Voice Nums|\[notify\_number\]|Restricts association of voice only capable number with number group having inbound/outbound SMS workflows.|
|Restrict Workflows For only SMS Numbers|\[notify\_number\]|Restricts association of SMS only capable number with number group having inbound/outbound voice workflows.|
|Validations on default record|\[notify\_group\_selector\]|Validates that source table and order field are mandatory in case of default set to false and both fields empty in case of default set to true.|
|Clearing fields when Default is true|\[notify\_group\_selector\]|Clears out some fields when default is set to true.|
|No Default selector set|\[notify\_group\_selector\]|Ensures one active provider selector is set as default.|
|Check active default selector is unique|\[notify\_group\_selector\]|Ensures only one provider selector is set as default.|
|Process SMS preferences for incoming SMS|\[notify\_message\]|When an SMS preference configuration defined for a particular telephony provider, then apply it for every incoming SMS.|
|Check default notify group is unique|\[notify\_group\]|Validates that not more than one group is set as default Notify group.|
|Trigger conference end|\[notify\_conference\_call\]|When a conference call ends, triggers the notify.conference.end event|
|Update Call Active State|\[notify\_call\_status\]|Updates the status of the call in notify\_call\_status with the status received from Twilio.|
|Update Conference Call Active State|\[notify\_participant|Updates the active flag in notify\_participant table. Also calculates the duration when the call is ended by a participant.|
|Update Participant Active State|\[notify\_participant\_session\]|Updates the active flag for the participant \(notify\_participant\), and calculates the total time on the call upon disconnecting from the call.|
|Update Participant Session Active State|\[notify\_call\]|Synchronizes the state of the call between notify\_call and notify\_participant\_session. Upon disconnecting from the call, updates notify\_participant\_session with the duration of the call.|
|Warn for incorrectly configured workflow|\[notify\_group\]|Checks notify\_group table and displays an error if the a workflow is not configured correctly|

**Parent Topic:**[Components installed with Notify](installed-with-notify2.md)

