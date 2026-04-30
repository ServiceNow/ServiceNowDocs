---
title: Script code for comment type and updates for input actions
description: Use the following script to determine where user comments entered in an input form are stored. The script also records comment deletion, updates, insertions of new text, and tracking the timestamp of changes.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-03-06"
reading_time_minutes: 1
breadcrumb: [Configure input form actions in an input form screen, Input form actions in an input form screen, Input actions and input sources, Configure an input form screen, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Script code for comment type and updates for input actions

Use the following script to determine where user comments entered in an input form are stored. The script also records comment deletion, updates, insertions of new text, and tracking the timestamp of changes.

This code defines a function **WriteBackAction** that processes parameter actions for a specific input. It retrieves the parameter actions for *input1* and iterates through them to handle comments. If a comment is marked as deleted, the admin can set any logic that handles the deletion of a comment. If the comment is not marked as deleted, it retrieves the comment value and the last updated timestamp, and adds or updates the comment in the result table for the specific record.

```
(function WriteBackAction(parm_input, parm_variable, actionResult, additionalData) { 
var additionalInputDataMap = additionalData.getAdditionalInputDataMap();
var paramActions = additionalInputDataMap['input1'].getParameterActions(); // input1 stands for the input's name. Could be any input type
for (i = 0; i < paramActions.length; i++) {
var currentAction = paramActions[i];
// Handle Add/Remove/Update Comment 
if (currentAction.getType() === 'comment') {
var hasDeleted = currentAction.hasDeleted(); // Checks if the user deleted the comment in the input form's UI
if (hasDeleted && hasDeleted == true) {
// Handle delete logic here, for example set the field where the comment is set to an empty string
} 
else 
{
  var commentValue = currentAction.getCommentValue();
              var commentLastUpdatedTimeStamp = currentAction.getLastUpdatedTimestamp();

// handle here add/update comment to the result table for the specific record 
}
}
}

```

