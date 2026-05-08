---
title: WFActivityHandler - Global
description: The WFActivityHandler script include is the base class for all workflow activities.Logs a debug message.Logs a debug message.Generates approvals and tasks before the activity runs for a preview of upcoming work.Logs an information message.Logs an information message.Evaluates activity variables in the script.Event handler for cancel event.Virtual method. Activity subclasses must override this method to perform work appropriate to the activity.Enables activities to run a script contained in an activity variable of type script.Sets the activity output property.Sets the activity result as failed with an optional reason string.Sets the result of this activity as successful.Logs a warning message.Logs a warning message.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# WFActivityHandler- Global

The WFActivityHandler script include is the base class for all workflow activities.

As the base class for all workflow activities, this code always executes as part of an activity.

When developing your own workflow activities, create your script object by deriving from this class and overriding methods as necessary to get the functionality you want. Client code must override method onExecute\(\) to perform meaningful activity processing.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## WFActivityHandler - debug\(String msg, String args\)

Logs a debug message.

|Name|Type|Description|
|----|----|-----------|
|msg|String|Message to send to the log.|
|args|String|String to send to the log|

|Type|Description|
|----|-----------|
|void| |

## WFActivityHandler - debug\(String msg, Array args\)

Logs a debug message.

|Name|Type|Description|
|----|----|-----------|
|msg|String|Message to send to the log.|
|args|Array|Array of values to send to the log|

|Type|Description|
|----|-----------|
|void| |

## WFActivityHandler - generate\(String activityId, String order, GlideDateTime startAtDspValue, Boolean noCreateFlag\)

Generates approvals and tasks before the activity runs for a preview of upcoming work.

Enables generating objects at the start of a workflow in a **pending** state. For related information, see Generate workflow activity.

<table id="table_dv2_sh5_4t" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

activityId

</td><td>

String

</td><td>

Sys\_id of this running activity. Table: Workflow Activities \[wf\_activity\]

</td></tr><tr><td>

order

</td><td>

String

</td><td>

Order number associated with the task or approval.

</td></tr><tr><td>

startAtDspValue

</td><td>

String

</td><td>

Starting time for the task or approval in [GlideDateTime](../../GlideDateTime/concept/c_GlideDateTimeAPI.md#) format.

</td></tr><tr><td>

noCreateFlag

</td><td>

Boolean

</td><td>

Flag that indicates whether to skip creating an approval record.Valid values:

-   true: Don't create an approval record.
-   false: Create an approval record.

Default: true

</td></tr></tbody>
</table><table id="table_ev2_sh5_4t" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Pre-generation object saved in the workflow scratchpad. For example, the object might be an array of approval IDs. When the activity runs the onExecute function, it can request the pre-generation object to determine one of the following conditions:-   Approvals have already been created in a pending state.
-   Activity must create the approvals using the onExecute function.

</td></tr></tbody>
</table>## WFActivityHandler - info\(String msg, String args\)

Logs an information message.

|Name|Type|Description|
|----|----|-----------|
|msg|String|Message to send to the log.|
|args|String|String to send to the log.|

|Type|Description|
|----|-----------|
|void| |

## WFActivityHandler - info\(String msg, Array args\)

Logs an information message.

|Name|Type|Description|
|----|----|-----------|
|msg|String|Message to send to the log.|
|args|Array|Array of values to send to the log|

|Type|Description|
|----|-----------|
|void| |

## WFActivityHandler - js\(String str\)

Evaluates activity variables in the script.

Used to evaluate strings that contain el such as `${some script}` or strings starting with `javascript:`. See almost any existing activity for example usage.

|Name|Type|Description|
|----|----|-----------|
|str|String|String that possibly contains embeded el.|

|Type|Description|
|----|-----------|
|String|The evaluated string.|

## WFActivityHandler - onCancel\( \)

Event handler for **cancel** event.

The base class for the activity script sets this activity to be cancelled. Derived classes \(activities\) can override this method if additional processing is required to cancel this activity. Activity **Manual Approvals** is an example of overriding this method to perform additional processing to cancel this activity.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## WFActivityHandler - onExecute\( \)

Virtual method. Activity subclasses must override this method to perform work appropriate to the activity.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## WFActivityHandler - runScript\(String script\)

Enables activities to run a script contained in an activity variable of type script.

Example activities that use this method include If, **Wait for condition**, and **Approval - User**.

|Name|Type|Description|
|----|----|-----------|
|script|String|String containing valid Javascript.|

|Type|Description|
|----|-----------|
|variable|If the script set the workflow variable *answer* then this value is returned. If not, then the result of the script execution is returned.|

## WFActivityHandler - setActivityOutput\( \)

Sets the activity output property.

See activity **SOAP Message**.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## WFActivityHandler - setResultFailed\(String reason\)

Sets the activity result as failed with an optional reason string.

See Activity **SOAP Message**.

|Name|Type|Description|
|----|----|-----------|
|reason|String|\(Optional\) Description of the reason this activity failed.|

|Type|Description|
|----|-----------|
|void| |

## WFActivityHandler - setResultSucceeded\( \)

Sets the result of this activity as successful.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## WFActivityHandler - warn\(String msg, String args\)

Logs a warning message.

|Name|Type|Description|
|----|----|-----------|
|msg|String|Message to send to the log.|
|args|String|String to send to the log|

|Type|Description|
|----|-----------|
|void| |

## WFActivityHandler - warn\(String msg, Array args\)

Logs a warning message.

|Name|Type|Description|
|----|----|-----------|
|msg|String|Message to send to the log.|
|args|Array|Array of values to send to the log|

|Type|Description|
|----|-----------|
|void| |

