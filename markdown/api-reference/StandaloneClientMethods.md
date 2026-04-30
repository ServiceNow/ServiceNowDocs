---
title: StandaloneClientMethods
description: Standalone client methods are methods that you can use within your client JavaScripts, such as reflistOpen, but aren't a part of any class or API.Shows the reference field data in a standard pop-up window. This method is commonly used when selecting a magnifying glass icon, beside any reference field, in UI 16 forms.
locale: en-US
release: yokohama
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# StandaloneClientMethods

Standalone client methods are methods that you can use within your client JavaScripts, such as reflistOpen, but aren't a part of any class or API.

You can directly access these methods within a client script without any constructor or other type of instantiation before use.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## Standalone - reflistOpen \(String target, String elementName, String refTableName, String dependent, String useQBE, String refQualElements, String additionalQual, String parentID, String forceReference, String ignoreTargetValue\)

Shows the reference field data in a standard pop-up window. This method is commonly used when selecting a magnifying glass icon, beside any reference field, in UI 16 forms.

For example, using this method you can display reference field data for a specific set of query criteria:

![Ref data in pop-up window](../image/reflistOpen_popup_image1.png)

Similarly, you can use this method to display a search form that enables the user to enter their own set of query criteria for selecting the reference field data to display.

![Search in pop-up window](../image/reflistOpen_popup_image2.png)

When opening the URL in the standard pop-up, if the URL length is greater than TinyURL length, 1024 by default, the URL is converted to TinyURL, such as:

`"sys_user_list.do?sysparm_tiny=7ea02c4ff8a8b510f877c74d78b60460"`.

**Note:**

reflistOpen\(\) isn’t supported in Workspace Client Script. Use the g\_modal.showFrame\(\) method instead.

<table id="table_sx2_hgs_nyb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

target

</td><td>

String

</td><td>

Form target reference field ID.For example, the `caller_id` parameter's target reference field ID is `incident.caller_id`.

</td></tr><tr><td>

elementName

</td><td>

String

</td><td>

Form reference field element name. For example: `caller_id`

</td></tr><tr><td>

refTableName

</td><td>

String

</td><td>

Reference table to map to the form reference field. For example, for the reference field `caller_id`, sys\_user is the reference table. In this case, you would pass the value `sys_user`.

</td></tr><tr><td>

dependent

</td><td>

String

</td><td>

Configured dependent field for the specified **target** element. For additional information, see [Make a field dependent](https://www.servicenow.com/docs/access?context=t_MakingAFieldDependent&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

useQBE

</td><td>

String

</td><td>

Flag that indicates the type of information to return in the pop-up window.Valid values:

-   true: Display a query form with a search button.
-   false: Display the query results.

Default: false

</td></tr><tr><td>

refQualElements

</td><td>

String

</td><td>

Configured reference qualifier for the specified **target** element. The function appends the specified reference qualifiers to the URL and only displays the filtered results in the pop-up window. If you don't want to include a reference qualifier, pass an empty string.For additional information on reference qualifiers, see [Reference qualifiers](https://www.servicenow.com/docs/access?context=c_ReferenceQualifiers&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

additionalQual

</td><td>

String

</td><td>

Optional. Additional qualifier query to use to filter the results that display in the pop-up window.For example, for a `caller_id` reference field in an incident, you could pass the user's sys\_id `sys_id=62826bf03710200044e0bfc8bcbe5df1`.

The function filters the User \[sys\_user\] table and shows the filtered results in the pop-up window.

</td></tr><tr><td>

parentID

</td><td>

String

</td><td>

Optional. Currently only an internal parameter, no need to pass a value.

</td></tr><tr><td>

forceReference

</td><td>

String

</td><td>

Optional. Currently only an internal parameter, no need to pass a value.

</td></tr><tr><td>

ignoreTargetValue

</td><td>

String

</td><td>

Optional. Currently only an internal parameter, no need to pass a value.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Pop-up window|Displays the returned reference field data in a standard pop-up window.|

The following example shows how to invoke this method to show the caller field data in the pop-up window for the incident table \(first image above\).

```
function onChange(control, oldValue, newValue, isLoading, isTemplate) {
   if (isLoading || newValue === '') {
      return;
   }

   reflistOpen('incident.caller_id', 'caller_id', 'sys_user','company', 'false', '');
}
```

The following example shows how to invoke this same client script, but with `useQBE = true`, which displays a search button and associated search criteria within the pop-up window \(second image above\).

```
function onChange(control, oldValue, newValue, isLoading, isTemplate) {
   if (isLoading || newValue === '') {
      return;
   }

   //  Type appropriate comment here, and begin script below
   reflistOpen('incident.caller_id', 'caller_id', 'sys_user','company', 'true', '');
}
```

