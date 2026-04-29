---
title: GlideTimelineItem - Global
description: The GlideTimelineItem API extends the abstract ScheduleItem class to define additional properties that are specific to the time line.Create a "dummy" GlideTimelineItem object.Constructor that sets the required table and sys\_id properties.Creates a new TimelineSpan object associated with the current instance object.Creates a new TimelineSpan object associated with the current instance object using the specified table and sys\_id.Returns a string specifying the name of the image file associated with the current GlideTimelineItem.Indicates whether or not the current instance object should be allowed as a "drop zone" when moving timeline elements vertically.Returns the text to be displayed in the left pane \(if enabled\).Returns the unique sysId of the current GlideTimelineItem's parent object.Returns all the TimelineSpan objects associated with the current instance in an ArrayList.Indicates if the left pane text is set to display using a bold style.Sets the name of the image file \(including it's path\) to use as the icon for the item in the left pane.Sets whether or not the current instance object can be clicked and dragged into another GlideTimelineItem.Specifies the text to display in the left pane for this item.Sets the parent of the current GlideTimelineItem.Specifies whether or not to bold the text style of the item in the left pane.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideTimelineItem- Global

The GlideTimelineItem API extends the abstract ScheduleItem class to define additional properties that are specific to the time line.

A time line item is essentially any item that displays in a singular row across the time line. A GlideTimelineItem has zero or more associated spans \(TimelineSpan objects\).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideTimelineItem - GlideTimelineItem\(String tableName\)

Create a "dummy" GlideTimelineItem object.

This is useful for creating rows that do not allow any YMoving into; however, contain nested children \(e.g. The top-level "Users" row in the Group Resource Timeline\). The **sys\_id**needs to be unique for DOM level functions to parse correctly. By default this object will not be "droppable" because a table name was not specified.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|The name of the table associated with current object.|

|Type|Description|
|----|-----------|
|void| |

## GlideTimelineItem - GlideTimelineItem\(String tableName, String sys\_id\)

Constructor that sets the required table and **sys\_id**properties.

The rest of this object's properties should be set by the caller. By default, this object instance is "droppable" since a table name is specified.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|The name of the table associated with current object.|
|sys\_id|String|The sys ID for the object.|

|Type|Description|
|----|-----------|
|void| |

## GlideTimelineItem - createTimelineSpan\(String tableName\)

Creates a new TimelineSpan object associated with the current instance object.

If no other TimelineSpan objects exist, the newly created object will share the same **sys\_id**as current instance object. Otherwise, a randomly generated GUID will be used.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|The name of the table associated with current object.|

|Type|Description|
|----|-----------|
|Object|The newly-created span object instance.|

## GlideTimelineItem - createTimelineSpan\(String tableName, String sys\_id\)

Creates a new TimelineSpan object associated with the current instance object using the specified table and sys\_id.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Name of the table associated with current object|
|sys\_id|String|Sys\_id for the object.|

|Type|Description|
|----|-----------|
|Object|Newly-created span object instance.|

The following example shows how to use createTimelineSpan\(\) to create a new TimelineSpan object.

```
var project_id="741cc7491b6f1c5043de32231b4bcbc5"; // Project ID 
var grUser = new GlideRecord('user_resource');
grUser.addQuery('planned_task', project_id);
grUser.setQueryReferences(true);
grUser.orderBy('user.name', 'DESC');
grUser.query();
while (grUser.next()) {
  var item = new GlideTimelineItem(grUser.getTableName(), grUser.user);
  /* Specify the text to display in the left pane for this item. */
  item.setLeftLabelText(grUser.user.name); 
  /* Set the name of the image file (including it's path) */
  item.setImage('../images/icons/user.gifx'); 
  /* Specify whether or not to bold the text style of the item in the left pane. */
  item.setTextBold(true); 
  /* Set whether or not the current instance object can be clicked and dragged into another GlideTimelineItem */
  item.setIsDraggable(true);
  /* Create a new TimelineSpan object associated with the current instance object using the specified table and sys_id. */ 
  item.createTimelineSpan(grUser.getTableName(), grUser.getUniqueValue());
}
```

## GlideTimelineItem - getImage\( \)

Returns a string specifying the name of the image file associated with the current GlideTimelineItem.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|The name of the image file associated with the current GlideTimelineItem. If no image is associated with the current item, an empty string \(""\) is returned.|

