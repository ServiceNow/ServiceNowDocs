---
title: OCRotationV2 - Global
description: The OCRotationV2 script include is an extension of OCRotation script include, which is used by Fullcalendar.io and the DHTMLX On-Call Calendar.Returns an array of groups that have active rotas.Returns an array of active rosters for a given rota ID.Returns an array of active rotas for a given group ID.Get the spans from the specified start date to the specified end date. If no start and end dates are provided, the start date defaults to a month before and the end date defaults to a month after the current time. You can also use the groups IDs, rota IDs, roster IDs, user IDs to further filter the spans.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# OCRotationV2- Global

The OCRotationV2 script include is an extension of OCRotation script include, which is used by Fullcalendar.io and the DHTMLX On-Call Calendar.

Use this script include to obtain the schedule time span between two dates that are further filtered by groups, rotas, rosters, and users. You can also extend OCRotationV2 to add or modify behavior. This is part of On-Call Scheduling.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## OCRotationV2 - getGroups\(\)

Returns an array of groups that have active rotas.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_pzg_nlb_h5" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

An array of group objects. Each contains the following attributes: -   sys\_id of the sys\_user\_group record
-   name of the sys\_user\_group record

</td></tr></tbody>
</table>## OCRotationV2 - getRostersByRotas\(String rotaSysIds\)

Returns an array of active rosters for a given rota ID.

|Name|Type|Description|
|----|----|-----------|
|rotaSysIds|String|Comma separated list of rota sys\_id \(cmn\_rota\) values.|

<table id="table_z14_1mb_h5" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

An array of rota objects. Each contains the following attributes:-   sys\_id of the cmn\_rota\_roster record
-   name of the cmn\_rota\_roster record
-   rota sys\_id of the cmn\_rota record

</td></tr></tbody>
</table>## OCRotationV2 - getRotasByGroup\(String groupSysIds\)

Returns an array of active rotas for a given group ID.

|Name|Type|Description|
|----|----|-----------|
|groupSysIds|String|Comma separated list of group sys\_id \(sys\_user\_group\) values.|

<table id="table_kcg_xlb_h5" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

An array of rota objects. Each contains the following attributes:-   sys\_id of the cmn\_rota record
-   name of the cmn\_rota record
-   group sys\_id of the sys\_user\_group record

</td></tr></tbody>
</table>## OCRotationV2 - getSpans\(\)

Get the spans from the specified start date to the specified end date. If no start and end dates are provided, the start date defaults to a month before and the end date defaults to a month after the current time. You can also use the groups IDs, rota IDs, roster IDs, user IDs to further filter the spans.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|An array of spans. Each contains the following attributes: id, sys\_id, table, rota\_id, roster\_id, user\_id, text, description, color, textColor, start\_date, end\_date.|

Get all spans for the default time period

```
var spans = new OCRotationV2().getSpans();
var firstSpanStartDate = spans[0].start_date; // get the first span's start date
```

Get all spans between 1st April 2014 and 5th June 2014

```
var spans = new OCRotationV2()
    .setStartDate("2014-04-01")
    .setEndDate("2014-06-05")
    .getSpans();

```

Get the Network group's spans for the default time period

```
var spans = new OCRotationV2()
     .setGroupIds("287ebd7da9fe198100f92cc8d1d2154e")
     .getSpans();

```

Get ITIL User's spans between 1st January 2014 and 31st January 2014

```
var spans = new OCRotationV2()
    .setStartDate("2014-01-01")
    .setEndDate("2014-01-31")
    .setUserIds("681b365ec0a80164000fb0b05854a0cd")
    .getSpans();

```

