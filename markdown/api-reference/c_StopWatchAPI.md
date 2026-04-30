---
title: StopWatch - Client
description: The StopWatch API provides methods to measure the duration of operations.Creates an instance of the StopWatch class.Creates an instance of the StopWatch class using the specified date as the initial value.Returns the number of milliseconds since the timer started.Resets the timer start to the current time.Returns the elapsed time.
locale: en-US
release: zurich
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# StopWatch- Client

The StopWatch API provides methods to measure the duration of operations.

You can use this API in client-side scripts using ListV2 and ListV3 APIs.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## StopWatch - StopWatch\(\)

Creates an instance of the StopWatch class.

Uses the current time as the start time.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var sw = new StopWatch();

// some slow code here
for(var i=0,j=1;i<100000000;i++) {
    j=Math.sqrt(i*i*j);
}

if (sw.getTime() > 500)
    console.log("Long running script. Execution time: [" + sw.toString() + "]");

sw.restart();

// some faster code
for(i=0,j;i<100000;i++) {
    j= i + Math.random() * i;
}

console.log("Finished in: " + sw.getTime() + "ms");
sw.stop();
```

## StopWatch - StopWatch\(Date initialDate\)

Creates an instance of the StopWatch class using the specified date as the initial value.

|Name|Type|Description|
|----|----|-----------|
|initialDate|Date|The initial date for the object.|

## StopWatch - getTime\(\)

Returns the number of milliseconds since the timer started.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_wx2_sm5_lv" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Time since the timer started.Unit: Milliseconds

</td></tr></tbody>
</table>```
var sw = new StopWatch();

// some slow code here
for(var i=0,j=1;i<100000000;i++) {
    j=Math.sqrt(i*i*j);
}

if (sw.getTime() > 500)
    console.log("Long running script. Execution time: [" + sw.toString() + "]");

sw.restart();

// some faster code
for(i=0,j;i<100000;i++) {
    j= i + Math.random() * i;
}

console.log("Finished in: " + sw.getTime() + "ms");
sw.stop();
```

## StopWatch - restart\(\)

Resets the timer start to the current time.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var sw = new StopWatch();

// some slow code here
for(var i=0,j=1;i<100000000;i++) {
    j=Math.sqrt(i*i*j);
}

if (sw.getTime() > 500)
    console.log("Long running script. Execution time: [" + sw.toString() + "]");

sw.restart();

// some faster code
for(i=0,j;i<100000;i++) {
    j= i + Math.random() * i;
}

console.log("Finished in: " + sw.getTime() + "ms");
sw.stop();
```

## StopWatch - toString\(\)

Returns the elapsed time.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ycm_pn5_lv" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Elapsed time. Format: HH:MM:SS.SSS

</td></tr></tbody>
</table>```
var sw = new StopWatch();

// some slow code here
for(var i=0,j=1;i<100000000;i++) {
    j=Math.sqrt(i*i*j);
}

if (sw.getTime() > 500)
    console.log("Long running script. Execution time: [" + sw.toString() + "]");

sw.restart();

// some faster code
for(i=0,j;i<100000;i++) {
    j= i + Math.random() * i;
}

console.log("Finished in: " + sw.getTime() + "ms");
sw.stop();
```

