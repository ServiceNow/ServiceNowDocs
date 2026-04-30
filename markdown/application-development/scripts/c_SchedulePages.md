---
title: Schedule Pages
description: A schedule page is a record that contains a collection of scripts that allow for custom generation of a calendar or timeline display.To access schedule pages, navigate to System Scheduler Schedules Schedule Pages .A Timeline Schedule Page is a specific record that contains configuration information for displaying time based points and spans in a "timeline" like fashion.The following example demonstrates how to create a timeline schedule page with corresponding script include utilizing a majority of the API described above.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Server-side scripting, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Schedule Pages

A schedule page is a record that contains a collection of scripts that allow for custom generation of a calendar or timeline display.

Creation of timeline schedule pages requires understanding of the page/event flow and the ability to write client and server side JavaScript.

**Parent Topic:**[Server-side scripting](../../server-scripting/concept/c_ServerScripting.md)

## Schedule pages form

To access schedule pages, navigate to **System Scheduler** &gt; **Schedules** &gt; **Schedule Pages**.

The form provides the following fields, depending upon the View Type selected:

<table id="table_i4p_34j_lp"><thead><tr><th>

Field

</th><th>

Field Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

String

</td><td>

General name that is used to identity the current schedule page.

</td></tr><tr><td>

Schedule type

</td><td>

String

</td><td>

The schedule type is a string that is used to uniquely identity the schedule page via the "sysparm\_page\_schedule\_type" URI parameter. For example, a schedule page could be accessed as follows: `/show_schedule_page.do?sysparm_type=gantt_chart&sysparm_timeline_task_id=d530bf907f0000015ce594fd929cf6a4`

 Alternatively, the schedule page can also be accessed by setting the "**sysparm\_page\_sys\_id**" URI parameter to that of the unique 32 character hexadecimal system identifier of the schedule page.

</td></tr><tr><td>

View Type

</td><td>

Choice

</td><td>

Each view type displays different field combinations. There are two options available:-   Calendars
-   Timelines

</td></tr><tr><td>

Description

</td><td>

String

</td><td>

General description that provides additional information about the current schedule page. This field is not necessary.

</td></tr><tr><td>

Init funciton name

</td><td>

String

</td><td>

**Note:** This functionality is only used by Calendar type schedule pages.

The init function name specifies the name of the JavaScript function to call inside the Client script function for calendar type schedule pages.

</td></tr><tr><td>

HTML

</td><td>

String

</td><td>

**Note:** This functionality is only used by Calendar type schedule pages.

The HTML field is a scriptable section that is parsed by Jelly and injected into the display page prior to the rest of the calendar. It can be used to pass in variables from the server and define extra fields are necessary.

</td></tr><tr><td>

Client script

</td><td>

String

</td><td>

The client script is a scriptable section that allows for configuring options of the schedule page display. The API is different depending on the schedule page view type and is discussed below.

</td></tr><tr><td>

Server AJAX processor

</td><td>

String

</td><td>

**Note:** This functionality is only used by Calendar type schedule pages.

The Server AJAX processor is specific to calendar type schedule pages that is used to return a set of schedule items and spans to be displayed.

</td></tr></tbody>
</table>## Timeline schedule pages

A Timeline Schedule Page is a specific record that contains configuration information for displaying time based points and spans in a "timeline" like fashion.

The timeline schedule page references a script include that extends from AbstractTimelineSchedulePage to perform dynamic modification to the timeline based on different events and conditions. Both the schedule page and the script include for timeline generation allow for extreme customization and their corresponding application programming interface \(API\) is documented below.

The following diagram shows the series of events that occur when a timeline schedule page is accessed. Once the timeline has been loaded, all subsequent events, such as events resulting from timeline interaction \(e.g. moving a timeline span\), follow the same logic flow shown in the gray event box.

![](../image/TimelineFlow.png "Timeline Flow")

### Applications that use schedule pages to generate time lines

-   Project Management
-   Maintenance Schedules
-   Group On-Call Rotation
-   Field Service Management

## Timeline schedule page example

The following example demonstrates how to create a timeline schedule page with corresponding script include utilizing a majority of the API described above.

For this example we are going to create an Incident Summary Timeline for a project support manager to visualize all of the new incidents. All new incidents should be displayed as single points where the priority of the incident is distinguished by a different point icon. Additionally, all closed incidents should be displayed on the timeline in a separate group that shows the duration of the incident before it was closed. Since the Project Manager wants to be able to easily close new items that are resolved without using any form lists, we will handle the vertical move event allowing the new incidents to be dragged into the closed incident group or items within.

