---
title: Field script use cases
description: Common use cases for field customization scripts.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Useful scripts, Scripting, API implementation, API implementation and reference]
---

# Field script use cases

Common use cases for field customization scripts.

**Warning:** The customization described here was developed for use in specific instances, and is not supported by Now Support. This method is provided as-is and should be tested thoroughly before implementation. Post all questions and comments regarding this customization to our community [forum](http://community.service-now.com/).

For more information, see [Server API reference](../../../build/applications/concept/api-server.md).

## Automatically populate a field

The following example shows how to use a client script to auto-fill a **Short Description** based on the selected **Subcategory**.

In this case, if the table has a record with **Subcategory** = Password and **Short Description** = Password Reset. When the user selects the **Subcategory** of **Password** on the Incident form, a client script looks up the matching record and sets **Short Description** equal to Password Reset.

Client script settings:

-   **Type** = onChange
-   **Table name** = incident
-   **Field name** = Subcategory

```
function onChange(control, oldValue, newValue, isLoading){
    if(isLoading){return;}
    var newrec = gel('sys_row');
    //Check if new record
    if (newrec.value == -1) {
        var lookup = new GlideRecord('u_short_desc_lookup');
        lookup.addQuery('u_subcategory', g_form.getValue('subcategory'));
        lookup.query();
        var temp; //temp var - reusable
        if(lookup.next()){
            temp = lookup.u_short_description;
            if(null != temp) {
                //Set the form value from lookup if there is a lookup value
                g_form.setValue('short_description', temp);
            } else {
                g_form.setValue('short_description',"");
                }
          } else {
              //If a lookup record does not exist based on lookup.addQuery
              //Then set to UNDEFINED or NULL depending on type
              g_form.setValue('short_description',"");
              }
     }
}
```

## Disable HTML tags in descriptions

This code disables HTML tags in **Description** and **Short Description** fields by substituting the tags with non-executing versions.

```
doit();
 
function doit(){ 
 var desc = current.description.toString();
 var shdesc = current.short_description.toString();
 if(desc.indexOf('script>')>-1|| shdesc.indexOf('script>')>-1){
   desc = desc.replace(/<script>/g,"(script)");
   current.description = desc.replace(/<\/script>/g,"(\/script)");
   shdesc = shdesc.replace(/<script>/g,"(script)");
   current.short_description = shdesc.replace(/<\/script>/g,"(\/script)");}
}
```

## Eliminate leading and trailing spaces in fields

This example of the script trims trailing and leading spaces in the **FirstName** and **LastName** fields of the sys\_user.

```
doit();
 
function doit(){ 
  var now_GR =new GlideRecord('sys_user');
  gr.query();
  while(gr.next()){
    if((gr.first_name.toString().length!= gr.first_name.toString().trim().length)||(gr.last_name.toString().length!= gr.last_name.toString().trim().length)){
     gr.first_name= gr.first_name.toString().trim();
     gr.last_name= gr.last_name.toString().trim();
     gr.autoSysFields(false);
     gr.update();}}
}
```

## Make a field label flash

The following client script example is for the number field on incident. The label flashes for two seconds.

```
g_form.flash("incident.number","#FFFACD",0);
```

The arguments for the flash method are as follows:

-   **tablename.fieldname**
-   RGB color or acceptable CSS color like "blue" or "tomato"
-   Integer that determines how long the label flashes:
    -   2 for a 1-second flash
    -   0 for a 2-second flash
    -   -2 for a 3-second flash
    -   -4 for a 4-second flash

**Note:** Do not specify this argument if you want the field label colored the specified color.

## Make a field label bold

This client script makes the label of a particular field bold. In this case, the field is the **Short Description** on the **Incident Table**.

```
function onLoad(){
  var l = g_form.getLabel('incident.short_description');
  l.style.fontWeight = 'bold';}
```

## Make fields read-only

This onLoad client script makes the following fields on the Incident \[incident\] table read-only:

-   **Incident state**
-   **Impact**
-   **Urgency**
-   **Priority**
-   **Configuration item**
-   **Assigned to**

The script also removes the magnifying glass for the read-only Reference Fields \(**Configuration item** and **Assigned to**\).

```
function onLoad(){
var incidentState = g_form.getValue('incident_state');
if( incidentState == '6'|| incidentState == '7'){
   g_form.setReadonly('incident_state',true);
   g_form.setReadonly('impact',true);
   g_form.setReadonly('urgency',true);
   g_form.setReadonly('priority',true);
   g_form.setReadonly('cmdb_ci',true);
   g_form.setReadonly('assigned_to',true);}}
```

## Set current date/time in field

You can set date and time values in client scripts and script includes.

-   **Client script**

    You can use the following two lines to set the current date and time in a date/time field. This approach bypasses the problem of getting the value into the proper format and proper time zone.

    ```
    var ajax = new GlideAjax('MyDateTimeAjax');
      ajax.addParam('sysparm_name','nowDateTime');
      ajax.getXML(function(){
        g_form.setValue('put your field name here', ajax.getAnswer());});
    ```

    For more information on running server-side scripts with the client, refer to [GlideAjax](../../ajax/topic/p_AJAX.md#).

-   **System script include**

    ```
    // Be sure the Glide AJAX enabled option is checked
     
    var MyDateTimeAjax = Class.create();
    MyDateTimeAjax.prototype = Object.extendsObject(AbstractAjaxProcessor,{
      nowDateTime:function(){
        return gs.nowDateTime();}});
    ```


## Toggle the timer field by field name

The following client script toggles the timer field based on a particular field name.

```
function toggleTimerByFieldName(fieldName){
 //Step 1: Find the timer object
 //timeObjectName: the timer objects name as it would normally be referenced
 //timeObjectHidden: the hidden input node in the field td
 //timeObjectParent: the parent td node containing the field and it's constituent nodes
 //timeObjectFields: anchor tag with onclick to stop timer
 
 var timeObjectName = fieldName;
 var timeObjectHidden = gel(timeObjectName);
 
 //Step 2: simulate click stop button
 var timeObjectParent;
 var timeObjectFields;
 
 //verify that we got the correct object
 if(timeObjectHidden.type=="hidden"){
 
    //Get Parent td node
    timeObjectParent = timeObjectHidden.parentNode;
 
    //Get input fields
    timeObjectFields = timeObjectParent.getElementsByTagName("input");
 
    //simulate click of stop button
    var timerTestString ="paused";
    var timerImg;
 
    //loop through input objects looking for the pause timer object
    for(var elIt=0; elIt < timeObjectFields.length; elIt++){
      if(timeObjectFields[elIt].id.match(timerTestString)){
        if(timeObjectFields[elIt].value=="false"){
          timeObjectFields[elIt].value="true";
          timerImg = timeObjectParent.getElementsByTagName("img")[0];
          timerImg.src="images/timer_start.gifx";}
      elseif(timeObjectFields[elIt].value=="true"){
          timeObjectFields[elIt].value="false";
          timerImg = timeObjectParent.getElementsByTagName("img")[0];
          timerImg.src="images/timer_stop.gifx";}}}}}
```

## Modify GlideDateTime field value

The following example uses a server-side script to access a **GlideDateTime** field.

The following server-side script example shows how to modify values using the GlideDateTime API. The same concept also applies to the GlideDate object.

```
//You first need a GlideDateTime object
//this can be from instantiating a new object "var gdt = new GlideDateTime()"
//or getting the object from a GlideDateTime field
//getting the field value (for example: var gdt = current.start_date) 
//only returns the string value, not the object
//to get the object use var gdt = current.start_date.getGlideObject();
//now gdt is a GlideDateTime object
var gdt = current.start_date.getGlideObject();
 
//All methods can use negative values to subtract intervals
 
//add 1 hour (60 mins * 60 secs)
gdt.addSecondsLocalTime(3600);
 
//add 1 day
gdt.addDaysLocalTime(1);
 
//subtract 1 day
gdt.addDaysLocalTime(-1);
 
//add 3 weeks
gdt.addWeeksLocalTime(3);
 
//subtract 6 months.
gdt.addMonthsLocalTime(-6);
 
//add 1 year, representing the date and time using the UTC timezone instead of the local user's timezone.
gdt.addYearsUTC(1);
```

-   **[Approval assignment scripts](r_UsefulApprovalAssignmentScripts.md)**  
This is a searchable version of the useful approval and assignment scripts.

**Parent Topic:**[Useful scripts](../concept/usefulScripts.md)

