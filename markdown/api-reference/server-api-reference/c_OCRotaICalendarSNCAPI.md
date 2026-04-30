---
title: OCRotaICalendarSNC - Global
description: The OCRotaICalendarSNC script include provides iCal formatted events for the a specific user's rotation.Records in the cmn\_rota\_resp\_cache table that have a From date prior to today.Returns list of AJAXScheduleItems for the user's on-call.Creates a VEVENT based on the scheduleItemSpan provided.Creates a formatted iCalendar if the user has no upcoming on-call.Returns the formatted iCalendar for the user's rotation.Returns the formatted iCalendar for the user's rotation if found in the cmn\_rota\_resp\_cache table.Checks whether the provided timeSpan intersects with one of the rota span items.Creates the subscribable URL for the user's iCalendar.Returns a URL to the on-call calendar based on the rota record.Returns an array of the user's overrides \(extra coverage\).Returns an object containing the user's override \(extra coverage\) and excluded spans.Used by business rules on the cmn\_rota\_member, cmn\_schedule\_span, and roster\_schedule\_span tables to update the cmn\_rota\_resp\_cache table.Checks whether the provided timeSpan matches one of the rotaSpanItems.Used by fixed job to populate the calendar subscription fields on the cmn\_rota formReturns an object containing the user's rotations.Inserts the user's iCalendar into the cmn\_rota\_resp\_cache table.Queues events to send an email to all members of the rotation.Returns an object that contains all of the timeSpans that need to be excluded from the user's iCalendar.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# OCRotaICalendarSNC- Global

The OCRotaICalendarSNC script include provides iCal formatted events for the a specific user's rotation.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## OCRotaICalendarSNC - cleanExpiredCache \(\)

Records in the cmn\_rota\_resp\_cache table that have a From date prior to today.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## OCRotaICalendarSNC - createCalendarEvents \(String groupId, String rotaId, String userId, Object dateRangeObj\)

Returns list of AJAXScheduleItems for the user's on-call.

|Name|Type|Description|
|----|----|-----------|
|groupId|String|The group sys id.|
|rotaId|String|The rota sys id.|
|userId|String|The user sys id.|
|dateRangeObj|Object|Contains the from and to dates for the data set.|

|Type|Description|
|----|-----------|
|AJAXScheduleItem|Java list of AJAXScheduleItems.|

## OCRotaICalendarSNC - createCustomEvent \(String groupName, Object scheduleItemSpan, String calendarLink\)

Creates a VEVENT based on the scheduleItemSpan provided.

|Name|Type|Description|
|----|----|-----------|
|groupName|String|Name of the on-call group.|
|scheduleItemSpan|Object|Span of time for the on-call period.|
|calendarLink|String|A link back to the on-call calendar in the instance.|

|Type|Description|
|----|-----------|
|String|A VEVENT based on the scheduleItemSpan provided.|

## OCRotaICalendarSNC - createPlaceholderCalendar \(GlideRecord rotaGR, Object dateRangeObj, String calendarLink\)

Creates a formatted iCalendar if the user has no upcoming on-call.

|Name|Type|Description|
|----|----|-----------|
|rotaGR|GlideRecord|The cmn\_rota glide record.|
|dateRangeObj|Object|Contains the from and to dates for the data set.|
|calendarLink|String|A link to the on-call calendar for this user.|

|Type|Description|
|----|-----------|
|String|Formatted iCalendar with a placeholder VEVENT.|

## OCRotaICalendarSNC - getCalendarEvents \(String groupId , String rotaId, String userId , Object dateRangeObj, Boolean useCache\)

Returns the formatted iCalendar for the user's rotation.

|Name|Type|Description|
|----|----|-----------|
|groupId|String|The group sys id.|
|rotaId|String|The rota sys id.|
|userId|String|The user sys id.|
|dateRangeObj|Object|Contains the from and to dates for the data set.|
|useCache|Boolean|If true, makes use of the cache table cmn\_rota\_resp\_cache.|

|Type|Description|
|----|-----------|
|String|Formatted iCalendar for the user's rotation.|

## OCRotaICalendarSNC - getEventsFromTable \(String groupId, String rotaId, String userId, Object dateRangeObj\)

Returns the formatted iCalendar for the user's rotation if found in the cmn\_rota\_resp\_cache table.

|Name|Type|Description|
|----|----|-----------|
|groupId|String|The group sys id.|
|rotaId|String|The rota sys id.|
|userId|String|The user sys id.|
|dateRangeObj|Object|Contains the from and to dates for the data set.|

|Type|Description|
|----|-----------|
|String|Formatted iCalendar for the user's rotation if found in the cmn\_rota\_resp\_cache table.|

## OCRotaICalendarSNC - getIntersectRotaSpanItem \(ScheduleTimeSpan timeSpan, Array rotaSpanItems\)

Checks whether the provided timeSpan intersects with one of the rota span items.

|Name|Type|Description|
|----|----|-----------|
|timeSpan|ScheduleTimeSpan|A single span for the user's on-call.|
|rotaSpanItems|Array|Contains the user's standard on-call spans.|

|Type|Description|
|----|-----------|
|Object|If the timeSpan intersects with one of the rota span items, returns an object containing the rota span item and the span that it intersects with.|

## OCRotaICalendarSNC - getMemberCalendarURL \(String groupId, Object rotaId, String userId\)

