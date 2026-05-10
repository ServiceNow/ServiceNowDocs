---
title: api - UI Builder
description: The api API provides methods that you can use when developing client scripts in the UI Builder.Page properties can be configured within UI Builder. The configuration values depend on the context in which the page is used.Context session properties associated with the current user.Boolean flag that indicates whether the last fetch attempt for the specified data resource instance finished successfully.Displays the specified error message at the top of the current form.Displays the specified informational message at the top of the current form.Adds an option to the specified choice type field.Displays the specified warning message at the top of the current form.Removes all informational and error messages from the top of the current form.Clears all options from the specified choice type field.Executes the specified UI action.Triggers an execute operation on the specified data resource.Hides the oldest message next to the specified field or clears all messages associated with the field.Hides the specified related list on the current form.Hides all related lists on the current form.Triggers a refresh operation for the specified non-mutating data resource instance.Reloads the current form using the same table and sys\_id.Removes an option from the specified choice type field.Triggers form submission using the Save UI action.Sets whether the specified form field is mandatory.Sets the read/write capabilities of the specified form field.Updates a specified GlideForm field with the specified value. Optionally, you can also update the display value with the same specified value.Sets the visibility of the specified form field.Displays the specified message next to the specified field.Displays the specified related list on the current form.Displays all related lists associated with the current form.Triggers form submission using the specified UI action.Emits an event with the specified name and payload.Sets the value of the specified client state parameter.Sets the value of the specified client state parameter to the value returned by the specified callback function.Current value of the specified client state parameter.
locale: en-US
release: australia
product: UI Builder API Reference
classification: ui-builder-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 24
breadcrumb: [UIB API reference, API reference, API implementation and reference]
---

# api - UI Builder

The api API provides methods that you can use when developing client scripts in the UI Builder.

This API is exposed to client scripts, also known as page scripts. Client scripts are executed in response to something happening on a page, such as:

-   User interaction events/actions, such as a button click.
-   Lifecycle events, such as a data broker execution started.

These scripts do not have to return anything to the framework and can be written as an asynchronous function.

This API is also exposed to scripted property values. These scripts are executed whenever the framework-runtime needs to calculate a value, such as:

-   Passing to a component property.
-   Determining component visibility.
-   Emitting an event with a payload.

These scripts cannot be written as an asynchronous function. They also cannot invoke side-effect methods on the api object, such as, api.emit\(\), api.setState\(\), and api.data.&lt;data\_resource\_id&gt;.\*\(\).

The api object contains both configuration dependent and configuration independent properties that you can access within the context of the associated page or component. You cannot directly modify the properties within this object. Modification can only be made through the available methods.

**Parent Topic:**[UIB API reference](../../../../../build/applications/concept/api-uib.md)

## api - api.context.props.&lt;page\_property\_name&gt;

Page properties can be configured within UI Builder. The configuration values depend on the context in which the page is used.

<table id="table_pnc_bkb_n4b"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;page\_property\_name&gt;

</td><td>

Any

</td><td>

Available values are dependant on the client script implementation.To access these properties, use the following: `api.context.props.<page_property_name>`.

 For example:

```
`// A record page with property table could be accessed with
function isActivityStreamVisible({api}) {
  return api.context.props.table === 'incident';
} `
```

 **Note:** These property values are read-only. Mutating nested object values from scripts is not supported.

</td></tr></tbody>
</table>## api - api.context.session.&lt;session\_property&gt;

Context session properties associated with the current user.

<table id="table_e24_hkc_n4b"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

isLoggedIn

</td><td>

Boolean

</td><td>

Flag that indicates whether the current user is logged in to the system.Possible values:

-   true: Current user is logged in to
-   false: Current user is not logged in.

</td></tr><tr><td>

properties.awaEnabled

</td><td>

String

</td><td>

The system property glide.awa.enabled that indicates whether the auto assignment for work items for Advanced Work Assignment \(AWA\) is enabled for the current user.Possible values:

-   true: AWA is enabled for the user.
-   false: AWA is not enabled for the user.

 For additional information, see [Components installed with Advanced Work Assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/installed-with-awa.md).

</td></tr><tr><td>

properties.forgetMe.value

</td><td>

String

</td><td>

The property glide.ui.forgetme that indicates whether to remove the **Remember Me** check box from the login page to prevent login information from being cached.Possible values:

-   true: Remove the **Remember Me** check box.
-   false: Display the **Remember Me** check box.

 For additional information, see [Remove remember me](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-remove-remember-me.md).