## GlideTimelineItem - getIsDroppable\( \)

Indicates whether or not the current instance object should be allowed as a "drop zone" when moving timeline elements vertically.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|Boolean|True if droppable; false otherwise.|

## GlideTimelineItem - getLeftLabelText\( \)

Returns the text to be displayed in the left pane \(if enabled\).

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|The value of the text to be displayed in the left pane.|

## GlideTimelineItem - getParent\( \)

Returns the unique **sysId** of the current GlideTimelineItem's parent object.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|The unique sysId of the current GlideTimelineItem's parent object. If the parent does not exist, this will return an empty string \(""\).|

## GlideTimelineItem - getTimelineSpans\( \)

Returns all the TimelineSpan objects associated with the current instance in an ArrayList.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|Object Array|The list of TimelineSpan objects associated with the current instance.|

## GlideTimelineItem - isTextBold\( \)

Indicates if the left pane text is set to display using a bold style.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_mmb_2tm_zt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the text should be bold.Possible values:

-   true: Text should be bold.
-   false: Text should not be bold.

</td></tr></tbody>
</table>The following example checks if an incident's state is "New" and sets the item text to bold.

```
var NewIncidentTimelineScriptInclude = Class.create();
NewIncidentTimelineScriptInclude.prototype = Object.extendsObject(AbstractTimelineSchedulePage, {

  getItems: function() {
    // Specify the page title 
    this.setPageTitle('New Incident Timeline');

    var groupNew = new GlideTimelineItem('new');
    groupNew.setLeftLabelText('New Incidents');

    groupNew.setImage('../images/icons/all.gifx');
    this.add(groupNew);

    // Get all the new incidents and add them to a new label 
    var grIncident = new GlideRecord('incident');
    grIncident.query();
    while (grIncident.next()) {
      // Loop through all and capture new incidents 
      if (grIncident.incident_state != '1') continue;

      // Create the item and the span item. 
      var item = new GlideTimelineItem(grIncident.getTableName(), grIncident.sys_id);
      var span = item.createTimelineSpan(grIncident.getTableName(), grIncident.sys_id);

      if (grIncident.incident_state == '1') { // New
        item.setParent(groupNew.getSysId());
        // Check and set bold text
          item.setTextBold(item.isTextBold() ? false : true);
        } 
      item.setImage('../images/icons/open.gifx');
      span.setTimeSpan(grIncident.getElement('opened_at').getGlideObject().getNumericValue(),
      grIncident.getElement('opened_at').getGlideObject().getNumericValue());

      // Show different colors based upon the priorities only for new incidents 
      switch (grIncident.getElement('priority').toString()) {
        case '1':
          span.setPointIconClass('red_circle');
          break;
        case '2':
          span.setPointIconClass('red_square');
          break;
        case '3':
          span.setPointIconClass('blue_circle');
          break;
        case '4':
          span.setPointIconClass('blue_square');
          break;
        case '5':
          span.setPointIconClass('sepia_circle');
          break;

          default: // Otherwise, the default point icon class will be used (Milestone)
      }

      // Common item properties 
      item.setLeftLabelText(grIncident.short_description);

      // Common span properties
      span.setSpanText(grIncident.short_description);
      span.setSpanColor('blue');
      span.setTooltip('<strong>' + GlideStringUtil.escapeHTML(grIncident.short_description) +
        '</strong><br>' + grIncident.number);
      this.add(item);
    }
  }

});
```

## GlideTimelineItem - setImage\(String strImageName\)