### Schedule Page

Create a new schedule page with the following properties:

-   **Name**: Hardware Incidents
-   **Schedule type**: incident\_timeline
-   **View Type**: Timeline
-   **Client Script**:

```
// Set our page configuration
glideTimeline.setReadOnly(false);
glideTimeline.showLeftPane(true);
glideTimeline.showLeftPaneAsTree(true);
glideTimeline.showTimelineText(true);
glideTimeline.showDependencyLines(false);
glideTimeline.groupByParent(true);
glideTimeline.setDefaultPointIconClass('milestone');
 
// We will define what items to display and provide a custom event handler for moving new items to the closed state
glideTimeline.registerEvent('getItems', 'IncidentTimelineScriptInclude');
glideTimeline.registerEvent('elementMoveY', 'IncidentTimelineScriptInclude');
```

### Script Include

Now that the schedule page has been created we need to generate a matching script include for the events that were registered. Create a new script include with the following properties:

-   **Name**: IncidentTimelineScriptInclude
-   **Active**: Checked
-   **Glide AJAX enabled**: Checked
-   **Script**:

```
// Class Imports
 
var IncidentTimelineScriptInclude = Class.create();
IncidentTimelineScriptInclude.prototype = Object.extendsObject(AbstractTimelineSchedulePage, {
 
  /////////////////////// // GET_ITEMS ///////////////////////////////////////
  getItems:function() { 
    // Specify the page title 
    this.setPageTitle('My Custom Incident Summary Timeline');
 
    var groupNew = new GlideTimelineItem('new');
    groupNew.setLeftLabelText('New Incidents');
    groupNew.setImage('../images/icons/all.gifx');
    groupNew.setTextBold(true);
    this.add(groupNew);
 
    var groupClosed = new GlideTimelineItem('closed');
    groupClosed.setLeftLabelText('Closed Incidents');
    groupClosed.setImage('../images/icons/all.gifx');
    groupClosed.setTextBold(true);
    groupClosed.setIsDroppable(true);
 
    // This allows us to drag an open incident onto the closed group row. 
    this.add(groupClosed);
 
    // Get all the incidents and let's add only the new/closed ones appropriately 
    var now_GR = new GlideRecord('incident');
    gr.query(); 
    while(gr.next()) { 
       // Only loop through new/closed incidents 
       if(gr.incident_state != '1' && gr.incident_state != '7') continue;
 
       // Ok, we have a new/closed incident. Create the item and the span first. 
       var item = new GlideTimelineItem(gr.getTableName(), gr.sys_id); 
       var span = item.createTimelineSpan(gr.getTableName(), gr.sys_id);
 
       // Specific properties for a new incident 
       if(gr.incident_state == '1') { // New 
         item.setParent(groupNew.getSysId()); 
         item.setImage('../images/icons/open.gifx');
         span.setTimeSpan(gr.getElement('opened_at').getGlideObject().getNumericValue(),
                          gr.getElement('opened_at').getGlideObject().getNumericValue());
 
         // We will show different colors based upon the priorities only for new incidents 
         switch(gr.getElement('priority').toString()) {
           case '1': span.setPointIconClass('red_circle'); break; 
           case '2': span.setPointIconClass('red_square'); break; 
           case '3': span.setPointIconClass('blue_circle'); break; 
           case '4': span.setPointIconClass('blue_square'); break; 
           case '5': span.setPointIconClass('sepia_circle'); break; 
           default: // Otherwise, the default point icon class will be used (Milestone)
          }
         }
        // Specific properties for a closed incident 
        else if(gr.incident_state == '7') { 
          item.setParent(groupClosed.getSysId()); 
          item.setImage('../images/icons/closed.gifx');
          span.setTimeSpan(gr.getElement('opened_at').getGlideObject().getNumericValue(),
                           gr.getElement('closed_at').getGlideObject().getNumericValue()); }
 
        // Common item properties 
        item.setLeftLabelText(gr.short_description);
 
        // Common span properties
        span.setSpanText(gr.short_description);
        span.setTooltip('<strong>' + GlideStringUtil.escapeHTML(gr.short_description) + '</strong><br>' + gr.number);
        span.setAllowXMove(false);
        span.setAllowYMove(gr.canWrite() ? true:false);
        span.setAllowYMovePredecessor(false);
        span.setAllowXDragLeft(false);
        span.setAllowXDragRight(false);
 
        // Now we add the actual item 
        this.add(item); 
        } } ,
 
 
   //////////////////////// // ELEMENT_MOVE_Y /////////////////////////////////////////////////////////////
 
   /**
   * This is one of the AbstractTimelineSchedulePage event handler methods that corresponds to a vertical
   * move. The arguments for this function are defined in the API section of the event handler methods.
   */
  elementMoveY: function(spanId, itemId, newItemId) {
 
    // Get information about the current incident 
    var now_GR = new GlideRecord('incident');
    gr.addQuery('sys_id', spanId);
    gr.query(); 
    if(!gr.next()) 
      return this.setStatusError('Error', 'Unable to lookup the current incident.');
 
    // Only allow the new incidents to have their state adjusted. 
    if(gr.incident_state != '1') 
      return this.setStatusError('Error','Only new incidents can have their state adjusted.');
 
    // Get information about the dropped GlideTimelineItem. If it was dropped in an item on the "New Incidents" 
    // group let's do nothing. If it was dropped in the "Closed Incidents" then let's adjust the state automatically. 
    var grDropped = new GlideRecord('incident');
    grDropped.addQuery('sys_id', newItemId );
    grDropped.query(); 
    if(!grDropped.next() || grDropped.incident_state == '7') { 
       // This means the dropped item was either the 'Closed Incidents' group (which has no record or sys_id) or an 
       // existing incident that is closed. The 'New Incidents' also has no sys_id; however, the default behavior for 
       // items without a sysId is to be non-droppable. This is why we explicitly denoted the 'Closed Incidents' to  
       // be marked as "droppable".
 
       // Return a dialog prompt 
       this.setStatusPrompt('Confirm', 'Are you sure you want to close: ' + 
              '<div style="margin:10px 0 10px 14px;padding:4px;background-color:#EBEBEB;"><strong>' +
               GlideStringUtil.escapeHTML(gr.short_description) + 
               '</strong><br/><div class="font_smaller">' + now_GR. number + '</div></div>', 
               'this._elementMoveYHandler_DoClose', // This function is for when the OK button is clicked. 
               'this._elementMoveYHandler_DoNothing', // This function is for when the Cancel button is clicked. 
               'this._elementMoveYHandler_DoNothing'); // This function is for when the Close button is clicked.
       } } ,
 
  _elementMoveYHandler_DoClose: function(spanId, itemId, newItemId) { 
    // Notice that this function takes the same function arguments as the original function for which it  
    // is a custom event handler for.
 
    // Update the database record from 'New' to 'Closed'. 
    var now_GR = new GlideRecord('incident');
    gr.addQuery('sys_id', spanId);
    gr.query();
    gr.next();
    gr.setValue('incident_state', '7');
    gr.update();
 
    // This will re-render the timeline showing the updated item in the closed group. 
    this.setDoReRenderTimeline(true);
 
    // Let's show a success message 
    this.setStatusSuccess('Success', '<strong>' + gr.short_description + '</strong> was successfully closed.'); } ,
 
  // Since the user clicked cancel or close we simply do nothing.
  _elementMoveYHandler_DoNothing: function(spanId, itemId, newItemId) { }
 
 });
```

### Screenshots / Results

1.  Navigate to:

    `http://[YOURINSTANCE]:8080/show_schedule_page.do?sysparm_page_schedule_type=incident_timeline`

    Notice the bold text is the value of the schedule page **Schedule type** field.

2.  The page displays a timeline as specified by the schedule page and script include created. A link to this page can be created and placed as a module or UI action as necessary.

    ![](../image/TimelineExampleIncidentPreview.png "Timeline Example Incident Preview")

3.  Attempting to move a closed incident anywhere displays the expected error message.

    ![](../image/TimelineExampleErrorMoving.png "Timeline Example Error Moving")

4.  Moving the incident: I need more memory displays the following confirmation box.

    ![](../image/TimelineExampleConfirmClose.png "Timeline Example Confirm Close")

5.  Clicking the **Cancel** button closes the overlay. Clicking the **OK** button actually updates the incident\_state of the record and then displays the following success box.

    ![](../image/TimelineExampleCloseSuccess.png "Timeline Example Close Success")

6.  After clicking **OK**, it is clear the incident is now listed in the **Closed Incidents** group.

    ![Timeline of an example incident](../image/TimelineExampleIncidentUpdated.png "Timeline Example Incident Updated")