</td></tr><tr><td>

properties.sessionTimeLeft.value

</td><td>

StringNumber coerced to string

</td><td>

The system property glide.ui.session\_timeleft that determines the mount of time left before the current session times out. Use this property to prompt the user to extent the current session before it times out.Unit: Minutes

</td></tr><tr><td>

properties.sessionTimeout.value

</td><td>

StringNumber coerced to string

</td><td>

The system property glide.ui.session\_timeout that determines the initial session time out value.Unit: Minutes - Values greater than 1440 minutes are treated as one day.

 For additional information, see [Session activity timeout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-session-activity-timeout.md)

</td></tr><tr><td>

properties.trackingEnabled.value

</td><td>

String

</td><td>

The system property glide.uxbuilder.tracking.enabled that indicates whether to enable/disable web analytics library loading and instantiation for UI Builder based applications.Possible values:

-   true: Enabled for the user.
-   false: Disabled for the user.

</td></tr><tr><td>

user.avatar

</td><td>

String

</td><td>

URL of the current user's avatar.

</td></tr><tr><td>

user.dateFormat

</td><td>

String

</td><td>

Default date format.

</td></tr><tr><td>

user.domain

</td><td>

String

</td><td>

Domain path for the current user.

</td></tr><tr><td>

user.firstName

</td><td>

String

</td><td>

First name of the current user.

</td></tr><tr><td>

user.fullName

</td><td>

String

</td><td>

First and last name of the current user.

</td></tr><tr><td>

user.initials

</td><td>

String

</td><td>

Initials of the current user.

</td></tr><tr><td>

user.language

</td><td>

String

</td><td>

Primary language spoken by the current user.

</td></tr><tr><td>

user.preferences

</td><td>

Array of objects

</td><td>

Name-value pairs that describe the user preferences. These user preferences are stored as records in the User Preference \[sys\_user\_preference\] table, and are updated each time the user changes their settings.For additional information, see [Exploring user administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/exploring-user-administration.md).

</td></tr><tr><td>

user.roles

</td><td>

Array

</td><td>

Comma-separated list of roles assigned to the current user.**Note:** If the user has no roles assigned, this context session property returns null rather than an empty array.

</td></tr><tr><td>

user.sys\_id

</td><td>

String

</td><td>

Sys\_id of the user in the User \[sys\_user\] table.

</td></tr><tr><td>

user.timeFormat

</td><td>

String

</td><td>

Default time format to use for the user.

</td></tr><tr><td>

user.timeZone

</td><td>

String

</td><td>

Time zone of the current user.

</td></tr><tr><td>

user.timeZoneOffset

</td><td>

String

</td><td>

Time zone offset of the current user.

</td></tr></tbody>
</table>## api - api.data.&lt;data\_resource\_id&gt;.lifecycle.lastFetchSucceeded

Boolean flag that indicates whether the last fetch attempt for the specified data resource instance finished successfully.

If the value is true, the last fetch attempt for the data resource instance finished successfully; otherwise, false.

<table id="table_svj_czb_n4b"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data\_resource\_id

</td><td>

String

</td><td id="data_resource_id-entry-api">

Unique identifier of the associated data resource. In most cases, you can use the Form Controller CTRL\_RECORD\#SAVE\_FORM action. If the record page has the Record Page Tabs component, the data resource for this method must be based off of GlideForm \(g\_form\).

The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.

</td></tr></tbody>
</table>## api - api.data.&lt;data\_resource\_id&gt;.addErrorMessage\(Object payload\)

Displays the specified error message at the top of the current form.

<table id="table_pct_ffd_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data\_resource\_id

</td><td>

String

</td><td id="data_resource_id-entry-api">

Unique identifier of the associated data resource. In most cases, you can use the Form Controller CTRL\_RECORD\#SAVE\_FORM action. If the record page has the Record Page Tabs component, the data resource for this method must be based off of GlideForm \(g\_form\).

The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.

</td></tr><tr><td>

payload

</td><td>

Object

</td><td>

Object that describes the error message to display.```
"payload": {
  "message": "String"
}
```

</td></tr><tr><td>

payload.message

</td><td>

String

</td><td>

