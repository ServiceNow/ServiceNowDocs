---
title: TimelineSpan - Global
description: The TimelineSpan API provides methods to define a set of properties that describe the characteristics and interactive behavior of an element rendered within a time line item.Adds multiple relationships between the current instance and other TimelineSpan objects by enumerating through the array of JavaScript objects.Adds the specified relationship between the current instance and another TimelineSpan and allows the relationship to open a GlideWindow to display information about the relationship.Adds the specified relationship between the current instance and another time line span with sys\_id strPredecessorSysId.Returns the boolean value of the AllowXDragLeft property.Returns the boolean value of the AllowXDragRight property.Returns the boolean value of the AllowXMove property.Returns the boolean value of the AllowYMove property.Returns the boolean value of the AllowYMovePredecessor property.Returns the name of the current inner segment class for the time line span.Returns the time in milliseconds of the end time of the inner segment portion of the timeline span.Returns the time in milliseconds of the start time of the inner segment portion of the timeline span.Returns a boolean that specifies whether or not the current timeline item has been modified after initialization.Returns a string that specifies the name of the icon class to use for displaying the element on the timeline if the current instance has zero duration.Returns an array of all the predecessor objects associated with the current instance. Each array object is a HashMap that contains a predecessor\_sys\_id and relationship\_sys\_id property.Returns the string name of the background color specified for displaying this span.Returns the string that specifies the text to display adjacent to the time element.Returns the start time in milliseconds of the current TimelineSpan object.Returns the sys\_id of the current object.Returns the name of the table where the sys\_id is referenced.Returns the text/html to display in the tooltip when the TimelineSpan element is being hovered over.Sets a flag that determines whether the element's start date can be dragged left or right therefore adjusting the duration of the task.Sets a flag that determines whether the element's end date can be dragged left or right therefore adjusting the duration of the task.Sets a flag that determines whether the element can be moved to start at a different time.Sets a flag that determines whether the element can be dragged vertically on the timeline.Sets a flag that determines whether a dashed relationship line can be drawn from this element interactively on the timeline.Sets the name of the class to use for stylizing the inner segment if it exists.Creates an inner segment to show within the current timespan defined by the specified range.Sets the icon class to use for displaying the current element on the timeline if the current instance has zero duration.Sets the color for displaying this span.Sets the text to display adjacent to the time element.Sets the start and end dates for the current span.Sets the start and end times for the current span.Sets the text to display in the tooltip when the TimelineSpan element is being hovered over.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# TimelineSpan- Global

The TimelineSpan API provides methods to define a set of properties that describe the characteristics and interactive behavior of an element rendered within a time line item.

Since it is extremely important for all of a time line item's collection of spans to be unique, the creation of a new instance should be performed using the createTimelineItem\(\) method of an existing time line Item instance.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## TimelineSpan - addPredecessor\(Object Array objArray\)

Adds multiple relationships between the current instance and other TimelineSpan objects by enumerating through the array of JavaScript objects.

Each object should have an internal property **relationship\_sys\_id** and **predecessor\_sys\_id** specified.

|Name|Type|Description|
|----|----|-----------|
|objArray|Object Array|JavaScript object array that contains two internal properties:**relationship\_sys\_id** and **predecessor\_sys\_id**.|

|Type|Description|
|----|-----------|
|void| |

## TimelineSpan - addPredecessor\(String strPredecessorSysId, String strRelationshipSysId, String strTableName\)

Adds the specified relationship between the current instance and another TimelineSpan and allows the relationship to open a GlideWindow to display information about the relationship.

|Name|Type|Description|
|----|----|-----------|
|strPredecessorSysId|String|Sys\_id of the planned task record that is the predecessor of the relationship.|
|strRelationshipSysId|String|Sys\_id of the relationship record of the relationship.|
|strTableName|String|Name of the table for the relationship.|

|Type|Description|
|----|-----------|
|void| |

## TimelineSpan - addPredecessor\(String strPredecessorSysId, String strRelationshipSysId\)

Adds the specified relationship between the current instance and another time line span with sys\_id **strPredecessorSysId**.

The drawn line will not have any double click handlers associated with it.

|Name|Type|Description|
|----|----|-----------|
|strPredecessorSysId|String|Sys\_id of the planned task record that is the predecessor of the relationship.|
|strRelationshipSysId|String|Sys\_id of the relationship record of the relationship.|

|Type|Description|
|----|-----------|
|void| |

## TimelineSpan - getAllowXDragLeft\(\)

Returns the boolean value of the **AllowXDragLeft** property.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_fh2_5bs_zt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the object's start time can be adjusted.Valid values:

-   true: Object start time can be adjusted.
-   false: Object start time can't be adjusted.

</td></tr></tbody>
</table>## TimelineSpan - getAllowXDragRight\(\)

Returns the boolean value of the **AllowXDragRight** property.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_hh2_5bs_zt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the object's end time can be adjusted.Valid values:

-   true: Object end time can be adjusted.
-   false: Object end time can't be adjusted.

</td></tr></tbody>
</table>## TimelineSpan - getAllowXMove\(\)

Returns the boolean value of the **AllowXMove** property.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_jh2_5bs_zt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the object can be moved horizontally.Valid values:

-   true: Object can be moved horizontally.
-   false: Object can't be moved horizontally.

</td></tr></tbody>
</table>## TimelineSpan - getAllowYMove\(\)

Returns the boolean value of the **AllowYMove** property.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_rhw_gds_zt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the object can be moved vertically.Valid values:

-   true: Object can be moved vertically.
-   false: Object can't be moved vertically.

</td></tr></tbody>
</table>## TimelineSpan - getAllowYMovePredecessor\(\)

Returns the boolean value of the **AllowYMovePredecessor** property.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_thw_gds_zt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the a dashed relationship line can be drawn from the current object to a new successor.Valid values:

-   true: Dashed relationship line can be drawn from the current object to a new successor.
-   false: Dashed relationship line can't be drawn from the current object to a new successor.

</td></tr></tbody>
</table>## TimelineSpan - getInnerSegmentClass\(\)

Returns the name of the current inner segment class for the time line span.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the class for the current inner segment style.|

## TimelineSpan - getInnerSegmentEndTimeMs\(\)

Returns the time in milliseconds of the end time of the inner segment portion of the timeline span.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_zhw_gds_zt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

End time of the timeline span inner segment portion.Unit: Milliseconds

</td></tr></tbody>
</table>## TimelineSpan - getInnerSegmentStartTimeMs\(\)

Returns the time in milliseconds of the start time of the inner segment portion of the timeline span.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_b3w_gds_zt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Start time of the timeline span inner segment portion.Unit: Milliseconds

</td></tr></tbody>
</table>## TimelineSpan - getIsChanged\(\)

Returns a boolean that specifies whether or not the current timeline item has been modified after initialization.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_obm_g2s_zt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the current span has been marked as changed.Valid values:

-   true: Marked as changed.
-   false: Not marked as changed.

</td></tr></tbody>
</table>## TimelineSpan - getPointIconClass\(\)

Returns a string that specifies the name of the icon class to use for displaying the element on the timeline if the current instance has zero duration.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the icon class to use for displaying the current timeline span if the duration is zero.|

## TimelineSpan - getPredecessors\(\)

Returns an array of all the predecessor objects associated with the current instance. Each array object is a HashMap that contains a `predecessor_sys_id` and `relationship_sys_id` property.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object Array|List of HashMaps that contain two internal properties: `predecessor_sys_id` and `relationship_sys_id`.|

## TimelineSpan - getSpanColor\(\)

Returns the string name of the background color specified for displaying this span.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|HTML color name to use as the background color for the element.|

## TimelineSpan - getSpanText\(\)

Returns the string that specifies the text to display adjacent to the time element.

**Note:** This text only displays if the GlideTimeline object has enabled timeline text defined using the `glideTimeline.showTimelineText(true)` method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Text displayed adjacent to the element.|

## TimelineSpan - getStartTimeMs\(\)

Returns the start time in milliseconds of the current TimelineSpan object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ybm_g2s_zt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Start time of the element.Unit: Milliseconds

</td></tr></tbody>
</table>## TimelineSpan - getSysId\(\)

Returns the sys\_id of the current object.

This method is useful for returning the sys\_id when the current object instance was created without a specific sys\_id to obtain the dynamically generated GUID.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Unique sys\_id of the current element.|

## TimelineSpan - getTable\(\)

Returns the name of the table where the sys\_id is referenced.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Table name.|

## TimelineSpan - getTooltip\(\)

Returns the text/html to display in the tooltip when the TimelineSpan element is being hovered over.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Tooltip text.|

## TimelineSpan - setAllowXDragLeft\(Boolean bFlag\)

Sets a flag that determines whether the element's start date can be dragged left or right therefore adjusting the duration of the task.

The effect of this behavior is controlled by the script include that handles the appropriate event. The default value for this property is false.

<table id="table_hzv_rfs_zt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

bFlag

</td><td>

Boolean

</td><td>

Flag that indicates whether the element's start date can be adjusted.Valid values:

-   true: Start date can be adjusted.
-   false: Start date can't be adjusted.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

## TimelineSpan - setAllowXDragRight\(Boolean bFlag\)

Sets a flag that determines whether the element's end date can be dragged left or right therefore adjusting the duration of the task.

The effect of this behavior is controlled by the script include that handles the appropriate event. The default value for this property is false.

<table id="table_jzv_rfs_zt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

bFlag

</td><td>

Boolean

</td><td>

Flag that indicates whether the element's end date can be adjusted.Valid values:

-   true: End date can be adjusted.
-   false: End date can't be adjusted.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

## TimelineSpan - setAllowXMove\(Boolean bFlag \)

Sets a flag that determines whether the element can be moved to start at a different time.

The effect of this behavior is controlled by the script include that handles the appropriate event. The default value for this property is false.

<table id="table_lzv_rfs_zt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

bFlag

</td><td>

Boolean

</td><td>

Flag that indicates whether the element can be moved horizontally.Valid values:

-   true: Element can be moved horizontally.
-   false: Element can't be moved horizontally.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

## TimelineSpan - setAllowYMove\(Boolean bFlag \)

Sets a flag that determines whether the element can be dragged vertically on the timeline.

The effect of this behavior is controlled by the script include that handles the appropriate event. The default value for this property is false.

<table id="table_hgg_sgs_zt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

bFlag

</td><td>

Boolean

</td><td>

Flag that indicates whether the element can be moved vertically.Valid values:

-   true: Element can be moved vertically.
-   false: Element can't be moved vertically.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

## TimelineSpan - setAllowYMovePredecessor\(Boolean bFlag\)

Sets a flag that determines whether a dashed relationship line can be drawn from this element interactively on the timeline.

The effect of this behavior is controlled by the script include that handles the appropriate event. The default value for this property is false.

<table id="table_jgg_sgs_zt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

bFlag

</td><td>

Boolean

</td><td>

Flag that indicates whether the a dashed relationship line can be drawn from the current object to a new successor.Valid values:

-   true: Dashed relationship line can be drawn from the current object to a new successor.
-   false: Dashed relationship line can't be drawn from the current object to a new successor.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

## TimelineSpan - setInnerSegmentClass\(String styleClass\)

Sets the name of the class to use for stylizing the inner segment if it exists.

<table id="table_lgg_sgs_zt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

styleClass

</td><td>

String

</td><td>

Name of the color class to use to stylize the inner segment. Valid values:

-   blue
-   green
-   silver

Default: green

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

## TimelineSpan - setInnerSegmentTimeSpan\(Number startTimeMs, Number endTimeMs\)

Creates an inner segment to show within the current timespan defined by the specified range.

<table id="table_ngg_sgs_zt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

startTimeMs

</td><td>

Number

</td><td>

Start time.Unit: Milliseconds

</td></tr><tr><td>

endTimeMs

</td><td>

Number

</td><td>

End time.Unit: Milliseconds

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

## TimelineSpan - setPointIconClass\(String iconClassName\)

Sets the icon class to use for displaying the current element on the timeline if the current instance has zero duration.

**Note:** This only affects the current TimelineSpan object and will take precedence over the defaultPointIconClass specified by the GlideTimeline.

<table id="table_pgg_sgs_zt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

iconClassName

</td><td>

String

</td><td>

Icon class to use to display the current element on the timeline if the current instance has zero duration.Valid values:

-   `black_circle`
-   `black_square`
-   `blue_circle`
-   `blue_square`
-   `green_circle`
-   `green_square`
-   `milestone`
-   `red_circle`
-   `red_square`
-   `sepia_circle`
-   `sepia_square`

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

## TimelineSpan - setSpanColor\(String strColor\)

Sets the color for displaying this span.

|Name|Type|Description|
|----|----|-----------|
|strColor|String|HTML name for the color of this span.|

|Type|Description|
|----|-----------|
|void| |

## TimelineSpan - setSpanText\(String strSpanText\)

Sets the text to display adjacent to the time element.

**Note:** This text only displays if the GlideTimeline object has enabled timeline text set using the glideTimeline.showTimelineText\(true\) method.

|Name|Type|Description|
|----|----|-----------|
|strSpanText|String|Text to display next to the time element.|

|Type|Description|
|----|-----------|
|void| |

## TimelineSpan - setTimeSpan\(Number nStartTime, Number nEndTimeMs\)

Sets the start and end dates for the current span.

<table id="table_yqd_l3s_zt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

nStartTime

</td><td>

Number

</td><td>

Start time.Unit: Milliseconds

</td></tr><tr><td>

nEndTimeMs

</td><td>

Number

</td><td>

End time.Unit: Milliseconds

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

## TimelineSpan - setTimeSpan\(String strStartTime, String strEndTimeMs\)

Sets the start and end times for the current span.

<table id="table_yqd_l3s_zt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

strStartTime

</td><td>

String

</td><td>

Start time.Unit: Milliseconds

</td></tr><tr><td>

strEndTimeMs

</td><td>

String

</td><td>

End time.Unit: Milliseconds

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

## TimelineSpan - setTooltip\(String strTooltipText\)

Sets the text to display in the tooltip when the TimelineSpan element is being hovered over.

<table id="table_ard_l3s_zt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

strTooltipText

</td><td>

String

</td><td>

Text to display in the tooltip.**Note:** You can specify valid HTML in this string.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

