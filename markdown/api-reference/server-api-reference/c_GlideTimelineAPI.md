---
title: GlideTimeline - Global
description: The GlideTimeline API provides the core implementation for configuring and displaying a Glide Windowing Toolkit Timeline.Specifies whether or not to group timeline items by their parent. If true, this will nest all child items inside their parent. This affects the ordering of display and children will always be listed immediately after their parent. The default value for the groupByParent property is false.Registers the specified Timeline server event. The strServerEvent must be one of the allowed events for registration to work correctly. When the event occurs, the GlideTimeline sends a request to the server and processes the event as handled inside the strScriptIncludeName class.Specifies the number of seconds to wait before performing an auto refresh of the data on the timeline. Setting the number of seconds to 0 will turn auto refresh off. By default, auto refresh is disabled. If intSeconds is greater than 0 and less than the minimum allowed time in seconds \(10\), it will be set to 10 seconds.Specifies the default icon class to use for Timeline Spans with zero duration if no icon class was explicitly specified in the properties of the Timeline Span returned from the server. The default value for the setDefaultPointIconClass property is milestone.Allows setting of additional parameters in the client script to be made available to the corresponding Script Include events by using the getParameter\(\) method. URI parameters that are prefixed with sysparm\_timeline\_ will automatically be included in all server side AJAX calls.Specifies the initial viewable range for the timeline. The format of the start and end dates must be in the default timestamp format: yyyy-MM-dd HH:mm:ss. The default range is the range that specifies the earliest Timeline Span point to the end of the latest Timeline Span. If the initialViewRange property is specified, it will override the default range.Specifies the initial viewable range for the timeline. The default range is the range that specifies the earliest Timeline Span point to the end of the latest Timeline Span. If the initialViewRange property is specified, it will override the default range.Specifies the initial viewable range for the timeline. The default range is the range that specifies the earliest Timeline Span point to the end of the latest Timeline Span. If the initialViewRange property is specified, it will override the default range.Specifies the initial viewable range for the timeline. The default range is the range that specifies the earliest Timeline Span point to the end of the latest Timeline Span. If the initialViewRange property is specified, it will override the default range.Enables or disables all timeline event interaction. If enabled, event interaction is determined from the corresponding attributes specified by each Timeline Item. The default value for the readOnly property is false.Specifies whether or not to show dependency lines between Timeline Spans. This method applies only if the set of Timeline Items returned from the server includes dependency relationships. The default value for the showDependencyLines property is false.Specifies whether or not to show grid lines for each row of data on the timeline. By default, grid lines are enabled.Specifies whether or not to show the left hand pane in the timeline. The default value for the leftPane property is true.Specifies how to show child items in the left pane of the timeline. Child items are displayed either as nested, indented nodes with expand and collapse capability or on a single indent level. The default value for the showLeftPaneAsTree property is false.Specifies whether or not to show the text input box at the bottom of the left pane with a default value as specified by strDefaultValue. If the left pane is diabled via showLeftPane\(\), the input box will not be visible. The default value for the showLeftPaneInputBox property is false.Specifies whether or not to show the summary pane at the bottom of the timeline. The default value for the showSummaryPane property is true.Specifies whether or not to show the timeline text underneath each Timeline Span in the primary timeline pane. The default value for the showTimelineText property is false.Specifies whether or not the vertical movement of timeline span objects \(if appropriately registered to perform this event\) should snap adjust into the closest row. By default this value is enabled.Specifies whether or not to group items by their left label text. The default value for the sortByLeftLabelText property is false.Specifies whether or not to sort the list of Timeline Items returned by the earliest start date of an item's Timeline Span objects. If groupByParent\(\) is set true, items are sorted after grouping has occurred. The default value for the sortByStartDate property is false.Specifies whether or not to sort the list of Timeline Items returned in alphabetical order according to the text that was specified to show in the Timeline Pane.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 11
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideTimeline- Global