Sets the name of the image file \(including it's path\) to use as the icon for the item in the left pane.

|Name|Type|Description|
|----|----|-----------|
|strImageName|String|Name of the image, including its path.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to use setImage\(\) to define the image that should appear for the icon in the left pane.

```
var project_id="741cc7491b6f1c5043de32231b4bcbc5"; // Project ID 
var grUser = new GlideRecord('user_resource');
grUser.addQuery('planned_task', project_id);
grUser.setQueryReferences(true);
grUser.orderBy('user.name', 'DESC');
grUser.query();
while (grUser.next()) {
  var item = new GlideTimelineItem(grUser.getTableName(), grUser.user);
  /* Specify the text to display in the left pane for this item. */
  item.setLeftLabelText(grUser.user.name); 
  /* Set the name of the image file (including it's path) */
  item.setImage('../images/icons/user.gifx'); 
  /* Specify whether or not to bold the text style of the item in the left pane. */
  item.setTextBold(true); 
  /* Set whether or not the current instance object can be clicked and dragged into another GlideTimelineItem */
  item.setIsDraggable(true); 
}
```

## GlideTimelineItem - setIsDraggable\(Boolean b\)

Sets whether or not the current instance object can be clicked and dragged into another GlideTimelineItem.

<table id="table_pmb_2tm_zt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

b

</td><td>

Boolean

</td><td>

Flag that indicates whether the item can be moved using click and drag. Valid values:

-   true: Item can be moved using click and drag.
-   false: Item cannot be moved using click and drag.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

The following example shows how to use setIsDraggable\(\) to enable the current object to be dragged into another GlideTimelineItem.

```
var project_id="741cc7491b6f1c5043de32231b4bcbc5"; // Project ID 
var grUser = new GlideRecord('user_resource');
grUser.addQuery('planned_task', project_id);
grUser.setQueryReferences(true);
grUser.orderBy('user.name', 'DESC');
grUser.query();
while (grUser.next()) {
  var item = new GlideTimelineItem(grUser.getTableName(), grUser.user);
  /* Specify the text to display in the left pane for this item. */
  item.setLeftLabelText(grUser.user.name); 
  /* Set the name of the image file (including it's path) */
  item.setImage('../images/icons/user.gifx'); 
  /* Specify whether or not to bold the text style of the item in the left pane. */
  item.setTextBold(true); 
  /* Set whether or not the current instance object can be clicked and dragged into another GlideTimelineItem */
  item.setIsDraggable(true); 
}
```

## GlideTimelineItem - setLeftLabelText\(String strText\)

Specifies the text to display in the left pane for this item.

|Name|Type|Description|
|----|----|-----------|
|strText|String|Text to display in the left pane for this item.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to use setLeftLabelText\(\) to set the text in the left pane.

```
var project_id="741cc7491b6f1c5043de32231b4bcbc5"; // Project ID 
var grUser = new GlideRecord('user_resource');
grUser.addQuery('planned_task', project_id);
grUser.setQueryReferences(true);
grUser.orderBy('user.name', 'DESC');
grUser.query();
while (grUser.next()) {
  var item = new GlideTimelineItem(grUser.getTableName(), grUser.user);
  /* Specify the text to display in the left pane for this item. */
  item.setLeftLabelText(grUser.user.name); 
  /* Set the name of the image file (including it's path) */
  item.setImage('../images/icons/user.gifx'); 
  /* Specify whether or not to bold the text style of the item in the left pane. */
  item.setTextBold(true); 
  /* Set whether or not the current instance object can be clicked and dragged into another GlideTimelineItem */
  item.setIsDraggable(true); 
}
```

## GlideTimelineItem - setParent\(String sysId\)

Sets the parent of the current GlideTimelineItem.

|Name|Type|Description|
|----|----|-----------|
|sysId|String|The sysID of the GlideTimelineItem that should become the parent of the current GlideTimelineItem.|

|Type|Description|
|----|-----------|
|void| |

## GlideTimelineItem - setTextBold\(Boolean b\)

Specifies whether or not to bold the text style of the item in the left pane.

<table id="table_obb_lvm_zt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

b

</td><td>

Boolean

</td><td>

Flag that indicates whether the text in left pane should be bold.Valid values:

-   true: Text should be bold.
-   false: Text should not be bold.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

The following example shows how to set the text in the left pane to bold.

```
var project_id="741cc7491b6f1c5043de32231b4bcbc5"; // Project ID 
var grUser = new GlideRecord('user_resource');
grUser.addQuery('planned_task', project_id);
grUser.setQueryReferences(true);
grUser.orderBy('user.name', 'DESC');
grUser.query();
while (grUser.next()) {
  var item = new GlideTimelineItem(grUser.getTableName(), grUser.user);
  /* Specify the text to display in the left pane for this item. */
  item.setLeftLabelText(grUser.user.name); 
  /* Set the name of the image file (including it's path) */
  item.setImage('../images/icons/user.gifx'); 
  /* Specify whether or not to bold the text style of the item in the left pane. */
  item.setTextBold(true); 
  /* Set whether or not the current instance object can be clicked and dragged into another GlideTimelineItem */
  item.setIsDraggable(true); 
}
```

