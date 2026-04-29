---
title: AbstractTimelineSchedulePage - Global
description: The AbstractTimelineSchedulePage script include is a helper class to facilitate working with the data displayed on timelines.Adds a TimelineItem object that will be returned to the client and appropriately displayed on the timeline.Adds a horizontal frame separator into the list of timeline items. All future items added via add\(\) will be added into the subsequent timeline frame.Event handler for when a timeline span moves horizontally.Event handler for when a timeline span moves both horizontally and vertically.Event handler for when a timeline span moves vertically.Event handler for when a timeline relationship has been created between two spans.Event handler for when a timeline span's end date was modified.Event handler for when a timeline span's start date was modified.Event handler for returning schedule items to display on the timeline.Event handler for when a string was typed into the left pane input box.Event handler for when a timeline row item was moved and dragged into another row item.Specifies whether or not to re-render all of the timeline items using the getItems\(\) function.Specifies the text to display as the title of the timeline.Sets the current event request to an error status with a specified title and message to display in phase two of the GlideTimeline event processing.Sets the current event request to a prompt error status with a specified title and message to display in a confirmation dialog box during phase two of the GlideTimeline event processing. The confirmation box displays an OK and Cancel button that each generate new events that will call the functions specified the parameter arguments. The custom defined functions for OK, Cancel, and Close receive the same parameter arguments as those for the current event.Sets the current event request to a success status with a specified title and message to display in phase two of the GlideTimeline event processing.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# AbstractTimelineSchedulePage- Global

The AbstractTimelineSchedulePage script include is a helper class to facilitate working with the data displayed on timelines.

Processing the data displayed within a timeline starts by executing the corresponding function of the specified script include. Like other script includes, the language syntax is JavaScript and follows the default security constraints of this type of resource. However, because the different types of display options are complex, a helper class was created. To display a timeline, extend the AbstractTimelineSchedulePage class and pair it with it's corresponding schedule page. At a minimum, extending classes should override the getItems\(\) method, as this is the primary event handler for returning items to be displayed on the client.

The client processes the data that AbstractTimelineSchedulePage returns in two phases. The first phase makes the actual updates to the timeline. Immediately after, if configured, the second phase displays a success message box, error message box, or dialog message prompt. In phase one, the available options for manipulating data include:

-   Do Not Update Any Items: This is the default behavior. Do not perform any of the remaining steps in phase one.
-   Update With Specific Items: This is done using: add\(\).
-   Render The Timeline Using the getItems\(\) Function: This is done using: `setDoReRenderTimeline(true)`.

**Note:** If both TimelineItems are returned and **setDoReRenderTimeline** is set to **true**, the system ignores the **setDoReRenderTimeline** property and explicitly shows only the TimelineItems that were added by theadd\(\) function.

The available options in phase two include:

-   Do Not Display Any Message Boxes: This is the default behavior.
-   Display a Success Dialog Box: This is done using: setStatusSuccess\(\).
-   Display an Error Dialog Box: This is done using: setStatusError\(\).
-   Display a Dialog Confirm Box: This is done using: setStatusPrompt\(\).

**Note:**

A script include class that extends AbstractTimelineSchedulePage automatically receives all URI parameters from the original URL whose prefix begins with `sysparm_timeline_`. To access the values of these, use:`this.getParameter("sysparm_timeline_VARIABLE");` inside your extended class.

This is useful if you need to display a schedule page from a dynamic element, such as from a context menu from a list. By passing in dynamic data via the URL the schedule page auto-includes these parameters inside the Ajax calls and therefore will be accessible inside the AbstractTimelineSchedulePage script include.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## AbstractTimelineSchedulePage - add\(Object ObjTimeline\)

Adds a TimelineItem object that will be returned to the client and appropriately displayed on the timeline.

|Name|Type|Description|
|----|----|-----------|
|ObjTimeline|Object|The TimelineItem object to add to the timeline.|

|Type|Description|
|----|-----------|
|void| |

## AbstractTimelineSchedulePage - addSeparator\(\)

