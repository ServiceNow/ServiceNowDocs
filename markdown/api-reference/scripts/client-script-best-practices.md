---
title: Client-side scripting design and processing
description: Well-designed client scripts can reduce the amount of time it takes users to complete a form.If you create UI policies or client scripts for fields on a form, you must use another method to ensure that data in those fields is similarly controlled in a list.Use client data as much as possible to eliminate the need for time-consuming server lookups.When using setValue\(\) on a reference field, include the displayValue parameter to avoid additional server calls.When possible, consider using a UI policy instead of a client script.An excellent use for a client script is to validate the input from the user.Control the order of execution for your client scripts using the Order field. To avoid having two or more client scripts run concurrently and then conflict, you can add an order for the scripts to run in. Avoid Document Object Model \(DOM\) manipulation if possible. It can cause a maintainability issue when browsers are updated.A global client script is any client script where the selected Table is Global. Global client scripts have no table restrictions, therefore they will load on every page in the system introducing browser load delay in the process.Enclose the code in a client script inside a function.To avoid running time-consuming scripts unnecessarily, make sure that client scripts perform only necessary tasks.
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 11
breadcrumb: [Client-side scripting, Scripting, API implementation, API implementation and reference]
---

# Client-side scripting design and processing

Well-designed client scripts can reduce the amount of time it takes users to complete a form.

Proper client-side processing depends on the form loading first. Making record updates prior to form load can produce unexpected results that bypass client-side processing.

If you create client scripts to control field values on a form, you must use another method to control these field values in a list. You can:

-   Disable list editing for the table.
-   Create appropriate business rules or access controls for list editing.
-   Create data policies.
-   Create a separate onCellEdit client script.

**Parent Topic:**[Client-side scripting](client-side-scripting-overview.md)

## Restrict list editing

If you create UI policies or client scripts for fields on a form, you must use another method to ensure that data in those fields is similarly controlled in a list.

With the exception of onCellEdit client scripts, UI policies and client scripts apply to forms only. Use the following methods to restrict list editing when using client scripts:

-   Disable list editing for the table.
-   Create appropriate business rules or access controls for list editing.
-   Create data policies.
-   Create a separate onCellEdit client script.

## Minimize server lookups

Use client data as much as possible to eliminate the need for time-consuming server lookups.

Client scripting uses either data available on the client or data retrieved from the server. The top ways to get information from the server are g\_scratchpad and asynchronous GlideAjax lookup.

The primary difference between these methods is that g\_scratchpad is sent once when a form is loaded \(information is pushed from the server to the client\), whereas GlideAjax is dynamically triggered when the client requests information from the server.

**Note:** GlideRecord and g\_form.getReference\(\) are also available for retrieving server information. However, these methods are no longer recommended due to their performance impact. Both methods retrieve all fields in the requested GlideRecord when most cases only require one field.

### Retrieve server data using g\_scratchpad

The g\_scratchpad object passes information from the server to the client, such as when the client requires information not available on the form.

For example, if you have a client script that needs to access the field u\_retrieve, and the field is not on the form, the data is not available to the client script. A typical solution to this situation is to place the field on the form and then always hide it with a client script or UI policy. While this solution may be faster to configure, it is slower to execute.

If you know what information the client needs from the server before the form is loaded, a display business rule can create g\_scratchpad properties to hold this information. Theg\_scratchpad is sent to the client when the form is requested, making it available to all client-side scripting methods. This is a very efficient means of sending information from the server to the client. However, you can only load data this way when the form is loaded. The business rule cannot be triggered dynamically. In those cases, use an asynchronous GlideAjax call.

For example, assume you open an incident and need to pass this information to the client:

-   The value of the system property css.base.color
-   Whether or not the current record has attachments
-   The name of the caller's manager

A display business rule sends this information to the client using the following script:

```
g_scratchpad.css = gs.getProperty('css.base.color');
g_scratchpad.hasAttachments = current.hasAttachments();
g_scratchpad.managerName = current.caller_id.manager.getDisplayValue();
```

