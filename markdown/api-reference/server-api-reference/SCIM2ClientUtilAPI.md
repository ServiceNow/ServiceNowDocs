---
title: SCIM2ClientUtil - Scoped
description: The SCIM2ClientUtil API provides utility methods to obtain the unique identifiers of external provider systems and then use that information when calling the SCIM2Client API.Returns the unique identifier of a specified resource from a specified external provider system for a unique resource ID in a ServiceNow instance using a filter expression to describe the desired resource.Returns the unique identifier of a specified resource from a specified external provider system for a unique resource ID in a ServiceNow instance.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SCIM2ClientUtil- Scoped

The SCIM2ClientUtil API provides utility methods to obtain the unique identifiers of external provider systems and then use that information when calling the SCIM2Client API.

This API runs in the `sn_auth` namespace and requires the SCIM v2 - ServiceNow Cross-domain Identity Management Client \(com.snc.integration.scim2.client\) plugin to be installed to access the API.

For additional information on SCIM, see [System for Cross-domain Identity Management \(SCIM\)](https://www.servicenow.com/docs/access?context=scim&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SCIM2ClientUtil - getProviderIdByFilter\(String provider, String resourceName, String filter\)

Returns the unique identifier of a specified resource from a specified external provider system for a unique resource ID in a ServiceNow instance using a filter expression to describe the desired resource.

This API is useful when mapping ServiceNow fields to SCIM fields where the resource identifier in the external provider system is needed. Before calling this method, a unique field must be defined for the resource in the system attribute map, located in the SCIM Provider Resource Mapping \[sys\_scim\_provider\_resource\_mapping \] table.

For additional information on provider resource mapping, see [Create a SCIM Provider Resource Mapping](https://www.servicenow.com/docs/access?context=scim-provider-resource-mapping&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

<table id="table_j21_ks5_ctb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

provider

</td><td>

String

</td><td>

Name of the configured SCIM service provider. Table: In the name field of the SCIM Provider \[sys\_scim\_provider\] table.

</td></tr><tr><td>

resourceName

</td><td>

String

</td><td>

Name of the resource type, such as User or Group.Table: In the resource\_name field of the SCIM Provider Resource Mapping \[sys\_scim\_provider\_resource\_mapping\] table.

</td></tr><tr><td>

filter

</td><td>

String

</td><td>

Filter expression to apply to the return results.For additional information on the available filter parameters and their associated format, refer to the following section in the Internet Engineering Task Force document: System for Cross-domain Identity Management: Protocol

[https://datatracker.ietf.org/doc/html/rfc7644\#section-3.4.2.2](https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2.2)

</td></tr></tbody>
</table><table id="table_k21_ks5_ctb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Unique resource identifier used by the external service provider.Throws an exception if there is any problem while fetching the information.

</td></tr></tbody>
</table>The following example shows how to obtain the resource identifier of the user using the filter `'username eq "abel.tuter"'`.

```
var response = sn_auth.SCIM2ClientUtil.getProviderIdByFilter('SNOW Provider','User','username eq "abel.tuter"'); 
gs.info('response: ' + response);
```

Output:

```

 "005d500b536073005e0addeeff7b12f4"

```

The following example shows how to use a script to obtain the resource identifier of the manager using the filter `'userName eq "' + manager + '"'`.

```
(function getValue(resourceGR) {
  try {
    var manager = resourceGR.manager.user_name;
    return sn_auth.SCIM2ClientUtil.getProviderIdByFilter('SCIM Provider Demo', 'User', 'userName eq "' + manager + '"');
  } catch (e) {
    gs.error('Unable to get attribute value using script' + e);
    // Handle failure scenario here
  }
})(resourceGR);
```

Output:

```

  "125d500b535973005e0addeeff8c12a2"
```

## SCIM2ClientUtil - getProviderIdByResourceId\(String provider, String resourceName, String resourceId\)

Returns the unique identifier of a specified resource from a specified external provider system for a unique resource ID in a ServiceNow instance.

This API is useful when mapping ServiceNow fields to SCIM fields where the resource identifier in the external provider system is needed. Before calling this method, a unique field must be defined for the resource in the system attribute map, located in the SCIM Provider Resource Mapping \[sys\_scim\_provider\_resource\_mapping\] table.

For additional information on provider resource mapping, see [Create a SCIM Provider Resource Mapping](https://www.servicenow.com/docs/access?context=scim-provider-resource-mapping&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

<table id="table_rks_rd5_ctb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

provider

</td><td>

String

</td><td>

Name of the configured SCIM service provider. Table: In the name field of the SCIM Provider \[sys\_scim\_provider\] table.

</td></tr><tr><td>

resourceName

</td><td>

String

</td><td>

Name of the resource type, such as User or Group.Table: In the resource\_name field of the SCIM Provider Resource Mapping \[sys\_scim\_provider\_resource\_mapping\] table.

</td></tr><tr><td>

resourceId

</td><td>

String

</td><td>

Sys\_id of the resource saved in the ServiceNow instance \(the client\).Table: In the primary\_table field of the SCIM Provider Resource Mapping \[sys\_scim\_provider\_resource\_mapping\] table.

</td></tr></tbody>
</table><table id="table_sks_rd5_ctb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Unique resource identifier used by the external service provider.Throws an exception if there is any problem while fetching the information.

</td></tr></tbody>
</table>The following example shows how to obtain the resource identifier of the user with the sys\_id f282abf03710200044e0bfc8bcbe5d12.

```
var response = sn_auth.SCIM2ClientUtil.getProviderIdByResourceId('SNOW Provider','User','f282abf03710200044e0bfc8bcbe5d12'); 
gs.info('response: ' + response);
```

Output:

```

  "005d500b536073005e0addeeff7b12f4"

```