Adds a horizontal frame separator into the list of timeline items. All future items added via add\(\) will be added into the subsequent timeline frame.

All future items added using the add\(\) method are added into the subsequent timeline frame.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

The following code example shows how to call this method.

```
// Inside of a script include that extends AbstractTimelineSchedulePage
      this.addSeparator();
    
```

## AbstractTimelineSchedulePage - elementMoveX\(String spanSysId, String newStartDateTimeMs\)

Event handler for when a timeline span moves horizontally.

|Name|Type|Description|
|----|----|-----------|
|spanSysId|String|The sys ID of the current span being adjusted.|
|newStartDateTimeMs|String|The new start time of the span in milliseconds. Make sure to parse the string using parseInt\(\) before performing any numerical comparisons.|

|Type|Description|
|----|-----------|
|void| |

## AbstractTimelineSchedulePage - elementMoveXY\(String spanSysId, String itemSysId, String itemSysId, String newItemSysId, String newStartDateTimeMs\)

Event handler for when a timeline span moves both horizontally and vertically.

|Name|Type|Description|
|----|----|-----------|
|spanSysId|String|The sys ID of the current span being adjusted.|
|itemSysId|String|The sys ID of the timeline item associated with the current span.|
|newItemSysId|String|The sys ID of the timeline item \(a row\) that the current span was dragged into.|
|newStartDateTimeMs|String|The new start time of the span in milliseconds. Make sure to parse the string using parseInt\(\) before performing any numerical comparisons.|

|Type|Description|
|----|-----------|
|void| |

## AbstractTimelineSchedulePage - elementMoveY\(String spanSysId, String itemSysId, String newItemSysId\)

Event handler for when a timeline span moves vertically.

|Name|Type|Description|
|----|----|-----------|
|spanSysId|String|The sys ID of the current span being adjusted.|
|itemSysId|String|The sys ID of the timeline item associated with the current span.|
|newItemSysId|String|The sys ID of the timeline item \(a row\) that the current span was dragged into.|

|Type|Description|
|----|-----------|
|void| |

## AbstractTimelineSchedulePage - elementSuccessor\(String spanSysId, String newSuccSpanId\)

Event handler for when a timeline relationship has been created between two spans.

|Name|Type|Description|
|----|----|-----------|
|spanSysId|String|The sys ID of the current span which will be a predecessor for the newly created relationship.|
|newSuccSpanId|String|The sys ID of the successor span from the relationship created.|

|Type|Description|
|----|-----------|
|void|ReturnValue|

## AbstractTimelineSchedulePage - elementTimeAdjustEnd\(String spanSysId, String newEndDateTimeMs\)

Event handler for when a timeline span's end date was modified.

|Name|Type|Description|
|----|----|-----------|
|spanSysId|String|The sys ID of the current span that is being adjusted.|
|newEndDateTimeMs|String|The new end time of the span in milliseconds. Make sure to parse the string using parseInt\(\) prior to performing any numerical comparisons.|

|Type|Description|
|----|-----------|
|void| |

## AbstractTimelineSchedulePage - elementTimeAdjustStart\(String spanSysId, String newStartDateTimeMs\)

Event handler for when a timeline span's start date was modified.

|Name|Type|Description|
|----|----|-----------|
|spanSysId|String|The sys ID of the current span that is being adjusted.|
|newStartDateTimeMs|String|The new start time of the span in milliseconds. Make sure to parse the string using parseInt\(\) prior to performing any numerical comparisons.|

|Type|Description|
|----|-----------|
|void| |

## AbstractTimelineSchedulePage - getItems\(\)

Event handler for returning schedule items to display on the timeline.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|void| |

## AbstractTimelineSchedulePage - inputBox\(String strInputText\)

Event handler for when a string was typed into the left pane input box.

|Name|Type|Description|
|----|----|-----------|
|strInputText|String|The text that was entered in the input box in the left pane.|

|Type|Description|
|----|-----------|
|void| |

## AbstractTimelineSchedulePage - itemMove\(String itemSysId, String newItemSysId\)

Event handler for when a timeline row item was moved and dragged into another row item.