The GlideTimeline API provides the core implementation for configuring and displaying a Glide Windowing Toolkit Timeline.

For security, the GlideTimeline has already been instantiated as a single instance variable called *GlideTimeline*. All configurations should be made in the client script section of the corresponding schedule page that references this instance variable.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideTimeline - groupByParent\(Boolean b\)

Specifies whether or not to group timeline items by their parent. If **true**, this will nest all child items inside their parent. This affects the ordering of display and children will always be listed immediately after their parent. The default value for the **groupByParent** property is **false**.

If **true**, this will nest all child items inside their parent. This affects the ordering of display and children will always be listed immediately after their parent. The default value for the **groupByParent** property is **false**.

|Name|Type|Description|
|----|----|-----------|
|b|Boolean|If **true**, displays Timeline Items grouped by parent.|

|Type|Description|
|----|-----------|
|void| |

```
glideTimeline.groupByParent(true);
```

## GlideTimeline - registerEvent\(String strServerEvent, String strScriptIncludeName\)

Registers the specified Timeline server event. The strServerEvent must be one of the allowed events for registration to work correctly. When the event occurs, the GlideTimeline sends a request to the server and processes the event as handled inside the strScriptIncludeName class.

The strServerEvent must be one of the allowed events for registration to work correctly. When the event occurs, the GlideTimeline sends a request to the server and processes the event as handled inside the strScriptIncludeName class.

<table id="table_opw_v4s_5t" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

strServerEvent

</td><td>

String

</td><td>

Specifies one of the following case-sensitive events: -   **getItems**
-   **elementMoveX**
-   **elementMoveY**
-   **elementMoveXY**
-   **elementSuccessor**
-   **elementTimeAdjustStart**
-   **elementTimeAdjustEnd**
-   **inputBox**
-   **itemMove**

</td></tr><tr><td>

strScriptIncludeName

</td><td>

String

</td><td>

Specifies the name of the class to receive the **strServerEvent**. This class must be defined in a script include that extends AbstractTimelineSchedulePage.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
glideTimeline.registerEvent("getItems", "TimelineGanttSchedulePage");
```

## GlideTimeline - setAutoRefresh\(Number intSeconds\)

Specifies the number of seconds to wait before performing an auto refresh of the data on the timeline. Setting the number of seconds to 0 will turn auto refresh off. By default, auto refresh is disabled. If **intSeconds** is greater than 0 and less than the minimum allowed time in seconds \(10\), it will be set to 10 seconds.

Setting the number of seconds to 0 will turn auto refresh off. By default, auto refresh is disabled. If intSeconds is greater than 0 and less than the minimum allowed time in seconds \(10\), it will be set to 10 seconds.

|Name|Type|Description|
|----|----|-----------|
|intSeconds|Number|An integer specifying the time in seconds between auto-refreshing.|

|Type|Description|
|----|-----------|
|void| |

```
glideTimeline.setAutoRefresh(15); // Sets the interval for auto-refreshing to 15 seconds.
```

## GlideTimeline - setDefaultPointIconClass\(String icon\_class\)

Specifies the default icon class to use for Timeline Spans with zero duration if no icon class was explicitly specified in the properties of the Timeline Span returned from the server. The default value for the setDefaultPointIconClass property is **milestone**.

The default value for the setDefaultPointIconClass property is **milestone**.

<table id="table_c2p_mns_5t" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

icon\_class

</td><td>

String

</td><td>

String that specifies one of the following values: -   `milestone`
-   `blue_square`
-   `sepia_square`
-   `green_square`
-   `red_square`
-   `black_square`
-   `blue_circle`
-   `sepia_circle`
-   `green_circle`
-   `red_circle`
-   `black_circle`

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
glideTimeline.setDefaultPointIconClass('blue_circle');
```

## GlideTimeline - setExtraAjaxParam\(String strName, String strValue\)

