---
title: WorkflowDuration - Global
description: The WorkflowDuration script include provides methods to calculates the duration \(in seconds\) based on the variables of a workflow activity. It is an interface between Workflow Timer\(\) and DurationCalculator\(\).Adds the number of seconds to the specified start date/time.Calculates the number of seconds and the due date.Calculates the number of seconds remaining to the specified end date/time.Returns the end date/time set by a call to calculate\(record\).Returns the seconds value that was set by a call to calculate\(record\).Returns the totalSeconds value that was set by a call to calculate\(record\).Sets the end date/time to use when calculating the remaining time.Sets the end date/time to use when calculating the remaining time.Sets the start date/time to use in the calculations.Sets the start date/time to use in the calculations.Sets the used seconds compensation, where the number of seconds is the number of seconds inside of any schedule.Sets the workflow schedule/timezone. Used for schedule\_type workflow\_schedule and timezone\_type workflow\_timezone\).
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# WorkflowDuration- Global

The WorkflowDuration script include provides methods to calculates the duration \(in seconds\) based on the variables of a workflow activity. It is an interface between Workflow Timer\(\) and DurationCalculator\(\).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## WorkflowDuration - addSeconds\(GlideRecord record, Number amount\)

Adds the number of seconds to the specified start date/time.

|Name|Type|Description|
|----|----|-----------|
|record|GlideRecord|description|
|amount|Number|amount|

|Type|Description|
|----|-----------|
|Boolean|True, if object was successfully created.|

## WorkflowDuration - calculate\(GlideRecord record\)

Calculates the number of seconds and the due date.

|Name|Type|Description|
|----|----|-----------|
|record|GlideRecord|The record that contains the fields with the schedule, timezone, and date/time information. This is almost always **activity.vars.\_\_var\_record\_\_**.|

|Type|Description|
|----|-----------|
|void| |

## WorkflowDuration - calculateTimeLeft\(GlideRecord record\)

Calculates the number of seconds remaining to the specified end date/time.

|Name|Type|Description|
|----|----|-----------|
|record|GlideRecord|The record that contains the fields with the schedule, timezone, and date/time information. This is almost always **activity.vars.\_\_var\_record\_\_**.|

|Type|Description|
|----|-----------|
|void| |

## WorkflowDuration - getEndDateTime\( \)

Returns the end date/time set by a call to calculate\(record\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideDateTime|The end date/time.|

## WorkflowDuration - getSeconds\( \)

Returns the seconds value that was set by a call to calculate\(record\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The number of seconds set by a call to calculate\(record\).|

## WorkflowDuration - getTotalSeconds\( \)

Returns the totalSeconds value that was set by a call to calculate\(record\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The total number of seconds set by a call to calculate\(record\).|

## WorkflowDuration - setEndDateTime\(String dt\)

Sets the end date/time to use when calculating the remaining time.

To convert the value into the GlideDateTime internal format, use GlideDateTime.getValue\(\).

|Name|Type|Description|
|----|----|-----------|
|dt|String|The end date/time to use.|

|Type|Description|
|----|-----------|
|void| |

## WorkflowDuration - setEndDateTime\(GlideDateTime dt\)

Sets the end date/time to use when calculating the remaining time.

To convert the value into the GlideDateTime internal format, use **GlideDateTime.getValue\(\)**.

|Name|Type|Description|
|----|----|-----------|
|dt|GlideDateTime|The end date/time to use.|

|Type|Description|
|----|-----------|
|void| |

## WorkflowDuration - setStartDateTime\(String dt\)

Sets the start date/time to use in the calculations.

|Name|Type|Description|
|----|----|-----------|
|dt|String|The start date/time to use, in GMT.|

|Type|Description|
|----|-----------|
|void| |

## WorkflowDuration - setStartDateTime\(GlideDateTime dt\)

Sets the start date/time to use in the calculations.

To convert the value into the GlideDateTime internal format, use GlideDateTime.getValue\(\).

|Name|Type|Description|
|----|----|-----------|
|dt|GlideDateTime|The start date/time to use.|

|Type|Description|
|----|-----------|
|void| |

## WorkflowDuration - setUsedSecs\(Number secs\)

Sets the **used seconds** compensation, where the number of seconds is the number of seconds inside of any schedule.

Can be a -ve number, which extends the duration.

|Name|Type|Description|
|----|----|-----------|
|secs|Number|The number of used seconds to set.|

|Type|Description|
|----|-----------|
|void| |

## WorkflowDuration - setWorkflow\(Object schedule, Object timezone\)

Sets the workflow schedule/timezone. Used for **schedule\_type** **workflow\_schedule** and **timezone\_type** **workflow\_timezone**\).

|Name|Type|Description|
|----|----|-----------|
|schedule|Object|The schedule to use. Usually from the workflow **context.schedule**.|
|timezone|Object|The timezone to use. Usually from the workflow **context.timezone**.|

|Type|Description|
|----|-----------|
|void| |

