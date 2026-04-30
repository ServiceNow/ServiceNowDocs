---
title: OCRotation - Global
description: The OCRotation script include provides methods to build a data structure that is used to display a calendar.Builds the on-call coverage based on your groups, rotas, and rosters. This is used by the OCRotationV2 - getSpans method.Returns the end date for the time period for which you want to retrieve on-call coverage.Returns a comma separated list of group sys\_id \(sys\_user\_group\) values for an on-call schedule.Returns the rosters according to the selected rotas.Returns a GlideRecord for the cmn\_rota table filtered by groups, rota, users, and roster.Returns the rotas for the groups on your calendar.Returns the start date for the time period for which you want to retrieve on-call coverage.Returns the timezone that your on-call calendar will use.This will filter the schedules return by users. Get comma separated list of user sys\_id \(sys\_user\) values used to filter on-call schedules.Set the end date for the time period for which you want to retrieve on-call coverage. If the end date is not set, then the last day of the next month is applied by default. Use in conjunction with OCRotationV2 - getSpans.Filters the schedules return by groups. Set comma separated list of group sys\_id \(sys\_user\_group\) values for an on-call schedule. Use in conjunction with OCRotationV2 - getSpans.Sets the rosters according to the selected rotas. Use in conjunction with OCRotationV2 - getSpans.Sets the rotas for the groups on your calendar. Use in conjunction with OCRotationV2 - getSpans.Sets the start date for the time period for which you want to retrieve on-call coverage. If the start date is not set, then the first day of the previous month is applied by default. Use in conjunction with OCRotationV2 - getSpans.Sets the timezone that your on-call calendar will use. Use in conjunction with OCRotationV2 - getSpans.Sets comma separated list of user sys\_id \(sys\_user\) values used to filter on-call schedules. Use in conjunction with OCRotationV2 - getSpans.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# OCRotation- Global

The OCRotation script include provides methods to build a data structure that is used to display a calendar.