Creates the subscribable URL for the user's iCalendar.

|Name|Type|Description|
|----|----|-----------|
|groupId|String|The group sys id.|
|rotaId|Object|The rota sys id.|
|userId|String|The user sys id.|

|Type|Description|
|----|-----------|
|String|The subscribable URL for the user's iCalendar.|

## OCRotaICalendarSNC - getOnCallCalendarURL \(GlideRecord rotaGR\)

Returns a URL to the on-call calendar based on the rota record.

|Name|Type|Description|
|----|----|-----------|
|rotaGR|GlideRecord|A cmn\_rota record.|

|Type|Description|
|----|-----------|
|String|URL to the on-call calendar based on the rota record.|

## OCRotaICalendarSNC - handleOverrideMember \(AJAXScheduleItem scheduleItem\)

Returns an array of the user's overrides \(extra coverage\).

|Name|Type|Description|
|----|----|-----------|
|scheduleItem|AJAXScheduleItem|A list of AJAXScheduleItems.|

|Type|Description|
|----|-----------|
|Array|An array of the user's overrides \(extra coverage\).|

## OCRotaICalendarSNC - handleRotaMember \(AjaxSchedueItem scheduleItem , Object rotaSpanItems, Object definitionItems, Array repeatRotaSpanIdArr\)

Returns an object containing the user's override \(extra coverage\) and excluded spans.

|Name|Type|Description|
|----|----|-----------|
|scheduleItem|AJAXSchedueItem|A list of AJAXScheduleItems.|
|rotaSpanItems|Object|Contains the user's standard on-call spans.|
|definitionItems|Object|Contains the rota's standard on-call spans.|
|repeatRotaSpanIdArr|Array|An array of rota span sys ids.|

|Type|Description|
|----|-----------|
|Object|Contains the user's override \(extra coverage\) and excluded spans.|

## OCRotaICalendarSNC - invalidateRotaRespCache \(GlideRecord rotaRespCacheGR\)

Used by business rules on the cmn\_rota\_member, cmn\_schedule\_span, and roster\_schedule\_span tables to update the cmn\_rota\_resp\_cache table.

|Name|Type|Description|
|----|----|-----------|
|rotaRespCacheGR|GlideRecord|Record that has been updated.|

|Type|Description|
|----|-----------|
|void| |

## OCRotaICalendarSNC - matchRotaSpanRule\(ScheduleTimeSpan timeSpan, Array rotaSpanItems, Array repeatRotaSpanIdArr, Object seriesStartTimes\)

Checks whether the provided timeSpan matches one of the rotaSpanItems.

|Name|Type|Description|
|----|----|-----------|
|timeSpan|ScheduleTimeSpan|A single span for the user's on-call.|
|rotaSpanItems|Array|Contains the user's standard on-call spans.|
|repeatRotaSpanIdArr|Array|An array of rota span sys ids.|
|seriesStartTimes|Object|Start time of the rota spans.|

|Type|Description|
|----|-----------|
|Boolean|Returns true if the timeSpan matches one of the rotaSpanItems.|

## OCRotaICalendarSNC - populateCalendarSubscriptionSettings \(\)

Used by fixed job to populate the calendar subscription fields on the cmn\_rota form

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## OCRotaICalendarSNC - processSeriesEvent \(List scheduleItems, Array repeatRotaSpanIdArr , String userId\)

Returns an object containing the user's rotations.

|Name|Type|Description|
|----|----|-----------|
|scheduleItems|List|The user's on-call rotation as an AJAXScheduleItem list.|
|repeatRotaSpanIdArr|Array|An array of the cmn\_rota schedule span record sys\_ids.|
|userId|String|The user sys id.|

|Type|Description|
|----|-----------|
|Object|Contains the user's rotations.|

## OCRotaICalendarSNC - saveCalendarEvents \(String groupId, String rotaId, String userId, Object dateRangeObj, String result\)

Inserts the user's iCalendar into the cmn\_rota\_resp\_cache table.

|Name|Type|Description|
|----|----|-----------|
|groupId|String|The group sys id.|
|rotaId|String|The rota sys id.|
|userId|String|The user sys id.|
|dateRangeObj|Object|Contains the from and to dates for the data set.|
|result|String|The user's iCalendar.|

|Type|Description|
|----|-----------|
|void| |

## OCRotaICalendarSNC - sendCalendarURL \(GlideRecord rotaGR\)

Queues events to send an email to all members of the rotation.

|Name|Type|Description|
|----|----|-----------|
|rotaGR|GlideRecord|A cmn\_rota record.|

|Type|Description|
|----|-----------|
|void| |

## OCRotaICalendarSNC - updateExceptionList \(AJAXScheduleItem scheduleItem, ScheduleTimeSpan timeSpan, Array rotaSpanItems\)

Returns an object that contains all of the timeSpans that need to be excluded from the user's iCalendar.

|Name|Type|Description|
|----|----|-----------|
|scheduleItem|AJAXScheduleItem|One AJAXScheduleItem.|
|timeSpan|ScheduleTimeSpan|A single user's standard on-call span.|
|rotaSpanItems|Array|Contains the user's standard on-call spans.|

|Type|Description|
|----|-----------|
|Object|Object that contains all of the timeSpans that need to be excluded from the user's iCalendar.|