Allows setting of additional parameters in the client script to be made available to the corresponding Script Include events by using the getParameter\(\) method. URI parameters that are prefixed with `sysparm_timeline_` will automatically be included in all server side AJAX calls.

URI parameters that are prefixed with `sysparm_timeline_` will automatically be included in all server side AJAX calls.

|Name|Type|Description|
|----|----|-----------|
|strName|String|The URI parameter name.|
|strValue|String|The value of strName.|

|Type|Description|
|----|-----------|
|void| |

```
glideTimeline.setExtraAjaxParam("sysparm_timeline_limit", "5");
```

## GlideTimeline - setInitialViewRange\(String objStartDate, String objEndDate\)

Specifies the initial viewable range for the timeline. The format of the start and end dates must be in the default timestamp format: yyyy-MM-dd HH:mm:ss. The default range is the range that specifies the earliest Timeline Span point to the end of the latest Timeline Span. If the **initialViewRange** property is specified, it will override the default range.

The format of the start and end dates must be in the default timestamp format: yyyy-MM-dd HH:mm:ss. The default range is the range that specifies the earliest Timeline Span point to the end of the latest Timeline Span. If the **initialViewRange** property is specified, it will override the default range.

|Name|Type|Description|
|----|----|-----------|
|objStartDate|String|The start time of the view range in format: yyyy-MM-dd HH:mm:ss .|
|objEndDate|String|The end time of the view range in format: yyyy-MM-dd HH:mm:ss .|

|Type|Description|
|----|-----------|
|void| |

```
// Sets the initial range to begin on June 20th, 2010 at 8:00 AM and end on June 28th, 2010 at 2:00 PM UTC time.
      glideTimeline.setInitialViewRange("2010-06-20 08:00:00", "2010-06-28 14:00:00");
    
```

## GlideTimeline - setInitialViewRange\(Number objStartDate, Number objEndDate\)

Specifies the initial viewable range for the timeline. The default range is the range that specifies the earliest Timeline Span point to the end of the latest Timeline Span. If the **initialViewRange** property is specified, it will override the default range.

The default range is the range that specifies the earliest Timeline Span point to the end of the latest Timeline Span. If the **initialViewRange** property is specified, it will override the default range.

|Name|Type|Description|
|----|----|-----------|
|objStartDate|Number|The start time of the view range in milliseconds.|
|objEndDate|Number|The end time in milliseconds.|

|Type|Description|
|----|-----------|
|void| |

```
// Sets the initial range to begin on June 20th, 2010 at 8:00 AM and end on June 28th, 2010 at 2:00 PM UTC time.
      glideTimeline.setInitialViewRange(1277046000000, 1277647200000);
```

## GlideTimeline - setInitialViewRange\(String objStartDate, Number objEndDate\)

Specifies the initial viewable range for the timeline. The default range is the range that specifies the earliest Timeline Span point to the end of the latest Timeline Span. If the **initialViewRange** property is specified, it will override the default range.

The default range is the range that specifies the earliest Timeline Span point to the end of the latest Timeline Span. If the **initialViewRange** property is specified, it will override the default range.

|Name|Type|Description|
|----|----|-----------|
|objStartDate|String|The start time of the view range in format: yyyy-MM-dd HH:mm:ss .|
|objEndDate|Number|The end time in milliseconds.|

|Type|Description|
|----|-----------|
|void| |

ExampleExplanation

```
// Sets the initial range to begin on June 20th, 2010 at 8:00 AM and end on June 28th, 2010 at 2:00 PM UTC time.
      glideTimeline.setInitialViewRange("2010-06-20 08:00:00", 1277647200000);
```

## GlideTimeline - setInitialViewRange\(Number objStartDate, String objEndDate\)

Specifies the initial viewable range for the timeline. The default range is the range that specifies the earliest Timeline Span point to the end of the latest Timeline Span. If the **initialViewRange** property is specified, it will override the default range.

The default range is the range that specifies the earliest Timeline Span point to the end of the latest Timeline Span. If the **initialViewRange** property is specified, it will override the default range.