To access scratchpad data using a client script:

```
// Check if the form has attachments
if (g_scratchpad.hasAttachments)
    // do something interesting here
else
    alert('You need to attach a form signed by ' + g_scratchpad.managerName);
```

### Retrieve server data using asynchronous GlideAjax

Asynchronous GlideAjax allows you to dynamically request information from the server.

This script compares the support group of the CI and the assignment group of the incident by name:

```
//Alert if the assignment groups name matches the support group
function onChange(control, oldValue, newValue, isLoading) {
 
    if (isLoading)
        return;
 
    var ga = new GlideAjax('ciCheck');
 
    ga.addParam('sysparm_name', 'getCiSupportGroup');
    ga.addParam('sysparm_ci', g_form.getValue('cmdb_ci'));
    ga.addParam('sysparm_ag', g_form.getValue('assignment_group'));
    ga.getXML(doAlert); // Always try to use asynchronous (getXML) calls rather than synchronous (getXMLWait)
}
 
// Callback function to process the response returned from the server
function doAlert(response) {
 
    var answer = response.responseXML.documentElement.getAttribute("answer");
 
    alert(answer);
}
```

This script relies on the accompanying script include:

```
var ciCheck = Class.create();
 
ciCheck.prototype = Object.extendsObject(AbstractAjaxProcessor, {
 
    getCiSupportGroup: function() {
 
        var retVal = ''; // Return value
        var ciID   = this.getParameter('sysparm_ci');
        var agID   = this.getParameter('sysparm_ag');		
        var ciRec  = new GlideRecord('cmdb_ci');
 
        // If we can read the record, check if the sys_ids match
        if (ciRec.get(ciID)) {
            if (ciRec.getValue('support_group') == agID)
                retVal = 'CI support group and assignment group match';
            else
                retVal = 'CI support group and assignment group do not match';
 
            // Can't read the CI, then they don't match
        } else {
            retVal = 'CI support group and assignment group do not match';
        }
 
        return retVal;
    }
 
});
```

## Use the setValue\(\) displayValue parameter for reference fields

When using setValue\(\) on a reference field, include the displayValue parameter to avoid additional server calls.

When using setValue\(\) on a reference field, be sure to include the reference field display value as the 3rd parameter. If you set the value without the displayValue, the instance does a synchronous call to retrieve the display value for the record you specified. This extra round trip to the server can impact performance.

This example demonstrates the incorrect way to call setValue:

```
var id = '5137153cc611227c000bbd1bd8cd2005';
 
g_form.setValue('assigned_to', id); // Client needs to go back to the server to
                                    // fetch the name that goes with this ID
```

Instead, include the display value as an optional parameter in setValue\(\):

```
var id = '5137153cc611227c000bbd1bd8cd2005';
var name = 'Fred Luddy';
 
g_form.setValue('assigned_to', id, name); // No server call required
```

## Use UI policy instead of a client script

When possible, consider using a UI policy instead of a client script.

UI policies provide these benefits over client scripts:

-   UI policies have an **Order** field to allow full control over the order in which client-side operations take place.
-   UI policies do not require scripting to make a field mandatory, read-only, or visible.

**Note:** UI policies apply after client scripts.

## Validating the input by using a client script

An excellent use for a client script is to validate the input from the user.

This validation improves the user experience because the user finds out if there are data issues before submitting the information.

An example of validation is to verify that the **Impact** field value is valid with the **Priority** field value. In this example, Low impact is not allowed with High priority.

```
if (g_form.getValue('impact') == '3' && g_form.getValue('priority') == '1')
   g_form.showFieldMsg('impact', getMessage('Low impact now allowed with High priority'), 'error');

```

## Set client script order

Control the order of execution for your client scripts using the Order field. To avoid having two or more client scripts run concurrently and then conflict, you can add an order for the scripts to run in.

### Before you begin

Role required: admin

### About this task

