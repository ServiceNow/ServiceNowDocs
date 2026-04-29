---
title: GlideSecurityManager - Global
description: The GlideSecurityManager API provides methods that enable you to retrieve a SecurityManager object and to check if the current user has access rights, both table-level and field-level, to a specified GlideRecord table based on the configured Access Control Rules \(ACLs\).Returns a SecurityManager object.Indicates whether the current user has table-level access rights to a specified GlideRecord table based on the configured Access Control Rules \(ACLs\). This method evaluates all available ACLs for the specific resource.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideSecurityManager- Global

The GlideSecurityManager API provides methods that enable you to retrieve a SecurityManager object and to check if the current user has access rights, both table-level and field-level, to a specified GlideRecord table based on the configured Access Control Rules \(ACLs\).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideSecurityManager - get\(\)

Returns a SecurityManager object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|SecurityManager object.|

The following code example shows how to call the GlideSecurityManager.get\(\) method to obtain a GlideSecurityManager object that is then used by the GlideSecurityManager.hasRightsTo\(\) method.

```
var sm = GlideSecurityManager.get();
var grInc = new GlideRecord('incident');
var path = 'record/incident/read';

gs.info(sm.hasRightsTo(path, grInc));

```

Output:

```
true
```

## GlideSecurityManager - hasRightsTo\(String path\_to\_resource, Object context\)

Indicates whether the current user has table-level access rights to a specified GlideRecord table based on the configured Access Control Rules \(ACLs\). This method evaluates all available ACLs for the specific resource.

For additional information on ACLs, see [Access Controls Evaluation Order](https://developer.servicenow.com/dev.do#!/learn/learning-plans/yokohama/servicenow_application_developer/app_store_learnv2_securingapps_yokohama_access_controls_evaluation_order).

<table id="table_mvc_jxd_d2c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

path\_to\_resource

</td><td>

String

</td><td>

Resource path to the GlideRecord table to check for access rights.For example: `record/incident/read`

Format: &lt;type&gt;/&lt;name&gt;/&lt;operation&gt;

-   &lt;type&gt;: Type of resource. Valid values: Existing ACL types. Available from the drop-down choice list on the ACL form.
-   &lt;name&gt;: Name of the table to check.
-   &lt;operation&gt;: Name of the operation that you want to check access rights for. In this case "read".

</td></tr><tr><td>

context

</td><td>

Object

</td><td>

Optional. For table-level validation this field is not required.

</td></tr></tbody>
</table><table id="table_nvc_jxd_d2c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the user's roles permit table-level reading of the specified table.Valid values:

-   true: Specified access is permitted.
-   false: Specified access isn't permitted.

</td></tr></tbody>
</table>The following code example shows how to use the hasRightsTo\(\) method to check if the current user has table-level read rights to all records in the Incident \[incident\] table.

```
var sm = GlideSecurityManager.get();
var grInc = new GlideRecord('incident');
var path = 'record/incident/read';

gs.info(sm.hasRightsTo(path, grInc));

```

Output:

```
false
```

