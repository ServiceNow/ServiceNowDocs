---
title: Script includes
description: Script includes are used to store JavaScript that runs on the server.Script includes have a name, description, and, script. They also specify whether they are active or not, and whether they can be called from a client script. View existing or create a new script include using the Script Include form.Script includes are found under System Definition or System UI. You can call existing script includes from a script or create a new script include.Glide AJAX enabled Script Includes make the script include available to client scripts, list/report filters, reference qualifiers, or if specified as part of the URL.Privacy settings for Glide AJAX enabled script includes determine who can access a Glide AJAX enabled script include.Change the privacy setting for a single Glide AJAX enabled script include by adding the isPublic\(\) function.Protect your Glide AJAX enabled script includes against unauthorized use. For all records which are created a customer application, recommendations display that may help reduce security risk.Discovery script includes define JavaScript classes that you can use to accomplish Discovery tasks.When writing Discovery sensors and sensor-related scripts, you may want to use DiscoveryException or AutomationException to indicate that an exception has come from Discovery.
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Script includes

Script includes are used to store JavaScript that runs on the server.

Create script includes to store JavaScript functions and classes for use by server scripts. Each script include defines either an object class or a function.

Consider using script includes instead of global business rules because script includes are only loaded on request. See [Privacy settings on Glide AJAX enabled script includes](c_ScriptIncludes.md#) and [Discovery script includes](c_ScriptIncludes.md#) for more information.

For additional examples of scripts, see [Useful scripts](../../useful-scripts/concept/usefulScripts.md).

**Parent Topic:**[Server-side scripting](c_ServerScripting.md)

## Script include form

Script includes have a name, description, and, script. They also specify whether they are active or not, and whether they can be called from a client script. View existing or create a new script include using the Script Include form.

To access script includes, navigate to **All** &gt; **System Definitions** &gt; **Script Includes**.

<table id="table_ntx_fcg_tq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the script include. If you are defining a class, this must match the name of the class, prototype, and type. If you are using a classless \(on-demand\) script include, the name must match the function name.

</td></tr><tr><td>

API Name

</td><td>

The internal name of the Script Include. Used to call the Script Include from out-of-scope applications.

</td></tr><tr><td>

Glide AJAX enabled \(or Client callable\)

</td><td>

The script include is available to client scripts, list/report filters, reference qualifiers, or if specified as part of the URL. Glide AJAX enabled script includes are invoked from `GlideAjax` and require that users satisfy an ACL associated with the script include. When selected, the **Access Controls** Related Link is available. See [Privacy settings on Glide AJAX enabled script includes](c_ScriptIncludes.md#) for more information.

</td></tr><tr><td>

Mobile callable

</td><td>

The script include is available to client scripts called from mobile devices.

</td></tr><tr><td>

Sandbox enabled

</td><td>

The script include is available to scripts invoked from the script sandbox, such as a query condition.**Important:** Script includes should only be made available to the script sandbox if necessary.

For information about the script sandbox, see [Script sandbox evaluator](script-sandbox.md).

</td></tr><tr><td>

Application

</td><td>

The application where this script include resides.

</td></tr><tr><td>

Accessible from

</td><td>

Sets which applications can access this script include:

-   **All application scopes**

Can be accessed from any application scope.

-   **This application scope only**

Can be accessed only from the current application scope.


</td></tr><tr><td>

Active

</td><td>

Enables the script include when selected. Deselect the active field to disable the script include.

</td></tr><tr><td>

Description

</td><td>

Provides descriptive content regarding the script include.

</td></tr><tr><td>

Script

</td><td>

Defines the server side script to run when called from other scripts.The script must define a single JavaScript class or a global function. The class or function name must match the **Name** field.

</td></tr><tr><td>

Package

</td><td>

The package that contains this script include.

</td></tr><tr><td>

Created by

</td><td>

The user who created this script include.

</td></tr><tr><td>

Updated by

</td><td>

The user who most recently updated this script include.

</td></tr><tr><td>

Protection policy

</td><td>

Sets the level of protection for the script include:

-   **None**

Allows anyone to read and edit this downloaded or installed script include.

-   **Read-only**

Allows anyone to read values from this downloaded or installed script include. No one can change script values on the instance on which they download or install the script include.

-   **Protected**

Provides intellectual property protection for application developers. Customers who download the script include cannot see the contents of the script field. The script is encrypted in memory to prevent unauthorized users from seeing it in plain text.


</td></tr><tr><td class="sub-head" colspan="2">

Related lists on the form view:

</td></tr><tr><td>

Versions

</td><td>

Shows all versions of the script include. Use this list to compare versions or to revert to a previous version. See Versions.

</td></tr><tr><td>

Access Controls

</td><td>

Becomes available when the **Glide AJAX enabled** is selected and is hidden from standard script includes. Use to protect a script include against unauthorized use when public access is not granted.

</td></tr></tbody>
</table>## Use script includes

Script includes are found under System Definition or System UI. You can call existing script includes from a script or create a new script include.

To create an entirely new script include, you can follow the format of any of the existing script includes. In this example, the name of your script include is NewInclude and there is a single function called `myFunction`. It is important that the name of the script include match the name of the class, prototype, and type. When you create a new script include and give it a name, the system provides a code snippet with the class and prototype properly set up.

```javascript
var NewInclude =Class.create();
 
NewInclude.prototype={
  initialize :function(){},
 
  myFunction :function(){<Put function code here>},
 
  type :'NewInclude'};
```

You could then use the `myFunction` line like this:

```javascript
var foo =new NewInclude();
foo.myFunction();
```

## Glide AJAX enabled script includes

Glide AJAX enabled Script Includes make the script include available to client scripts, list/report filters, reference qualifiers, or if specified as part of the URL.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **System Definition** &gt; **Script Includes**.

2.  Select **New** or select an existing script include for viewing or editing.

    See [Use script includes](c_ScriptIncludes.md#) for additional information on writing script includes.

3.  Complete the form and select the **Glide AJAX enabled** option.

    A role selector pops up to select a user role and automatically create an Access Control entry. Select a user role and click **OK**.![Select a user role window.](../../../administer/security/image/role-selector-ccsi.png)

    **Note:** To disable the role selector window, set the glide.script.ccsi.enable\_acl\_create\_ux to **false**.

    A script include record with a role-based Access Control is created. The Access Control Related Link becomes available with the selection of the **Glide AJAX enabled** check box.


### Privacy settings on Glide AJAX enabled script includes

Privacy settings for Glide AJAX enabled script includes determine who can access a Glide AJAX enabled script include.

#### Private privacy-setting

The private privacy-setting means that guests who access public pages cannot access the Glide AJAX enabled script-include. A private script cannot be executed by a non-logged-in user.

#### Public privacy-setting

A public privacy-setting means that the client script can be executed by non-logged-in users that create an appropriate HTTP request. This can create a security problem if the client script provides confidential information.

The following script includes remain public by default because Make UI pages public or private need to access them:

-   GlideSystemAjax
-   SysMessageAjax
-   KnowledgeMessagingAjax
-   KnowledgeAjax
-   PasswordResetAjax

#### Set privacy on all Glide AJAX enabled script includes

Change the privacy setting on all Glide AJAX enabled script includes.

To provide further control over all Glide AJAX enabled script includes, administrators can add the glide.script.ccsi.ispublic property. This property changes the visibility of Glide AJAX enabled script includes by making them all public or private. Configure the property as follows:

|Title|Property|
|-----|--------|
|Name|glide.script.ccsi.ispublic|
|Type|true\|false|
|Value|false|

**Note:** To learn more about this property, see Require authentication by default for client-callable script includes in Instance Security Hardening Settings.

#### Change privacy on a single Glide AJAX enabled script include

Change the privacy setting for a single Glide AJAX enabled script include by adding the isPublic\(\) function.

The isPublic\(\) setting takes precedence over the **glide.script.ccsi.ispublic** property. For example, if the property is set to **false**, making all Glide AJAX enabled script-includes private, and a script sets isPublic\(\) to **true**, the script is public.

To change the privacy for a single Glide AJAX enabled script include, add the following method to the script include:

```javascript
isPublic:function(){return[true/false];},
```

Make the NewInclude client script private.

```javascript
var NewInclude =Class.create();
 
NewInclude.prototype={
   initialize:function(){},
 
   myFunction:function(){//Put function code here},
   isPublic:function(){return false;},
 
   type:'NewInclude'};
```

#### Security on Glide AJAX enabled script includes

Protect your Glide AJAX enabled script includes against unauthorized use. For all records which are created a customer application, recommendations display that may help reduce security risk.

When creating a Glide AJAX enabled script include, the system displays the following security recommendations if they have not yet been configured:

-   Add or define an Access Control, unless the script include has public access.
-   Use GlideRecordSecure instead of GlideRecord API for better security, if the script queries the database.

    **Note:** To disable the security recommendation messages, set the property glide.script.ccsi.customer\_scoped.security\_msgs\_enabled to **false** in the sys\_properties table. The default value is set to **true**.


See Instance Security Hardening Settings for additional information on security compliance.

## Discovery script includes

Discovery script includes define JavaScript classes that you can use to accomplish Discovery tasks.

**Note:** Users with discovery\_admin role can write script includes. Follow best practices for server-side and client-side scripting to prevent security issues. See knowledge article [KB0550828](https://support.servicenow.com/kb_view.do?sysparm_article=KB0550828) for more information.

### Using GlideRecordUtil to Work with GlideRecords

GlideRecordUtil is a utility class that provides methods that are useful for working with GlideRecords during Discovery. Refer to [GlideRecordUtil](../../../app-store/dev_portal/API_reference/GlideRecordUtil/concept/c_GlideRecordUtilAPI.md#) for descriptions of available methods.

### Getting a GlideRecord Instance

To get a GlideRecord instance for a given configuration item, and of the correct class and table, use the getCIGR\(sys\_id\) method. For example, the following code gets the GlideRecord of a CI with the sys\_id of 2dfd7c8437201000deeabfc8bcbe5d56:

```javascript
var now_GR = new GlideRecordUtil().getCIGR("2dfd7c8437201000deeabfc8bcbe5d56");
```

To retrieve any hierarchical table without knowing its class type, use the getGR\(base\_table, sys\_id\) method. For instance, to get a GlideRecord for a computer class CI, you might have to distinguish whether it is a computer class, Windows server, or Linux server class. Using this method guarantees a GlideRecord with the correct class. Different classes have different attributes. In this use case, a Windows server has attributes different from a Linux server. The following example shows how to get a GlideRecord in the correct class with its attributes.

```javascript
var now_GR = new GlideRecordUtil().getGR( "cmdb_ci_computer", "2dfd7c8437201000deeabfc8bcbe5d56");
```

### Getting All the Fields In a GlideRecord

The getFields\(now\_GR\) method returns a JavaScript object, such as a hashmap, of all the fields or attributes that exist in a given GlideRecord.

```javascript
var now_GR = new GlideRecordUtil().getGR("cmdb_ci_computer", "2dfd7c8437201000deeabfc8bcbe5d56");
var fields = new GlideRecordUtil().getFields(now_GR);
gs.log(fields.join(" ")); // List all the fields that are in a computer CI
```

### Populating GlideRecord Object Fields

The populateFromGR\(hashmap, gr, ignore\) method enables you to take a GlideRecord object and populate its fields and values into a JavaScript object. The third argument \(*ignore*\) is an optional JavaScript object that enables you to exclude certain fields. For example, you may not care about **sys\_created\_by** or **sys\_updated\_by** fields in a GlideRecord.

```javascript
var objectToPopulate = { }; 
var now_GR = new GlideRecordUtil().getGR("cmdb_ci_computer", "2dfd7c8437201000deeabfc8bcbe5d56"); 
var ignore = {"sys_created_on": true, "sys_updated_by": true}; 
new GlideRecordUtil().populateFromGR(objectToPopulate, now_GR, ignore); 
// Now the objectToPopulate contains field/value pairs from the computer GlideRecord
```

The mergeToGR\(hashmap, gr, ignore\) method enables you to populate a GlideRecord with a field/value-paired object. The ignore argument stops specified fields from being updated. The following code example updates a computer record's **name** and **os** fields, but does not update the **sys\_created\_by** field:

```javascript
var now_GR = new GlideRecordUtil().getGR("cmdb_ci_computer", "2dfd7c8437201000deeabfc8bcbe5d56"); 
var obj = {"name": "xyz", "os": "windows 2000", "sys_created_by", "aleck.lin"};
var ignore = {"sys_created_by": true}; 
new GlideRecordUtil().mergeToGR(obj, gr, ignore);
gr.update();
```

### Getting Table Hierarchies

The getTables\(table\) method returns a list of table hierarchies, as shown in the following example:

```javascript
var tables = new GlideRecordUtil().getTables("cmdb_ci_linux_server");
gs.log(tables.join(",")); 
// The result would be "cmdb_ci, cmdb_ci_computer, cmdb_ci_server, cmdb_ci_linux_server".
```

### Using DiscoveryException and AutomationException

When writing Discovery sensors and sensor-related scripts, you may want to use DiscoveryException or AutomationException to indicate that an exception has come from Discovery.

The DiscoveryException script include extends AutomationException, which extends the GenericException class. The following example uses DiscoveryException to throw an exception:

```javascript
function foo() { 
  if(//condition matches) throw new DiscoveryException("The message", "The cause"); }
```

The first argument takes the message of the exception and the second argument \(optional\) takes the cause of the exception. You may also want to catch the exception and log it as shown in the example below:

```javascript
try {
  foo(); 
} 
catch(e) { 
   if(e instanceof DiscoveryException)
     gs.log("A DiscoveryException occurred. It is " + e. getMessage() + " caused by " + e.getCause()); }
```

The above example also applies for AutomationException. DiscoveryException is typically used to provide exception processing specifically for Discovery, while AutomationException is used for exception processing that applies to both Orchestration and Discovery.

