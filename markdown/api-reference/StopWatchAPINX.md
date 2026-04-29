---
title: StopWatch \(Next Experience\) - Client
description: The StopWatch API provides methods to measure durations in the Next Experience UI Framework.Constructor to initialize a new StopWatch.Returns the elapsed time in milliseconds since the StopWatch started.Resets the StopWatch start time as the current date and time.Returns the elapsed time in ISO 8601 format \(HH:mm:ss.sss\) since the StopWatch started.
locale: en-US
release: australia
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Client Next Experience API reference, API reference, API implementation and reference]
---

# StopWatch \(Next Experience\)- Client

The StopWatch API provides methods to measure durations in the Next Experience UI Framework.

|Name|Type|Description|
|----|----|-----------|
|started|[Date object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)|Start date and time for the StopWatch. This value is set when calling the constructor [StopWatch\(Object started\)](StopWatchAPINX.md#) or the [restart\(\)](StopWatchAPINX.md#) method.|

**Parent Topic:**[Client Next Experience API reference](../../../../../build/applications/concept/api-client-next.md)

## StopWatch \(Next Experience\) - StopWatch\(Object started\)

Constructor to initialize a new StopWatch.

<table id="table_lgv_pzl_rfc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

started

</td><td>

[Date object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)

</td><td>

Optional. Date and time to use as the start time for the StopWatch.Default: The current date and time.

</td></tr></tbody>
</table>This example initializes a new StopWatch starting at the current date and time.

```
var timer = new nowapi.StopWatch();
```

## StopWatch \(Next Experience\) - getTime\(\)

Returns the elapsed time in milliseconds since the StopWatch started.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_bxh_pxl_rfc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Elapsed time since the StopWatch started.Unit: Milliseconds

</td></tr></tbody>
</table>This example returns the elapsed StopWatch time in milliseconds.

```
var timer = new nowapi.StopWatch();
console.log(timer.started);  //logs the StopWatch start date and time to the console
var millis = timer.getTime();
```

## StopWatch \(Next Experience\) - restart\(\)

Resets the StopWatch start time as the current date and time.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

This example returns the elapsed milliseconds since the timer started and restarted.

```
var timer = new nowapi.StopWatch();
console.log(timer.started);  //logs the StopWatch start date and time to the console
timer.getTime();  //milliseconds since the timer started
timer.restart();
console.log(timer.started);  //logs the new StopWatch start date and time to the console
timer.getTime();  //milliseconds since the timer restarted
```

## StopWatch \(Next Experience\) - toString\(\)

Returns the elapsed time in ISO 8601 format \(HH:mm:ss.sss\) since the StopWatch started.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Duration in ISO 8601 format containing hours, minutes, seconds, and milliseconds \(HH:mm:ss.sss\).|

This example returns the elapsed StopWatch time in the format HH:mm:ss.sss.

```
var timer = new nowapi.StopWatch();
var duration = timer.toString();
```