|Name|Type|Description|
|----|----|-----------|
|itemSysId|String|The sys ID of the timeline item associated with the current span.|
|newItemSysId|String|The sys ID of the timeline item \(a row\) that the current span was dragged into.|

|Type|Description|
|----|-----------|
|void| |

## AbstractTimelineSchedulePage - setDoReRenderTimeline\(Boolean b\)

Specifies whether or not to re-render all of the timeline items using the getItems\(\) function.

|Name|Type|Description|
|----|----|-----------|
|b|Boolean|If **true**, re-render the timeline by making a new event call to the server's getItems\(\) handler.|

|Type|Description|
|----|-----------|
|void| |

## AbstractTimelineSchedulePage - setPageTitle\(String strTitle\)

Specifies the text to display as the title of the timeline.

The page title can be set \(and updated\) from any interactive event; however, is recommended to be set during thegetItems\(\) event.

|Name|Type|Description|
|----|----|-----------|
|strTitle|String|The text to be displayed on the timeline title.|

|Type|Description|
|----|-----------|
|void| |

## AbstractTimelineSchedulePage - setStatusError\(String strTitle, String strMessage\)

Sets the current event request to an error status with a specified title and message to display in phase two of the GlideTimeline event processing.

|Name|Type|Description|
|----|----|-----------|
|strTitle|String|The text to be displayed in the dialog box title.|
|strMessage|String|The text to be displayed within the dialog box. The text can contain HTML formatting.|

|Type|Description|
|----|-----------|
|void| |

## AbstractTimelineSchedulePage - setStatusPrompt\(String strTitle, String strOkFunction, String strCancelFunction, String strCloseFunction\)

Sets the current event request to a prompt error status with a specified title and message to display in a confirmation dialog box during phase two of the GlideTimeline event processing. The confirmation box displays an **OK** and **Cancel** button that each generate new events that will call the functions specified the parameter arguments. The custom defined functions for **OK**, **Cancel**, and **Close** receive the same parameter arguments as those for the current event.

The confirmation box displays an **OK** and **Cancel** button that each generate new events that will call the functions specified the parameter arguments.

**Note:** The custom defined functions for **OK**, **Cancel**, and **Close** receive the same parameter arguments as those for the current event.

|Name|Type|Description|
|----|----|-----------|
|strTitle|String|The text to display in the dialog box. The text can contain HTML formatting.|
|strOkFunction|String|The function to call in the current script include class if the users clicks the **OK** button.|
|strCancelFunction|String|The function to call in the current script include class if the user clicks the **Cancel** button.|
|strCloseFunction|String|The function to call in the current script include class if the user clicks the **Close** button.|

|Type|Description|
|----|-----------|
|void| |

```
var MyTimelineScriptIncludeClass = Class.create();
      MyTimelineScriptIncludeClass.prototype = Object.extendsObject(AbstractTimelineSchedulePage, {
      
      getItems: function() {
      //...
      },
      
      elementTimeAdjustEnd: function(spanSysId, newEndDateTimeMs) {
      // Display a status prompt dialog box
      this.setStatusPrompt('Confirm Action', 'Are you sure you want to do that?',
      'this._myOkHandlerFunction',  
      'this._myCancelHandlerFunction',
      'this._myCloseHandlerFunction');
      },
      
      _myOkHandlerFunction: function(spanSysId, newEndDateTimeMs) { // ... },
      
      _myCancelHandlerFunction: function(spanSysId, newEndDateTimeMs) { // ... },
      
      _myCloseHandlerFunction: function(spanSysId, newEndDateTimeMs) { // ... }
      };
    
```

## AbstractTimelineSchedulePage - setStatusSuccess\(String strTitle, String strMessage\)

Sets the current event request to a success status with a specified title and message to display in phase two of the GlideTimeline event processing.

|Name|Type|Description|
|----|----|-----------|
|strTitle|String|The text to be displayed in the dialog box title.|
|strMessage|String|The text to be displayed within the dialog box. The text can contain HTML formatting.|

|Type|Description|
|----|-----------|
|void| |