Adding an order to the client script creates a processing sequence, ordered from lowest to highest number. If two scripts conflict, the client script with the lower number executes first.

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Client Script** and open an existing client script or click **New**.

2.  Configuring the form layout to include the **Order** field.

3.  Add a number to the order field based on what order you want it to run in relation to other client scripts.

    Choose a lower number for the script you want to execute first.


## Avoid DOM manipulation

Avoid Document Object Model \(DOM\) manipulation if possible. It can cause a maintainability issue when browsers are updated.

Instead, use the GlideForm API or consider a different approach for the solution. In general, when using DOM manipulation methods, you have to reference an element in the DOM by ID or using a CSS selector. When referencing out-of-box DOM elements, there is a risk that the element ID or placement within the DOM could change, causing the code to stop working and/or generate errors. Use forethought, caution, and have a full understanding of the risk you are incurring. Review these objects and reduce the use of DOM manipulation methods as much as possible.

## Avoid global client scripts

A global client script is any client script where the selected Table is Global. Global client scripts have no table restrictions, therefore they will load on every page in the system introducing browser load delay in the process.

There is no benefit to loading this kind of scripts on every page.

As an alternative, and for a more modular and scalable approach, consider moving client scripts to a base table \(such as Task\[task\] or Configuration Item\[cmdb\_ci\]\) that can be derived for all the child/extending tables. This eliminates the system loading the scripts on every form in the UI - such as home pages or Service Catalog where they are rarely \(if ever\) needed.

## Enclose code in functions

Enclose the code in a client script inside a function.

Client scripts without a function cause issues with variable scope. When code is not enclosed in a function, variables and other objects are available and shared to all other client-side scripts. If you are using the same variable names, it is possible that they could collide. This can lead to unexpected consequences that are difficult to troubleshoot.

Consider this example:

```
var state = "6";
 
function onSubmit() {
 
   if(g_form.getValue('incident_state') == state) {
   		alert("This incident is Resolved");
   }
}
```

Because the *state* variable is not enclosed in a function, all client-side scripts, have access to it. Other scripts may also use the common variable name *state*. The duplicate names can conflict and lead to unexpected results. These issues are difficult to isolate and resolve. To avoid this issue, ensure that all code is wrapped in a function:

```
function onSubmit() {
 
   var state = "6";
 
   if(g_form.getValue('incident_state') == state) {
   		alert("This incident is Resolved");
   }
}
```

This solution is much safer because the scope of the variable *state* is limited to the onSubmit\(\) function. Therefore, the *state* variable does not conflict with *state* variables in other client-side scripts.

## Run only necessary scripts

To avoid running time-consuming scripts unnecessarily, make sure that client scripts perform only necessary tasks.

The following examples demonstrate improvements to the initial code sample. Each example demonstrates a particular enhancement to the script to improve performance and avoid unnecessary calls.

Remember that client scripts have no **Condition** field. This means that onLoad\(\) and onChange\(\) scripts run in their entirety every time the appropriate form is loaded. This example is an inefficient onChange\(\) client script set to run when the **Configuration item** field changes.

```
//Set Assignment Group to CI's support group if assignment group is empty
function onChange(control, oldValue, newValue, isLoading) {
 
    var ciSupportGroup = g_form.getReference('cmdb_ci').support_group;
 
    if (ciSupportGroup != '' && g_form.getValue('assignment_group) != '')
        g_form.setValue('assignment_group', ciRec.support_group.sys_id);
}
```

This example improves upon the first by replacing the getReference\(\) or GlideRecord lookup with an asynchronous GlideAjax call.

```
//Set Assignment Group to support group if assignment group is empty
function onChange(control, oldValue, newValue, isLoading) {
 
    var ga = new GlideAjax('ciCheck');
 
    ga.addParam('sysparm_name', 'getSupportGroup');
    ga.addParam('sysparm_ci', g_form.getValue('cmdb_ci'));
    ga.getXML(setAssignmentGroup);
}
 
function setAssignmentGroup(response) {
 
    var answer = response.responseXML.documentElement.getAttribute("answer");
 
    g_form.setValue('assignment_group', answer);
}
```

