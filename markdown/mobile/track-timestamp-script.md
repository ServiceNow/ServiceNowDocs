---
title: Using timestamps to track user changes in an input form
description: Use the following code to extract data to monitor the timestamp of changes made by different users on an input form screen.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure an input form screen, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Using timestamps to track user changes in an input form

Use the following code to extract data to monitor the timestamp of changes made by different users on an input form screen.

Timestamps can be retrieved via the script when the **Track timestamps for input updates** field is enabled in the input form's record. Enable the field to track the time input values are changed. For more information, search for the field **Track timestamps for input updates** in the topic [Configure an input form screen](../task/parameter-screen-config.md).

The following script is an example of how to retrieve timestamps based on when the input's value was changed. The information is accessible using a scripted writeback action.

```
(function WriteBackAction(parm_input, parm_variable, actionResult, additionalData) { 
// var additionalInputDataMap = additionalData.getAdditionalInputDataMap();
var input1Timestamp = additionalInputDataMap["input1"].getLastUpdatedTimestamp(); // input1 stands for the input's name. Could be any input type
//Handle timestamp logic here
})(parm_input, parm_variable, actionResult, additionalData);

```

