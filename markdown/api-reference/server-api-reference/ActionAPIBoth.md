---
title: action - Scoped, Global
description: The action API provides methods to handle data for URLs in a UI action script.Gets a GlideURI object to determine the user view.Gets the URL of the return page in view after a UI action is complete.Gets the value of a URL parameter.Opens a page with a GlideRecord in the user view.Indicates whether to enable or disable pop-up windows on the page in the current view.Sets the redirect URI for this transaction, which determines the next page the user sees.Sets the return URI for this transaction after a UI action is complete. You can use this method to determine what page the user has in view when they return from submit.Sets a URL parameter name and value.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# action - Scoped, Global

The action API provides methods to handle data for URLs in a UI action script.

Use this API to configure UI actions with which users can interact. Use these scripts in the UI Action \[sys\_ui\_action\] table. For information, see [UI actions](https://www.servicenow.com/docs/access?context=t_EditingAUIAction&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Methods for this API are referred to by the variable name 'action' in any server-side JavaScript. To learn more, see [Creating interactions with UI actions](https://developer.servicenow.com/blog.do?p=/post/training-ui-action-101/).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## action - getGlideURI\(\)

Gets a GlideURI object to determine the user view.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_exr_lfj_nkb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

GlideURI object representing the URI parameter of the user view.-   [GlideURI - Scoped](../../GlideURIScoped/concept/c_GlideURIScopedAPI.md#)
-   [GlideURI - Global](../../GlideURIGlobal/concept/GlideURIGlobalAPI.md#)

**Note:** Any other returned value is considered an error, including null.

</td></tr></tbody>
</table>The following example shows how to get the user view and set the redirect URL to the service catalog home page.

```
var uri = action.getGlideURI();
var path = 'catalog_home.do';

uri.set('sysparm_view', 'catalog_default');
action.setRedirectURL(uri.toString(path));
```

## action - getReturnURL\(\)

Gets the URL of the return page in view after a UI action is complete.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|URL of the return page in view after a UI action is complete.|

```
action.getReturnURL();
```

## action - getURLParameter\(String parameterName\)

Gets the value of a URL parameter.

|Name|Type|Description|
|----|----|-----------|
|parameterName|String|Name of the URL parameter name to be queried for the URL parameter value.|

|Type|Description|
|----|-----------|
|String|URL parameter value.|

```
action.getURLParameter('sysparm_query');
```

## action - openGlideRecord\(Object gr\)

Opens a page with a GlideRecord in the user view.

|Name|Type|Description|
|----|----|-----------|
|gr|[GlideRecord](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#)|GlideRecord of the page to be opened in the user view.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to include the caller name and incident description created from an interaction record. For more details, see [Customizing Configurable Workspace with declarative actions](https://www.servicenow.com/docs/access?context=declarative-actions-landing&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

```
if(current.update()){
  var inc = new GlideRecord("incident");
  inc.newRecord();
  inc.caller_id = current.opened_for;
  inc.short_description = current.short_description;
  action.openGlideRecord(inc);
}
```

## action - setNoPop\(Boolean noPop\)

Indicates whether to enable or disable pop-up windows on the page in the current view.

<table id="table_mms_gfj_nkb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

noPop

</td><td>

Boolean

</td><td>

Flag indicating whether to enable or disable pop-up windows on the page:-   true: Disables pop-up windows.
-   false: Default. Enables pop-up windows.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to disable pop-up windows for a UI action.

```

action.setNoPop(true);
```

## action - setRedirectURL\(Object URL\)

Sets the redirect URI for this transaction, which determines the next page the user sees.

For use cases:

-   [Create a UI routing action](https://www.servicenow.com/docs/access?context=useful-client-side-scripts&version=xanadu&pubname=xanadu-application-development&section=t_CreateAUIRoutingAction&ft:locale=en-US)
-   [Create knowledge articles from HR cases](https://www.servicenow.com/docs/access?context=ui-action-hrcase-article&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)
-   [Task relationships with UI actions](https://www.servicenow.com/docs/access?context=r_UIActions&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

|Name|Type|Description|
|----|----|-----------|
|URL|Object|URL to set as the redirect. You can provide the URL as a string or a [GlideRecord](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#). If you pass the URL as a GlideRecord, this value takes the focus to that record's form.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to redirect a user to a URL from a UI action using the [current](https://www.servicenow.com/docs/access?context=c_ScriptableServiceCatalogVariables&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US) variable.

```
var fixchg = new GlideRecord("change_request");
fixchg.short_description= current.short_description;
fixchg.comments= current.comments.getHTMLValue();
// fixchg.parent = current.sys_id;
fixchg.insert();
FixChange();
 
gs.addInfoMessage("Change "+ fixchg.number+" created");
action.setRedirectURL(current);
action.setReturnURL(fixchg);
 
function FixChange(){
var m2m = new GlideRecord('task_rel_task');
m2m.initialize();
m2m.child= current.sys_id;
m2m.parent= fixchg.sys_id;
m2m.type.setDisplayValue("Fixes::Fixed by");
m2m.insert();}
```

The following example shows how to create a new incident record and redirect to the new incident after a UI action completes.

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

## action - setReturnURL\(Object URL\)

Sets the return URI for this transaction after a UI action is complete. You can use this method to determine what page the user has in view when they return from submit.

|Name|Type|Description|
|----|----|-----------|
|URL|Object|URI to set as the return location after a UI action is complete. You can provide the URL as a string or a [GlideRecord](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).|

|Type|Description|
|----|-----------|
|void| |

The following example enables the user to select the UI action to create a change record using information from the problem record and the change template. After the change, the user returns to [current](https://www.servicenow.com/docs/access?context=c_ScriptableServiceCatalogVariables&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US) view. For more information, see [Scripted templates](https://www.servicenow.com/docs/access?context=r_ScriptedTemplates&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US). For more use cases, see [Task relationships with UI actions](https://www.servicenow.com/docs/access?context=r_UIActions&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

```
var change = new GlideRecord("change_request");
change.initialize();
change.short_description = current.short_description;
change.description = current.u_details;
change.cmdb_ci = current.u_service;
change.priority = current.priority;
change.requested_by = current.caller_id;
change.assignment_group.setDisplayValue('Change & Release');
change.u_status = 'New';
change.parent = current.number;
change.applyTemplate("standard_rfc");
current.rfc = change.insert();
current.comments = 'Change ' + change.number + ' created.';

var mySysID = current.update();

gs.addInfoMessage("Change " + change.number + " created");
action.setRedirectURL(change);
action.setReturnURL(current);
```

## action - setURLParameter\(String parameterName, String parameterValue\)

Sets a URL parameter name and value.

|Name|Type|Description|
|----|----|-----------|
|parameterName|String|Name of the URL parameter.|
|parameterValue|String|Value of the parameter.|

|Type|Description|
|----|-----------|
|void| |

```
action.setURLParameter('sysparm_query', 'priority=2^active=true');
```

