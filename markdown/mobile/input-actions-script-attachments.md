---
title: Script code for storing user-selected attachments in the database
description: Use the following script to determine where attachments selected by the user in the attachment input action are stored within the database.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure input form actions, Input form actions, Input actions and input sources, Configure an input form screen, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Script code for storing user-selected attachments in the database

Use the following script to determine where attachments selected by the user in the attachment input action are stored within the database.

This code defines a function **WriteBackAction** that processes an input and adds attachments to a specific record in the Incident \[incident\] table. It retrieves the parameter actions for the input and checks if any of them are of the type attachment. If the conditions are met, it adds the attachment to the specified record using the **actionResult.addActionAttachment** function parameter.

```
(function WriteBackAction(parm_input, parm_variable, actionResult, additionalData) { 
var targetTableName = "incident";
var targetTableRecordSysId = "37aa099533b352102ed2923fad5c7b09";
var inputName = "input1"; // input1 stands for the input's name. Could be any input type
var additionalInputDataMap = additionalData.getAdditionalInputDataMap();
var Param Actions = additionalInputDataMap[inputName].getParameterActions(); // input1 stands for the input's name
for (i = 0; i < paramActions.length; i++) {
var currentAction = paramActions[i]; 
if (currentAction.getType() === 'attachments') {
       if (currentAction.shouldAddAttachments()) {
actionResult.addActionAttachment(inputName, currentAction.getId(), targetTableName, targetTableRecordSysId);
}
}
}
})(parm_input, parm_variable, actionResult, additionalData);

```