|Name|Type|Description|
|----|----|-----------|
|objStartDate|Number|The start time of the view range in milliseconds.|
|objEndDate|String|The end time of the view range in format: yyyy-MM-dd HH:mm:ss .|

|Type|Description|
|----|-----------|
|void| |

ExampleExplanation

```
// Sets the initial range to begin on June 20th, 2010 at 8:00 AM and end on June 28th, 2010 at 2:00 PM UTC time.
      glideTimeline.setInitialViewRange(1277046000000, "2010-06-28 14:00:00");
```

## GlideTimeline - setReadOnly\(Boolean b\)

Enables or disables all timeline event interaction. If enabled, event interaction is determined from the corresponding attributes specified by each Timeline Item. The default value for the **readOnly** property is **false**.

If enabled, event interaction is determined from the corresponding attributes specified by each Timeline Item. The default value for the **readOnly** property is **false**.

|Name|Type|Description|
|----|----|-----------|
|b|Boolean|If **true**, marks the entire timeline as **read-only** \(non-interactive\).|

|Type|Description|
|----|-----------|
|void| |

```
glideTimeline.setReadOnly(true);
```

## GlideTimeline - showDependencyLines\(Boolean b\)

Specifies whether or not to show dependency lines between Timeline Spans. This method applies only if the set of Timeline Items returned from the server includes dependency relationships. The default value for the showDependencyLines property is **false**.

This method applies only if the set of Timeline Items returned from the server includes dependency relationships. The default value for the showDependencyLines property is **false**.

|Name|Type|Description|
|----|----|-----------|
|b|Boolean|If **true**, displays dependency lines on the timeline; otherwise, does not.|

|Type|Description|
|----|-----------|
|void| |

```
glideTimeline.showDependencyLines(true);
```

## GlideTimeline - showGridLines\(Boolean bShowGridlines, Number amount\)

Specifies whether or not to show grid lines for each row of data on the timeline. By default, grid lines are enabled.

By default, grid lines are enabled.

|Name|Type|Description|
|----|----|-----------|
|bShowGridlines|Boolean|If **true**, timeline shows grid lines; otherwise, does not display grid lines.|
|amount|Number|amount|

|Type|Description|
|----|-----------|
|void|ReturnValue|

```
glideTimeline.showGridLines(false); // Disables grid lines.
```

## GlideTimeline - showLeftPane\(Boolean b\)

Specifies whether or not to show the left hand pane in the timeline. The default value for the **leftPane** property is **true**.

The default value for the **leftPane** property is **true**.

|Name|Type|Description|
|----|----|-----------|
|b|Boolean|If **true**, the timeline shows the left pane; otherwise, the left pane is not be displayed.|

|Type|Description|
|----|-----------|
|void| |

```
glideTimeline.showLeftPane(false);
```

## GlideTimeline - showLeftPaneAsTree\(Boolean b\)

Specifies how to show child items in the left pane of the timeline. Child items are displayed either as nested, indented nodes with expand and collapse capability or on a single indent level. The default value for the **showLeftPaneAsTree** property is **false**.

The default value for the **showLeftPaneAsTree** property is **false**.

|Name|Type|Description|
|----|----|-----------|
|b|Boolean|If **true**, child item nodes are shown as indented with expand/collapse capability; otherwise, all left pane items are displayed at a single indent level.|

|Type|Description|
|----|-----------|
|void| |

```
glideTimeline.showLeftPaneAsTree(true);
```

## GlideTimeline - showLeftPaneInputBox\(Boolean b, String strDefaultValue\)

Specifies whether or not to show the text input box at the bottom of the left pane with a default value as specified by **strDefaultValue**. If the left pane is diabled via showLeftPane\(\), the input box will not be visible. The default value for the **showLeftPaneInputBox** property is **false**.

If the left pane is diabled via showLeftPane\(\), the input box will not be visible. The default value for the **showLeftPaneInputBox** property is **false**.