Error message to display.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
api.data.gform.addErrorMessage({message: 'Error message'});
```

## api -api.data.&lt;data\_resource\_id&gt;.addInfoMessage\(Object payload\)

Displays the specified informational message at the top of the current form.

<table id="table_pqr_wdd_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data\_resource\_id

</td><td>

String

</td><td id="data_resource_id-entry-api">

Unique identifier of the associated data resource. In most cases, you can use the Form Controller CTRL\_RECORD\#SAVE\_FORM action. If the record page has the Record Page Tabs component, the data resource for this method must be based off of GlideForm \(g\_form\).

The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.

</td></tr><tr><td>

payload

</td><td>

Object

</td><td>

Object that describes the informational message to display.```
"payload": {
  "message": "String"
}
```

</td></tr><tr><td>

payload.message

</td><td>

String

</td><td>

Informational message to display.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
api.data.gform.addInfoMessage({message: 'Test message'});
```

## api - api.data.&lt;data\_resource\_id&gt;.addOption\(Object payload\)

Adds an option to the specified choice type field.

<table id="table_okr_21j_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data\_resource\_id

</td><td>

String

</td><td id="data_resource_id-entry-api">

Unique identifier of the associated data resource. In most cases, you can use the Form Controller CTRL\_RECORD\#SAVE\_FORM action. If the record page has the Record Page Tabs component, the data resource for this method must be based off of GlideForm \(g\_form\).

The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.

</td></tr><tr><td>

payload

</td><td>

Object

</td><td>

Object that describes the field value to update.```
"payload": {
  "choiceIndex": "String",
  "choiceLabel": "String",
  "choiceValue": "String",
  "fieldName": "String"
}
```

</td></tr><tr><td>

payload.choiceIndex

</td><td>

String

</td><td>

Optional. Index into the choice list at which to insert the option.Default: End of the choice list.

</td></tr><tr><td>

payload.choiceLabel

</td><td>

String

</td><td>

Label of the option to add to the specified field.

</td></tr><tr><td>

payload.choiceValue

</td><td>

String

</td><td>

Value of the option to add to the specified field.

</td></tr><tr><td>

payload.fieldName

</td><td>

String

</td><td>

Name of the choice type form field to add the specified option to.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
api.data.gform.addOption({fieldName: 'priority', choiceLabel: 'Extremely High', choiceValue: '10'});
```

## api - api.data.&lt;data\_resource\_id&gt;.addWarningMessage\(Object payload\)

Displays the specified warning message at the top of the current form.

<table id="table_mgf_v2d_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data\_resource\_id

</td><td>

String

</td><td id="data_resource_id-entry-api">

Unique identifier of the associated data resource. In most cases, you can use the Form Controller CTRL\_RECORD\#SAVE\_FORM action. If the record page has the Record Page Tabs component, the data resource for this method must be based off of GlideForm \(g\_form\).

The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.

</td></tr><tr><td>

payload

</td><td>

Object

</td><td>

Object that describes the warning message to display.```
"payload": {
  "message": "String"
}
```

</td></tr><tr><td>

payload.message

</td><td>

String

</td><td>

Warning message to display.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
api.data.gform.addWarningMessage({message: 'Test message'});
```

## api - api.data.&lt;data\_resource\_id&gt;.clearMessage\(\)

Removes all informational and error messages from the top of the current form.

<table id="table_g4t_qfd_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data\_resource\_id

</td><td>

String

</td><td id="data_resource_id-entry-api">

Unique identifier of the associated data resource. In most cases, you can use the Form Controller CTRL\_RECORD\#SAVE\_FORM action. If the record page has the Record Page Tabs component, the data resource for this method must be based off of GlideForm \(g\_form\).

The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
api.data.gform.clearMessage();
```

## api - api.data.&lt;data\_resource\_id&gt;.clearOptions\(Object payload\)

Clears all options from the specified choice type field.

<table id="table_c3x_4dj_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data\_resource\_id

</td><td>

String

</td><td id="data_resource_id-entry-api">

Unique identifier of the associated data resource. In most cases, you can use the Form Controller CTRL\_RECORD\#SAVE\_FORM action. If the record page has the Record Page Tabs component, the data resource for this method must be based off of GlideForm \(g\_form\).

The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.

</td></tr><tr><td>

payload

</td><td>

Object

</td><td>

Object that describes the choice type field whose options are to be cleared.```
"payload": {
  "fieldName": "String"
}
```

</td></tr><tr><td>

payload.fieldName

</td><td>

String

</td><td>

Name of the choice type field whose options are to be cleared.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
api.data.gform.clearOptions({fieldName: 'priority'});
```

## api - api.data.&lt;data\_resource\_id&gt;.executeUiAction\(Object payload\)

Executes the specified UI action.

<table id="table_l41_s2j_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data\_resource\_id