The **isLoading** flag is the simplest way to prevent unnecessary code from taking up browser time in onChange scripts. The **isLoading** flag should be used at the beginning of any script that is not required to run when the form is loading. There is no need to run this script on a form load because the logic would have already run when the field was last changed. Adding the **isLoading** check to the script prevents it from doing a cmdb\_ci lookup on every form load.

The **isTemplate** flag indicates that a template is loading.

```
//Set Assignment Group to CI's support group if assignment group is empty
function onChange(control, oldValue, newValue, isLoading, isTemplate) {
 
    if (isLoading)
        return;
 
    var ga = new GlideAjax('ciCheck');
 
    ga.addParam('sysparm_name', 'getSupportGroup');
    ga.addParam('sysparm_ci', g_form.getValue('cmdb_ci'));
    ga.getXML(setAssignmentGroup);
}
 
function setAssignmentGroup(response) {
 
    var answer = response.responseXML.documentElement.getAttribute("answer");
 
    g_form.setValue('assignment_group', answer);
}

```

If the onChange script should run during loading, use the following convention:

```
function onChange(control, oldValue, newValue, isLoading, isTemplate) {
 
    if (isLoading) {}; // run during loading
 
    // rest of script here
 
}
```

The newValue check tells this script to continue only if there is a valid value in the relevant field. This prevents the script from running when the field value is removed or blanked out. This also ensures that there will always be a valid value available when the rest of the script runs.

```
//Set Assignment Group to CI's support group if assignment group is empty
function onChange(control, oldValue, newValue, isLoading, isTemplate) {
 
    if (isLoading)
        return;
 
    if (newValue) {
        var ga = new GlideAjax('ciCheck');
 
        ga.addParam('sysparm_name', 'getSupportGroup');
        ga.addParam('sysparm_ci', g_form.getValue('cmdb_ci'));
        ga.getXML(setAssignmentGroup);
    }
}
 
function setAssignmentGroup(response) {
 
   var answer = response.responseXML.documentElement.getAttribute("answer");
 
   g_form.setValue('assignment_group', answer);
}
```

To have the script react to a value that changes after the form loads, use the newValue != oldValue check.

**Note:** This example does not catch users changing a value and then changing it back to its original value.

```
//Set Assignment Group to CI's support group if assignment group is empty
function onChange(control, oldValue, newValue, isLoading, isTemplate) {
 
    if (isLoading)
        return;
 
    if (newValue) {
        if (newValue != oldValue) {
            var ga = new GlideAjax('ciCheck');
 
            ga.addParam('sysparm_name', 'getSupportGroup');
            ga.addParam('sysparm_ci', g_form.getValue('cmdb_ci'));
            ga.getXML(setAssignmentGroup);
        }
    }
}
 
function setAssignmentGroup(response) {
 
   var answer = response.responseXML.documentElement.getAttribute("answer");
 
   g_form.setValue('assignment_group', answer);
}
```

In this example, the GlideAjax call is buried one level deeper by rearranging the script to check as many things available to the client as possible before running the server calls. The script checks the assignment before executing the GlideAjax call. This prevents the server lookup when the **assignment\_group** field is already set.

```
//Set Assignment Group to CI's support group if assignment group is empty
function onChange(control, oldValue, newValue, isLoading, isTemplate) {
 
    if (isLoading)
       return;
 
    if (newValue) {
        if (newValue != oldValue) {
            if (g_form.getValue('assignment_group') == '') {
                var ga = new GlideAjax('ciCheck');
 
                ga.addParam('sysparm_name', 'getSupportGroup');
                ga.addParam('sysparm_ci', g_form.getValue('cmdb_ci'));
                ga.getXML(setAssignmentGroup);
            }
        }
    }
}
 
function setAssignmentGroup(response) {
 
   var answer = response.responseXML.documentElement.getAttribute("answer");
 
   g_form.setValue('assignment_group', answer);
}
```