The code builds up the GlideAJAXSchedulePage object which stores a list of span items. You can use this type for the Gwt \(legacy\) calendar. See the [OCRotationV2 - Global](../../OCRotationV2/Concept/c_OCRotationV2.md#) script include for other calender types. This is part of On-Call Scheduling.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## OCRotation - buildRotas\(\)

Builds the on-call coverage based on your groups, rotas, and rosters. This is used by the OCRotationV2 - getSpans method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Void| |

**Related topics**  


[OCRotationV2 - getSpans\(\)](../../OCRotationV2/Concept/c_OCRotationV2.md#)

## OCRotation - getEndDate\(\)

Returns the end date for the time period for which you want to retrieve on-call coverage.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|End date for the time period for which you want to retrieve on-call coverage.|

## OCRotation - getGroupIds\(\)

Returns a comma separated list of group sys\_id \(sys\_user\_group\) values for an on-call schedule.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Comma separated list of group sys\_id \(sys\_user\_group\) values for an on-call schedule.|

## OCRotation - getRosterIds\(\)

Returns the rosters according to the selected rotas.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Rosters according to the selected rotas.|

## OCRotation - getRotaGr\(String rotaIds, String groupIds, String rosterIds, String userIds\)

Returns a GlideRecord for the cmn\_rota table filtered by groups, rota, users, and roster.

|Name|Type|Description|
|----|----|-----------|
|rotaIds|String|Comma separated list of rota sys\_id \(cmn\_rota\) values for an on-call schedule.|
|groupIds|String|Comma separated list of group sys\_id \(sys\_user\_group\) values for an on-call schedule.|
|rosterIds|String|Comma separated list of roster sys\_id \(cmn\_rota\_roster\) values for an on-call schedule.|
|userIds|String|Comma separated list of user sys\_id \(sys\_user\) values for an on-call schedule.|

|Type|Description|
|----|-----------|
|GlideRecord|A GlideRecord for the cmn\_rota table filtered by groups, rota, users, and roster.|

## OCRotation - getRotaIds\(\)

Returns the rotas for the groups on your calendar.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Rotas for the groups on your calendar.|

## OCRotation - getStartDate\(\)

Returns the start date for the time period for which you want to retrieve on-call coverage.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Start date for the time period for which you want to retrieve on-call coverage.|

## OCRotation - getTimezone\(\)

Returns the timezone that your on-call calendar will use.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Timezone that your on-call calendar will use. For example, **Europe/Madrid** and **US/Pacific**.|

## OCRotation - getUserIDs\(\)

This will filter the schedules return by users. Get comma separated list of user sys\_id \(sys\_user\) values used to filter on-call schedules.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Comma separated list of user sys\_id \(sys\_user\) values used to filter on-call schedules.|

## OCRotation - setEndDate\(String endDate, Boolean inclusive\)

Set the end date for the time period for which you want to retrieve on-call coverage. If the end date is not set, then the last day of the next month is applied by default. Use in conjunction with OCRotationV2 - getSpans.

|Name|Type|Description|
|----|----|-----------|
|endDate|String|\[Optional\] End date of the on-call schedule.|
|inclusive|Boolean|\[Optional\] When true, the end date is included in the time span. If not specified, this value defaults to true.|

|Type|Description|
|----|-----------|
|Void| |

**Related topics**  


[OCRotationV2 - getSpans\(\)](../../OCRotationV2/Concept/c_OCRotationV2.md#)

## OCRotation - setGroupIds\(String groupIds\)

Filters the schedules return by groups. Set comma separated list of group sys\_id \(sys\_user\_group\) values for an on-call schedule. Use in conjunction with OCRotationV2 - getSpans.

|Name|Type|Description|
|----|----|-----------|
|groupIds|String|Comma separated list of group sys\_id \(sys\_user\_group\) values for an on-call schedule.|

|Type|Description|
|----|-----------|
|Void| |

**Related topics**  


[OCRotationV2 - getSpans\(\)](../../OCRotationV2/Concept/c_OCRotationV2.md#)

## OCRotation - setRosterIds\(String rosterIds\)

Sets the rosters according to the selected rotas. Use in conjunction with OCRotationV2 - getSpans.

|Name|Type|Description|
|----|----|-----------|
|RosterIds|String|Rosters according to the selected rotas.|

|Type|Description|
|----|-----------|
|void| |

**Related topics**  


[OCRotationV2 - getSpans\(\)](../../OCRotationV2/Concept/c_OCRotationV2.md#)

## OCRotation - setRotaIds\(String rotaIds\)

Sets the rotas for the groups on your calendar. Use in conjunction with OCRotationV2 - getSpans.

|Name|Type|Description|
|----|----|-----------|
|RotaIds|String|Rotas for the groups on your calendar.|

|Type|Description|
|----|-----------|
|Void| |

**Related topics**  


[OCRotationV2 - getSpans\(\)](../../OCRotationV2/Concept/c_OCRotationV2.md#)

## OCRotation - setStartDate\(String startDate\)

Sets the start date for the time period for which you want to retrieve on-call coverage. If the start date is not set, then the first day of the previous month is applied by default. Use in conjunction with OCRotationV2 - getSpans.

|Name|Type|Description|
|----|----|-----------|
|startDate|String|\[Optional\] Start date for the time period for which you want to retrieve on-call coverage.|

|Type|Description|
|----|-----------|
|void| |

**Related topics**  


[OCRotationV2 - getSpans\(\)](../../OCRotationV2/Concept/c_OCRotationV2.md#)

## OCRotation - setTimezone\(String timezone\)

Sets the timezone that your on-call calendar will use. Use in conjunction with OCRotationV2 - getSpans.

|Name|Type|Description|
|----|----|-----------|
|Timezone|String|Timezone that your on-call calendar will use. For example, **Europe/Madrid** and **US/Pacific**.|

|Type|Description|
|----|-----------|
|Void| |

**Related topics**  


[OCRotationV2 - getSpans\(\)](../../OCRotationV2/Concept/c_OCRotationV2.md#)

## OCRotation - setUserIds\(String userIds\)

Sets comma separated list of user sys\_id \(sys\_user\) values used to filter on-call schedules. Use in conjunction with OCRotationV2 - getSpans.

|Name|Type|Description|
|----|----|-----------|
|UserIds|String|Comma separated list of user sys\_id \(sys\_user\) values used to filter on-call schedules.|

|Type|Description|
|----|-----------|
|Void| |

**Related topics**  


[OCRotationV2 - getSpans\(\)](../../OCRotationV2/Concept/c_OCRotationV2.md#)

