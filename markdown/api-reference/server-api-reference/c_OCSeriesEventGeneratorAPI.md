---
title: OCSeriesEventGenerator - Global
description: The OCSeriesEventGenerator script include provide methods to generate the repeating VEVENTS for a user's iCalendar.Returns an array of the repeating on-call events.Returns an array of VEVENTs that represent the on-call for the provided rotaScheduleSpanGR and the memberScheduleSpanGR.Returns an array of the repeating on-call VEVENTS.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# OCSeriesEventGenerator- Global

The OCSeriesEventGenerator script include provide methods to generate the repeating VEVENTS for a user's iCalendar.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## OCSeriesEventGenerator - getMemberCalendar \(String groupId, String rotaId, String userId, Object dateRangeObj, Object memberSchedules, String calendarLink\)

Returns an array of the repeating on-call events.

|Name|Type|Description|
|----|----|-----------|
|groupId|String|The group sys id.|
|rotaId|String|The rota sys id.|
|userId|String|The user sys id.|
|dateRangeObj|Object|Contains the from and to dates for the data set.|
|memberSchedules|Object|The user's schedule.|
|calendarLink|String|A link back to the on-call calendar in the instance.|

|Type|Description|
|----|-----------|
|Array|Array of the repeating on-call events.|

## OCSeriesEventGenerator - getRosterICalEvents \(GlideRecord rotaScheduleSpanGR, GlideRecord memberScheduleSpanGR, Array seriesStartTimes, Object excludeItems, String repeatUntil, String timeZone, String calendarLink\)

Returns an array of VEVENTs that represent the on-call for the provided rotaScheduleSpanGR and the memberScheduleSpanGR.

|Name|Type|Description|
|----|----|-----------|
|rotaScheduleSpanGR|GlideRecord|A cmn\_schedule\_span glide record for a rota.|
|memberScheduleSpanGR|GlideRecord|A cmn\_schedule\_span glide record for a rota member.|
|seriesStartTimes|Array|An array of the repeating rota span start times.|
|excludeItems|Object|The schedule items that need to be excluded.|
|repeatUntil|String|A formatted ScheduleDateTime string.|
|timeZone|String|Time zone for the on-call rota.|
|calendarLink|String|A link to the on-call calendar for this user.|

|Type|Description|
|----|-----------|
|Array|An array of VEVENTs that represent the on-call for the provided rotaScheduleSpanGR and the memberScheduleSpanGR.|

## OCSeriesEventGenerator - getRosterMemberEvents \(GlideRecord rotaMemberGR, Array seriesStartTimes, Object excludeItems, String repeatUntil, String calendarLink\)

Returns an array of the repeating on-call VEVENTS.

|Name|Type|Description|
|----|----|-----------|
|rotaMemberGR|GlideRecord|A cmn\_rota\_member record.|
|seriesStartTimes|Array|An array of the repeating rota span start times.|
|excludeItems|Object|The schedule items that need to be excluded.|
|repeatUntil|String|A formatted ScheduleDateTime string.|
|calendarLink|String|A link to the on-call calendar for this user.|

|Type|Description|
|----|-----------|
|Array|An array of the repeating on-call VEVENTS|

