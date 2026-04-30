---
title: Client-side script use cases
description: Use cases for client-side scripts include displaying field messages, changing form colors, adding fields, and creating UI routing actions.This is an example of adding a Company field to the checkout below the Requested for field using non-cart layout macros, that is, glide.sc.use\_cart\_layouts is false.Add autofill functionality is also called incident template, auto assignments, quick calls, call script, or auto populate.Changes color of a form field of the form on state change. The script can easily be changed to adjust any property of any object on the page accessible via the HTML DOM.This solution enables you to create a record with the service desk without knowing whether it is an incident or request item; the service desk can then route the record to the appropriate table.Rather than use JavaScript alert\(\), for a cleaner look, you can display an error on the form itself. The methods showFieldMsg\(\) and hideFieldMsg\(\) can be used to display a message just below the field itself.You can use a script to validate input upon a UI Action click on the client side before updating the record on the server side. The user will not have to click the button twice to validate the required fields and update the record.
locale: en-US
release: zurich
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Useful scripts, Scripting, API implementation, API implementation and reference]
---

# Client-side script use cases

Use cases for client-side scripts include displaying field messages, changing form colors, adding fields, and creating UI routing actions.

**Parent Topic:**[Useful scripts](usefulScripts.md)

## Add a field to the service catalog checkout

This is an example of adding a **Company** field to the checkout below the **Requested for** field using non-cart layout macros, that is, **glide.sc.use\_cart\_layouts** is `false`.

### Before you begin

Role required: Admin

### About this task

This field passes a provided value to the **Company** field of the Service Catalog Request.

This example makes the following assumptions:

-   The instance using two-step checkout. If two-step checkout is not enabled, enable it before beginning. For more information, see [Service Catalog checkout models](https://www.servicenow.com/docs/access?context=c_EnableATwoStepCheckout&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
-   This example populates the **Company** field on the Service Catalog Request form. If the field does not appear on the form, configure the form before beginning. For instructions, see [Personalize a form](https://www.servicenow.com/docs/access?context=t_PersonalizeAForm&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

### Procedure

1.  Go to **System UI &gt; UI Macros** and select **servicecatalog\_cart\_template**.

2.  Find where there are hidden variables declared and add the following line:

    ```
    <input type="HIDDEN" name="cart_id" id="cart_id" value="$[sc_cart.sys_id]" />
    ```

3.  Find the following code, which generates the **Requested For** code:

    ```
    <tr class="header">
    <td width = "30%">
      ${gs.getMessage('Requested for')}:
      </td>
      <td width="70%">
        <label for="requestor_location">${gs.getMessage('Deliver to')}:</label>
      </td>
    </tr>
    <tr><td>$[SP]</td> 
    </tr>
      <tr><td valign="top">
        <j2:if test="$[jvar_can_delta_rf == false]">
          $[sc_cart.requested_for.getDisplayValue()]
        </j2:if>
        <j2:if test="$[jvar_can_delta_rf != false]">
          <g2:catalog_requested_for />
        </j2:if>
      </td>
      <td>
        <textarea id="requestor_location" style="width:100%" rows="4"
          name="requestor_location" wrap="soft" onChange="catDeliveryAddress('$[sc_cart.sys_id]', 'requestor_location');"> 
          $[sc_cart.delivery_address]
        </textarea>
      </td>
    </tr>
    <tr>
      <td>$[SP]</td>
    </tr>
    ```

4.  Add the following code afterward:

    ```
    <tr class="header">
      <td colspan="2">Company</td>
    </tr>
    <tr>
      <td>$[SP]</td>
    </tr>
    <tr>
      <td colspan="2">
        <g2:ui_reference name="core_company" table="core_company" onchange="setCartValue()"/>
      </td>
    </tr>
    <tr>
      <td>$[SP]</td>
    </tr>
    ```

    **Note:** The `'ui_reference'` macro defines a reference field. There are several macros for different field types. You can see examples of these field types under **System UI -&gt; UI Macros**. These macros start with `'ui_'`. For this example, the reference field created is named **core\_company**. For more information, see [UI macros](../../server-scripting/concept/c_UIMacros.md#).

5.  Now navigate to **System UI &gt; UI Pages** and select the **servicecatalog\_checkout\_one** UI Page.

6.  Add the followings script to the **Client script** field.

    ```
    function setCartValue() { 
      var newField = gel('core_company'); 
      var myCart = gel('cart_id'); 
      var cart_item = new GlideRecord('sc_cart_item');
      cart_item.addQuery('cart', myCart.value);
      cart_item.query(); 
      if(cart_item.next()) {
        cart_item.hints = "<hints><entry key='sysparm_processing_hint' value='setfield:request.company=" + newField.value + "'/></hints>";
        cart_item.update(); 
      } 
    }
    ```

    For this example, the reference field was called **core\_company**, and the field being populated on the request is **company**. If different fields are used:

    -   Find this line: `var company = gel('core_company');` and replace **core\_company** with the name of the field in the checkout.
    -   In the line that starts with `'cart_item.hints'` replace `'request.company'` with the name of the field to be populated on the request ticket where `'request'` is the request being generated and `'company'` is the name of the field.
    When an item is ordered, the company field appears on the **Catalog** form.


## Add autofill functionality

Add autofill functionality is also called incident template, auto assignments, quick calls, call script, or auto populate.

To auto-fill a **Short Description** field based on the **Subcategory** selected:

1.  Create a lookup table.
2.  Populate the key field, **Subcategory**.
3.  Populate the auto-filled field, **Short Description**.

```
function onChange(control, oldValue, newValue, isLoading) { 
  if (isLoading) { return; } 
  var newrec = gel('sys_row');
  //Check if new record
  if (newrec.value == -1) { 
    var lookup = new GlideRecord('u_short_desc_lookup'); 
    lookup.addQuery('u_subcategory', g_form.getValue('subcategory'));
    lookup.query();
    var temp; //temp var - reusable
    if (lookup.next()) {
      temp = lookup.u_short_description;
        if (null != temp) { //Set the form value from lookup if there is a lookup value
          g_form.setValue('short_description', temp); } 
        else {
          g_form.setValue('short_description', "" ); } } 
   else { 
     //If a lookup record does not exist based on lookup.addQuery 
     //Then set to UNDEFINED or NULL depending on type
      g_form.setValue('short_description', ""); } } 
}
```

You can populate many fields or pull in call script questions into the **Comments** field so call center personnel gather good information to pass on to a technician.

-   **Setting a field to password reset**

    Lookup table has a record with the following key and auto-fill settings:

    -   **Subcategory** = Password
    -   **Short Description** = Password Reset
    Client script settings:

    -   **Type** = onChange
    -   **Table name** = incident
    -   **Field name** = Subcategory
    When the user selects the subcategory of Password on the Incident form, a client script looks up the matching record and sets the short description equal to Password Reset.


## Change form color on state change

Changes color of a form field of the form on state change. The script can easily be changed to adjust any property of any object on the page accessible via the HTML DOM.

**Warning:** The customization described here was developed for use in specific instances, and is not supported by Now Support. This method is provided as-is and should be tested thoroughly before implementation. Post all questions and comments regarding this customization to our community [forum](http://community.service-now.com/).

Name: Change Form Color on State Change

Type: Client script

Description: Changes color of a form field of the form on state change. The script can easily be changed to adjust any property of any object on the page accessible via the HTML DOM.

Script:

```
function onChange(control, oldValue, newValue, isLoading) { 
  var elementID = gel("incident.priority");
    switch(newValue) { 
      case "1": elementID.style.backgroundColor = "red"; break; 
      case "2": elementID.style.backgroundColor = "tomato"; break;
      case "3": elementID.style.backgroundColor = "orange"; break;
      case "4": elementID.style.backgroundColor = "yellow"; break;
      case "5": elementID.style.backgroundColor = "green"; break; 
      default: elementID.style.backgroundColor = "white"; break; } }
```

## Create a UI routing action

This solution enables you to create a record with the service desk without knowing whether it is an incident or request item; the service desk can then route the record to the appropriate table.

### Before you begin

Role required: **Admin**

### Procedure

1.  Create a new table that extends the `task` table \(for example, New Call\).

2.  Create a module to create a new New Call record.

3.  Create any fields that you want on the New Call table.

    The only fields you need are those fields necessary to determine whether the new call should route to an Incident or a Request Item. Ensure that the form contains any fields that you want to pass to the Incident or Request Item. In this example, the following are created on the form:

    -   **Requested for** \(reference\)
    -   **Location** \(reference\)
    -   **Call type** \(choice with two values--Incident and Request\)
    -   **Request Item** \(reference to the `sc_cat_item` Item table\)
4.  Add some UI policies to set a couple of fields to mandatory and hide the **Request item** field based on the **Call type** selection.

5.  Remove unnecessary buttons and functionality from the form.

6.  Create a new UI Action button.

    This button redirects the user to either an incident or a request. It also creates the incident record and copies values to the incident and the Request Item form.

    ```
    var reqItem = current.u_item;
    var requestedFor = current.u_requested_for;
    var location = current.location;
    
    if(current.u_incident_request == 'Incident'){
      //Create a new incident record and redirect to the new incident
      var rec = new GlideRecord('incident');
      rec.initialize();
      rec.caller_id = requestedFor;
      rec.location = location;
      rec.insert();
      action.setRedirectURL(rec);
    }
    
    if(current.u_incident_request == 'Request'){
      //Build the url and route the user to the request item
      var url = '';
      if(current.u_item.sys_class_name == 'sc_cat_item_guide'){
        url = 'com.glideapp.servicecatalog_cat_item_guide_view.do?sysparm_initial=true&sysparm_guide=' + 
          reqItem + '&sysparm_user=' + requestedFor + '&sysparm_location=' + location;
      }
      else{
        url = 'com.glideapp.servicecatalog_cat_item_view.do?sysparm_id=' + reqItem + '&sysparm_user=' +  
          requestedFor + '&sysparm_location=' + location;
      }
      action.setRedirectURL(url);
    }
    ```

7.  The **Route** button in the preceding example passes the **Requested for** and **Location** values in the URL to the Request Item form.

    Ensure that you have variables called *requested\_for* and *location* on your item, record producer, or order guide that map these values using the following client script. There is a limit as to how much information you can pass, as the URL has a restricted length. Avoid sending information from long text fields using this method.

    ```
    function onLoad() {
      var url = document.location.toString();
      var userKey = 'sysparm_user=';
      var locKey = 'sysparm_location=';
      var userPosition = url.indexOf(userKey);
      var locPosition = url.indexOf(locKey)
      if (userPosition != -1) {
        var user = url.substr(userPosition+userKey.length, 32);
        g_form.setValue('requested_for', user);
      }
      if (locPosition != -1) {
        var loc = url.substr(locPosition+locKey.length, 32);
        g_form.setValue('location', loc);
      }
    }
    ```


## Display field messages

Rather than use JavaScript alert\(\), for a cleaner look, you can display an error on the form itself. The methods showFieldMsg\(\) and hideFieldMsg\(\) can be used to display a message just below the field itself.

showFieldMsg and hideFieldMsg are methods that can be used with the *g\_form* object.

These methods are used to change the form view of records \(Incident, Problem, and Change forms\). These methods may also be available in other client scripts, but must be tested to determine whether they work as expected.

When a field message is displayed on a form on load, the form scrolls to ensure that the field message is visible. Ensuring that users do not miss a field message because it was off the screen.

The global property *glide.ui.scroll\_to\_message\_field* controls automatic message scrolling when the form field is offscreen \(scrolls the form to the control or field\).

<table id="table_bgp_bwq_bp"><thead><tr><th>

Method Detail

</th><th>

Parameters

</th><th>

Example

</th></tr></thead><tbody><tr><td>

showFieldMsg\(input, message, type, \[scrollform\]\)

</td><td>

-   input — name of the field or control
-   message — message you would like to appear
-   type — 'info', 'error', or 'warning'; defaults to info if not supplied
-   scroll form — \(optional\) Set scrollForm to false to prevent scrolling to the field message offscreen

</td><td>

Error message```
g_form.showFieldMsg('impact','Low impact not allowed with High priority','error');
```

![Low impact not allowed with high priority message.](../image/ShowFieldMsgError.png)

Informational message

```
g_form.showFieldMsg('impact', 'Low impact response time can be one week','info');
//or this defaults to info type
//g_form.showFieldMsg('impact', 'Low impact response time can be one week');
```

![Low impact response time can be one week message.](../image/ShowFieldMsgInfo.png)

</td></tr><tr><td>

hideFieldMsg\(input\)

</td><td>

-   input — name of the field or control
-   clearAll — \(optional\) boolean parameter indicating whether to clear all messages. If true, all messages for the field are cleared. If false or empty, only the first message is removed

</td><td>

Removing a message```
//this will clear the first message printed to the field
g_form.hideFieldMsg('impact');
```

</td></tr></tbody>
</table>### Legacy support

The showErrorBox\(\) and hideErrorBox\(\) methods are not recommended.

## Using client and server code in a UI action

You can use a script to validate input upon a UI Action click on the client side before updating the record on the server side. The user will not have to click the button twice to validate the required fields and update the record.

The script calls the client function for client-side validation, and the UI action completes the task if it passes. The `code that runs without onclick` statement ensures that the server-side function does not run until the client function is no longer running. If successful, the server-side function runs and updates the record.

```
// Client-side onclick function
function resolveIncident() {
  // Set the 'Incident state' and 'State' values to 'Resolved', and display mandatory fields
  g_form.setValue('incident_state', 6);
  g_form.setValue('state', 6);
  g_form.setValue('resolved_by', g_user.userID);

  // Call the UI action and skip the 'onclick' function
  gsftSubmit(null, g_form.getFormElement(), 'resolve_incident'); //MUST call the 'Action name' set in this UI Action
}

// Code that runs without 'onclick'
// Ensure call to server-side function with no browser errors
if (typeof window == 'undefined')
  serverResolve();

// Server-side function
function serverResolve() {
  current.incident_state = IncidentState.RESOLVED;
  current.state = IncidentState.RESOLVED;
  current.resolved_by = gs.getUserID();
  current.update();
}
```

### gsftSubmit\(String control, Object form, String action\_name\)

Submits a form as if the user had clicked a UI Action after checking for required fields and executing onSubmit\(\) client scripts. Enables calling client-side code and server-side code and in a single UI action.

<table id="table_lmr_qwr_fz" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

control

</td><td>

String

</td><td>

Name of a form button on which you want to simulate a user click. Use `null` otherwise.

</td></tr><tr><td>

form

</td><td>

Object

</td><td>

Optional. The form element that contains the submitted input. You can retrieve this value by calling the g\_form.getFormElement\(\) method.

</td></tr><tr><td>

action\_name

</td><td>

String

</td><td>

Action name. This value is provided in the record listed in the UI Actions \[sys\_ui\_action\] table.For example, `'resolve_incident'` is the action name of the **Resolve** button in the Incident \[incident\] table.

</td></tr></tbody>
</table>**Related topics**  


[GlideForm - getFormElement\(\)](../../../app-store/dev_portal/API_reference/GlideForm/concept/c_GlideFormAPI.md#)

[Scoped GlideSystem - eventQueue\(String name, Object instance, String parm1, String parm2, String queue\)](../../../app-store/dev_portal/API_reference/glideSystemScoped/concept/c_GlideSystemScopedAPI.md#)

[GlideUser - Client](../../../app-store/dev_portal/API_reference/GlideUser/concept/c_GlideUserAPI.md#)

[Defining UI actions](https://www.servicenow.com/docs/access?context=c_UIActions&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