|Name|Type|Description|
|----|----|-----------|
|b|Boolean|If **true**, show the left pane input box.|
|strDefaultValue|String|The default value to display in the input box.|

|Type|Description|
|----|-----------|
|void| |

```
glideTimeline.showLeftPaneInputBox(true, 'Add a new task ...');
    
```

## GlideTimeline - showSummaryPane\(Boolean b\)

Specifies whether or not to show the summary pane at the bottom of the timeline. The default value for the showSummaryPane property is **true**.

The default value for the showSummaryPane property is **true**.

|Name|Type|Description|
|----|----|-----------|
|b|Boolean|If **true**, the timeline includes the summary pane; otherwise, the summary pane is not displayed.|

|Type|Description|
|----|-----------|
|void| |

```
glideTimeline.showSummaryPane(false);
```

## GlideTimeline - showTimelineText\(Boolean b\)

Specifies whether or not to show the timeline text underneath each Timeline Span in the primary timeline pane. The default value for the showTimelineText property is **false**.

The default value for the showTimelineText property is **false**.

|Name|Type|Description|
|----|----|-----------|
|b|Boolean|If **true**, displays descriptive text underneath each Timeline Span; otherwise, no text is displayed underneath each Timeline Span.|

|Type|Description|
|----|-----------|
|void| |

```
glideTimeline.showTimelineText(true);
```

## GlideTimeline - snapVertScrollingIntoRows\(Boolean b\)

Specifies whether or not the vertical movement of timeline span objects \(if appropriately registered to perform this event\) should snap adjust into the closest row. By default this value is enabled.

By default this value is enabled.

|Name|Type|Description|
|----|----|-----------|
|b|Boolean|If **true**, snaps vertical movement of timeline span objects into rows; otherwise, items move exactly with respect to the mouse.|

|Type|Description|
|----|-----------|
|void| |

```
glideTimeline.snapVertScrollingIntoRows(false);
```

## GlideTimeline - sortByLeftLabelText\(Boolean b\)

Specifies whether or not to group items by their left label text. The default value for the **sortByLeftLabelText** property is **false**.

The default value for the **sortByLeftLabelText** property is **false**.

|Name|Type|Description|
|----|----|-----------|
|b|Boolean|If **true**, sort Timeline Items alphabetically by the text specified in each item's left label.|

|Type|Description|
|----|-----------|
|void| |

```
glideTimeline.sortByLeftLabelText(true);
```

## GlideTimeline - sortByStartDate\(Boolean b\)

Specifies whether or not to sort the list of Timeline Items returned by the earliest start date of an item's Timeline Span objects. If groupByParent\(\) is set **true**, items are sorted after grouping has occurred. The default value for the **sortByStartDate** property is **false**.

If groupByParent\(\) is set **true**, items are sorted after grouping has occurred. The default value for the **sortByStartDate** property is **false**.

|Name|Type|Description|
|----|----|-----------|
|b|Boolean|If **true**, sort Timeline Items chronologically starting with their earliest start date.|

|Type|Description|
|----|-----------|
|void| |

```
glideTimeline.sortByStartDate(true);
```

## GlideTimeline - sortByTimelineLabelText\(Boolean b\)

Specifies whether or not to sort the list of Timeline Items returned in alphabetical order according to the text that was specified to show in the Timeline Pane.

**Note:** This sort order still applies even if the timeline text has been set **false** via the showTimelineText\(\) method. Additionally, if groupByParent\(\) is set **true**, items will be sorted appropriately after grouping has occurred.

The default value for the **sortByTimelineLabelText** property is **false**.

|Name|Type|Description|
|----|----|-----------|
|b|Boolean|If true, sorts Timeline Items alphabetically by the text specified in each item's timeline span text.|

|Type|Description|
|----|-----------|
|void| |

```
glideTimeline.sortByTimelineLabelText(true);
```