</td><td>

String

</td><td id="data_resource_id-entry-api">

Unique identifier of the associated data resource. In most cases, you can use the Form Controller CTRL\_RECORD\#SAVE\_FORM action. If the record page has the Record Page Tabs component, the data resource for this method must be based off of GlideForm \(g\_form\).

The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.

</td></tr><tr><td>

payload

</td><td>

Object

</td><td>

Description of the UI action to execute.```
"payload": {
  "actionSysId": "String"
}
```

</td></tr><tr><td>

payload.actionSysId

</td><td>

String

</td><td>

Sys\_id of the UI action to execute. Table: UI Action \[sys\_ui\_action\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
api.data.gform.executeUiAction({actionSysId: '60615ff90f730010ac7de6f8c4767e9a'});
```

## api - api.data.&lt;data\_resource\_id&gt;.execute\(Object inputValues\)

Triggers an execute operation on the specified data resource.

This method is only available if the data resource is one of the following types:

-   Composite
-   GraphQL
-   REST
-   Scriptlet
-   Transform

**Note:** This method is only exposed if the **mutates\_server\_data** field is set to `true` on the corresponding data resource \(sys\_ux\_data\_broker\_\* table\) record. It is accessible under api.data.&lt;data\_resource\_Id&gt;.refresh\(\).

|Name|Type|Description|
|----|----|-----------|
|data\_resource\_id|String|Unique identifier of the associated data resource. The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.|
|inputValues|Object|Object to pass to the specified data resource. This object must conform to the data resource's input parameters.|

|Type|Description|
|----|-----------|
|None| |

This code example shows a page script that is invoked when the **Submit** button on the page is clicked. The page is configured wit a Server Data Resource tat creates a new record.

```
function handler({api}) {
  if (api.state.movieYear === 2020) {
    // The data resource used in this case specifies two input parameters: name and year
    api.data.create_movie_record.execute({
      name: api.state.movieName,
      year: api.state.movieYear
    });
  }
}
```

## api - api.data.&lt;data\_resource\_id&gt;.hideFieldMessage\(Object payload\)

Hides the oldest message next to the specified field or clears all messages associated with the field.

<table id="table_jl3_b33_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data\_resource\_id

</td><td>

String

</td><td id="data_resource_id-entry-api">

Unique identifier of the associated data resource. In most cases, you can use the Form Controller CTRL\_RECORD\#SAVE\_FORM action. If the record page has the Record Page Tabs component, the data resource for this method must be based off of GlideForm \(g\_form\).

The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.

</td></tr><tr><td>

payload

</td><td>

Object

</td><td>

Object that describes the field message to hide.```
"payload": {
  "clearAll": Boolean,
  "fieldName": "String"
}
```

</td></tr><tr><td>

payload.clearAll

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to clear all messages associated with the specified form field.Valid values:

-   true: Clear all messages associated with the specified field.
-   false: Do not clear all messages associated with the specified field.

 Default: false

</td></tr><tr><td>

payload.fieldName

</td><td>

String

</td><td>

Name of the form field for which to hide the oldest message or clear all associated messages.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
api.data.gform.hideFieldMessage({fieldName: 'short_description'});
```

## api - api.data.&lt;data\_resource\_id&gt;.hideRelatedList\(Object payload\)

Hides the specified related list on the current form.

<table id="table_yxg_jq3_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data\_resource\_id

</td><td>

String

</td><td id="data_resource_id-entry-api">

Unique identifier of the associated data resource. In most cases, you can use the Form Controller CTRL\_RECORD\#SAVE\_FORM action. If the record page has the Record Page Tabs component, the data resource for this method must be based off of GlideForm \(g\_form\).

The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.

</td></tr><tr><td>

payload

</td><td>

Object

</td><td>

Object that describes the related list to hide.```
"payload": {
  "listTableName ": "String"
}
```

</td></tr><tr><td>

payload.listTableName

</td><td>

String

</td><td>

Name of the related list to hide. If the list to hide is through a relationship, provide the sys\_id of the list instead of the name.Table: Related List \[sys\_ui\_related\_list\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
api.data.gform.hideRelatedList({listTableName:'incident.parent_incident'});
```

## api - api.data.&lt;data\_resource\_id&gt;.hideRelatedLists\(\)

Hides all related lists on the current form.

<table id="table_cy4_cm3_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data\_resource\_id

</td><td>

String

</td><td id="data_resource_id-entry-api">

Unique identifier of the associated data resource. In most cases, you can use the Form Controller CTRL\_RECORD\#SAVE\_FORM action. If the record page has the Record Page Tabs component, the data resource for this method must be based off of GlideForm \(g\_form\).

The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
api.data.gform.hideRelatedLists();
```

## api - api.data.&lt;data\_resource\_id&gt;.refresh\(\)

Triggers a refresh operation for the specified non-mutating data resource instance.

Call this method if the underlying data being fetched by the data resource changes. A data resource is considered non-mutating if the **mutates\_server\_data** field on the record is set to false.

This method is asynchronous and emits an internal event to trigger the refresh of the specified data resource instance. The UI Builder allows you to trigger client scripts in response to data resource lifecycle events, such as DATA\_FETCH\_SUCCEEDED and DATA\_FETCH\_FAILED. For additional information on these events, see [Event mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/event-mapping.md).

This method is only available if the data resource is one of the following types:

-   Composite
-   GraphQL
-   REST
-   Scriptlet
-   Transform

**Note:** This method is only exposed if the **mutates\_server\_data** field is set to `false` on the corresponding data resource \(sys\_ux\_data\_broker\_\* table\) record.

|Name|Type|Description|
|----|----|-----------|
|data\_resource\_id|String|Unique identifier of the associated data resource. The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.|

|Type|Description|
|----|-----------|
|None| |

This code example shows a page script that is invoked when a dropdown item is selected in a page. The page is configured with two Server Data Resources that query problem and incident tables.

```
function handler({api, event}) {
  const value = event.payload.value[0];
  if (value === 'problem')
    api.data.problem_list_1.refresh();
  else if(value === 'incident')
    api.data.incident_list_1.refresh();
}
```

## api - api.data.&lt;data\_resource\_id&gt;.reload\(\)

Reloads the current form using the same table and sys\_id.

<table id="table_cwc_kw3_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data\_resource\_id

</td><td>

String

</td><td id="data_resource_id-entry-api">

Unique identifier of the associated data resource. In most cases, you can use the Form Controller CTRL\_RECORD\#SAVE\_FORM action. If the record page has the Record Page Tabs component, the data resource for this method must be based off of GlideForm \(g\_form\).

The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
api.data.gform.reload();
```

## api - api.data.&lt;data\_resource\_id&gt;.removeOption\(Object payload\)

Removes an option from the specified choice type field.

<table id="table_gky_wcj_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data\_resource\_id

</td><td>

String

</td><td id="data_resource_id-entry-api">

Unique identifier of the associated data resource. In most cases, you can use the Form Controller CTRL\_RECORD\#SAVE\_FORM action. If the record page has the Record Page Tabs component, the data resource for this method must be based off of GlideForm \(g\_form\).

The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.

</td></tr><tr><td>

payload

</td><td>

Object

</td><td>

Object that describes the choice type field to update.```
"payload": {
  "choiceValue": "String",
  "fieldName": "String"
}
```

</td></tr><tr><td>

payload.choiceValue

</td><td>

String

</td><td>

Value of the option to remove from the specified choice type field.

</td></tr><tr><td>

payload.fieldName

</td><td>

String

</td><td>

Name of the choice type form field from which to remove the specified value.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
api.data.gform.removeOption({fieldName: 'priority', choiceValue: '1'});
```

## api - api.data.&lt;data\_resource\_id&gt;.save\(\)

Triggers form submission using the Save UI action.

<table id="table_fn1_vw3_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data\_resource\_id

</td><td>

String

</td><td id="data_resource_id-entry-api">

Unique identifier of the associated data resource. In most cases, you can use the Form Controller CTRL\_RECORD\#SAVE\_FORM action. If the record page has the Record Page Tabs component, the data resource for this method must be based off of GlideForm \(g\_form\).

The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
api.data.gform.save();
```

## api - api.data.&lt;data\_resource\_id&gt;.setMandatory\(Object payload\)

Sets whether the specified form field is mandatory.

<table id="table_yws_2v3_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data\_resource\_id

</td><td>

String

</td><td id="data_resource_id-entry-api">

Unique identifier of the associated data resource. In most cases, you can use the Form Controller CTRL\_RECORD\#SAVE\_FORM action. If the record page has the Record Page Tabs component, the data resource for this method must be based off of GlideForm \(g\_form\).

The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.

</td></tr><tr><td>

payload

</td><td>

Object

</td><td>

Object that describes the field whose mandatory information to update.```
"payload": {
  "fieldName": "String",
  "mandatory": Boolean
}
```

</td></tr><tr><td>

payload.fieldName

</td><td>

String

</td><td>

Name of the form field whose mandatory value is to be set.

</td></tr><tr><td>

payload.mandatory

</td><td>

Boolean

</td><td>

Flag that indicates the specified form field is mandatory, meaning the form cannot be saved without this field containing a valid value.Valid values:

-   true: Field is mandatory.
-   false: Field is optional.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
api.data.gform.setMandatory({fieldName: 'short_description', mandatory: false});
```

## api - api.data.&lt;data\_resource\_id&gt;.setReadOnly\(Object payload\)

Sets the read/write capabilities of the specified form field.

<table id="table_d13_ps3_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data\_resource\_id

</td><td>

String

</td><td id="data_resource_id-entry-api">

Unique identifier of the associated data resource. In most cases, you can use the Form Controller CTRL\_RECORD\#SAVE\_FORM action. If the record page has the Record Page Tabs component, the data resource for this method must be based off of GlideForm \(g\_form\).

The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.

</td></tr><tr><td>

payload

</td><td>

Object

</td><td>

Object that describes the field whose readability information to update.```
"payload": {
  "fieldName": "String",
  "readonly": Boolean
}
```

</td></tr><tr><td>

payload.fieldName

</td><td>

String

</td><td>

Name of the form field whose readability is to be set.

</td></tr><tr><td>

payload.readonly

</td><td>

Boolean

</td><td>

Flag that indicates the read/write capabilities of the specified form field.Valid values:

-   true: Field is read only.
-   false: Field is read/write.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
api.data.gform.setReadOnly({fieldName: 'short_description', readonly: false});
```

## api -api.data.&lt;data\_resource\_id&gt;.setValue\(Object payload\)

Updates a specified GlideForm field with the specified value. Optionally, you can also update the display value with the same specified value.

Only the value on the form is updated. The value is not saved in the database.

<table id="table_tyh_31d_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data\_resource\_id

</td><td>

String

</td><td id="data_resource_id-entry-api">

Unique identifier of the associated data resource. In most cases, you can use the Form Controller CTRL\_RECORD\#SAVE\_FORM action. If the record page has the Record Page Tabs component, the data resource for this method must be based off of GlideForm \(g\_form\).

The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.

</td></tr><tr><td>

payload

</td><td>

Object

</td><td>

Object that describes the field whose value to update.```
"payload": {
  "displayValue": "String",
  "fieldName": "String",
  "value": "String"
}
```

</td></tr><tr><td>

payload.displayValue

</td><td>

String

</td><td>

Optional. Name of the display value to update. If left blank, the display value is not modified.

</td></tr><tr><td>

payload.fieldName

</td><td>

String

</td><td>

Name of the form field to update.

</td></tr><tr><td>

payload.value

</td><td>

String

</td><td>

Value to update the field with.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
api.data.gform.setValue({fieldName: 'short_description', value: 'short description'});
```

## api - api.data.&lt;data\_resource\_id&gt;.setVisible\(Object payload\)

Sets the visibility of the specified form field.

<table id="table_j5k_gr3_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data\_resource\_id

</td><td>

String

</td><td id="data_resource_id-entry-api">

Unique identifier of the associated data resource. In most cases, you can use the Form Controller CTRL\_RECORD\#SAVE\_FORM action. If the record page has the Record Page Tabs component, the data resource for this method must be based off of GlideForm \(g\_form\).

The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.

</td></tr><tr><td>

payload

</td><td>

Object

</td><td>

Object that describes the field on which to set visibility.```
"payload": {
  "fieldName": "String",
  "visibility": Boolean
}
```

</td></tr><tr><td>

payload.fieldName

</td><td>

String

</td><td>

Name of the form field whose visibility is to be set.

</td></tr><tr><td>

payload.visibility

</td><td>

Boolean

</td><td>

Flag that indicates whether the associated field is visible on the current form.Valid values:

-   true: Field will display on the form.
-   false: Field will not display on the form.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
api.data.gform.setVisible({fieldName: 'short_description', visibility: false});
```

## api - api.data.&lt;data\_resource\_id&gt;.showFieldMessage\(Object payload\)

Displays the specified message next to the specified field.

<table id="table_o35_xgd_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data\_resource\_id

</td><td>

String

</td><td id="data_resource_id-entry-api">

Unique identifier of the associated data resource. In most cases, you can use the Form Controller CTRL\_RECORD\#SAVE\_FORM action. If the record page has the Record Page Tabs component, the data resource for this method must be based off of GlideForm \(g\_form\).

The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.

</td></tr><tr><td>

payload

</td><td>

Object

</td><td>

Object that describes the field message to display.```
"payload": {
  "fieldName": "String",
  "message": "String",
  "type": "String"
```

</td></tr><tr><td>

payload.fieldName

</td><td>

String

</td><td>

Name of the field next to which the message should appear.

</td></tr><tr><td>

payload.message

</td><td>

String

</td><td>

Message to display.

</td></tr><tr><td>

payload.type

</td><td>

String

</td><td>

Optional. Type of message to display.Valid values:

-   error
-   info
-   warning

 Default: info

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
api.data.gform.showFieldMessage({fieldName: 'short_description', message: 'Error message', type: 'error'});
```

## api - api.data.&lt;data\_resource\_id&gt;.showRelatedList\(Object payload\)

Displays the specified related list on the current form.

<table id="table_xc2_tn3_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data\_resource\_id

</td><td>

String

</td><td id="data_resource_id-entry-api">

Unique identifier of the associated data resource. In most cases, you can use the Form Controller CTRL\_RECORD\#SAVE\_FORM action. If the record page has the Record Page Tabs component, the data resource for this method must be based off of GlideForm \(g\_form\).

The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.

</td></tr><tr><td>

payload

</td><td>

Object

</td><td>

Object that describes the related list to display.```
"payload": {
  "listTableName ": "String"
}
```

</td></tr><tr><td>

payload.listTableName

</td><td>

String

</td><td>

Name of the related list to display. If the list to display is through a relationship, provide the sys\_id of the list instead of the name.Table: Related List \[sys\_ui\_related\_list\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
api.data.gform.showRelatedList({listTableName:'incident.parent_incident'});
```

## api - api.data.&lt;data\_resource\_id&gt;.showRelatedLists\(\)

Displays all related lists associated with the current form.

<table id="table_wzd_sl3_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data\_resource\_id

</td><td>

String

</td><td id="data_resource_id-entry-api">

Unique identifier of the associated data resource. In most cases, you can use the Form Controller CTRL\_RECORD\#SAVE\_FORM action. If the record page has the Record Page Tabs component, the data resource for this method must be based off of GlideForm \(g\_form\).

The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
api.data.gform.showRelatedLists();
```

## api - api.data.&lt;data\_resource\_id&gt;.submit\(\)

Triggers form submission using the specified UI action.

<table id="table_zc1_hx3_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data\_resource\_id

</td><td>

String

</td><td id="data_resource_id-entry-api">

Unique identifier of the associated data resource. In most cases, you can use the Form Controller CTRL\_RECORD\#SAVE\_FORM action. If the record page has the Record Page Tabs component, the data resource for this method must be based off of GlideForm \(g\_form\).

The available data resource instances are configuration-dependent and defined when you add the data resource to your page in UI Builder.

</td></tr><tr><td>

payload

</td><td>

Object

</td><td>

Object that describes the UI action to use to submit the current form.```
"payload": {
  "submitActionName": "String"
}
```

</td></tr><tr><td>

payload.submitActionName

</td><td>

String

</td><td>

Name of the UI action to execute to submit the current form.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
api.data.gform.submit({submitActionName:'sysverb_ws_save'});
```

## api - api.emit\(String eventName, Object payload\)

Emits an event with the specified name and payload.

The event name being emitted must be part of the associated page definition's dispatched events list, which is stored in the UX Macroponent Definition \[sys\_ux\_macroponent\] table. Any api.emit call that dispatches events not declared in this table are ignored.

For additional information on events, see [Work with events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/work-events.md).

<table id="table_yyz_njj_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

eventName

</td><td>

String

</td><td>

Name of the event to emit. This name should follow the UI Framework action naming guidelines:-   Should be upper snake case, such as ITEM\_CHANGED. All letters in upper case and all spaces replaced with underscores.
-   Should be past tense, such as BUTTON\_CLICKED or USER\_SELECTED.

 For additional information on these action naming guidelines, see [https://developer.servicenow.com/dev.do\#!/reference/now-experience/sandiego/ui-framework/main-concepts/dispatching-actions](https://developer.servicenow.com/dev.do#!/reference/now-experience/sandiego/ui-framework/main-concepts/dispatching-actions).

</td></tr><tr><td>

payload

</td><td>

Object

</td><td>

Optional. Object that contains the data to send with the emitted event. This object is free-form and can contain whatever data is necessary by the entity receiving the data.**Note:** Payloads of primitive type work, but could result in inconsistent behavior.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows emitting an event called **NOW\_UXF\_PAGE\#ADD\_NOTIFICATIONS** with an associated **items** payload.

```
function handler({api}) { 
  api.emit('NOW_UXF_PAGE#ADD_NOTIFICATIONS', { 
    items: [
      { 
        id: 'alert1', 
        status: 'positive', 
        icon: 'check-circle-outline', 
        content: 'Here is some information!', 
        textLinkProps: { 
          label: 'More info',
          href: 'https://www.servicenow.com' 
        }, 
      action: {type: 'acknowledge'} 
      } 
    ] 
  }); 
} 
```

## api - setState\(String stateParam, Any value\)

Sets the value of the specified client state parameter.

Use client state parameters to maintain a shared state on a page. The shared state can then be passed as values to properties of components used on the page. You can also access and update client states in multiple page scripts. A common use case is to keep track of values input by users in multiple form controls on a page. When the form is submitted, a client script could then use all of the values stored in client state parameters to create a new record with a data broker. A page can have one or more client state parameters, which you can declare for a page through the UI Builder. You can then bind a client state parameter to one or more components to share or act on the client state parameter.

api.setState\(\) calls are executed asynchronously and do not necessarily update the UI immediately. If the value to set depends on the **currentValue** of the client state parameter, or any of the properties provided in the api object, you should use this variant of the api.setState\(\) method to avoid using outdated values.

<table id="table_lgw_35q_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

stateParm

</td><td>

String

</td><td id="stateParm-entry-api">

Name of the client state parameter to update. This name must be declared in the client state parameters of the associated page. For additional information on declaring client state parameters, see [Work with client state parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/state-parameters.md).

</td></tr><tr><td>

value

</td><td>

Any - Must be the same as the client state parameter declaration.

</td><td>

Value to set the specified client state parameter to.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example shows a script that could be executed to update the email client state parameter when an input value is set on a now-input component.

```
function handler({api, event}) {
    api.setState('email', event.payload.value);
}
```

## api - setState\(String stateParam, Function callbackFn\)

Sets the value of the specified client state parameter to the value returned by the specified callback function.

The callback function is invoked with an object that has two properties: **currentValue** and **api**. The function should never mutate the **currentValue** property or the **api** object directly.

Use client state parameters to maintain a shared state on a page. The shared state can then be passed as values to properties of components used on the page. You can also access and update client states in multiple page scripts. A common use case is to keep track of values input by users in multiple form controls on a page. When the form is submitted, a client script could then use all of the values stored in client state parameters to create a new record with a data broker. A page can have one or more client state parameters, which you can declare for a page through the UI Builder. You can then bind a client state parameter to one or more components to share or act on the client state parameter.

api.setState\(\) calls are executed asynchronously and do not necessarily update the UI immediately. If the value to set depends on the **currentValue** of the client state parameter, or any of the properties provided in the api object, you should use this variant of the api.setState\(\) method to avoid using outdated values.

<table id="table_vlt_gyq_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

stateParm

</td><td>

String

</td><td id="stateParm-entry-api">

Name of the client state parameter to update. This name must be declared in the client state parameters of the associated page. For additional information on declaring client state parameters, see [Work with client state parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/state-parameters.md).

</td></tr><tr><td>

callbackFn

</td><td>

Function

</td><td>

Callback function to execute to obtain the value.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example shows how to use api.setState to log users into a page.

```
function handler({api, event}) {
  const {name, value} = event.payload;
  if (name === 'username' || name === 'password') {
    // Update the loginParameters state object with the username/password value
    api.setState('loginParameters', ({currentValue}) => {
      return {
        ...currentValue,
        [name]: value
      };
    });
  }
}
```

## api - api.state.&lt;client\_state\_parameter\_name&gt;

Current value of the specified client state parameter.

<table id="table_yk3_rmb_n4b"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;client\_state\_parameter\_name&gt;

</td><td>

Any. The available client state parameters are dependent on the page configuration.

</td><td>

Name of the client state parameter. Available client states are dependant on the client script implementation.To access the available client states, use the following: `api.state.<client_state_name>`.

 For example:

```
function showRelatedLists({api}) { 
  return !api.state.isCustomListSelected; 
} 
```

 **Note:** These property values are read-only. To update a client state parameter, use [api.setState\(\)](apiAPI.md#). Mutating nested object values from scripts is not supported.

</td></tr></tbody>
</table>