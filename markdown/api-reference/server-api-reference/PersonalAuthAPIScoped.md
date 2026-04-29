---
title: PersonalAuthAPI - Scoped
description: The PersonalAuthAPI provides methods that enable you to manage access/refresh tokens for personal authentication credentials.Instantiates a new PersonalAuthAPI object.Returns the OAuth initiator URL for the personal authentication credential associated with a specified alias.Checks whether a valid access/refresh token exists for the personal authorization credential associated with a specified alias.Revokes an existing access/refresh token for the personal authentication credential associated with a specified alias.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# PersonalAuthAPI- Scoped

The PersonalAuthAPI provides methods that enable you to manage access/refresh tokens for personal authentication credentials.

To access this API the Personal Authentication \(com.snc.sn\_ihub\_personal\_auth\) plugin must be activated. This API runs in the `sn_cc` namespace.

Before accessing this API, Personal Authentication must be configured on your instance. For additional information, see [Create a Connection &amp; Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=australia&pubname=australia-platform-security&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## PersonalAuthAPI - PersonalAuthAPI\(\)

Instantiates a new PersonalAuthAPI object.

|Name|Type|Description|
|----|----|-----------|
|None| ||

The following code example shows how to instantiate a PersonalAuthAPI object.

```
var personalAuthAPI = new sn_cc.PersonalAuthAPI();
```

## PersonalAuthAPI - getInitiatorURL\(String aliasId\)

Returns the OAuth initiator URL for the personal authentication credential associated with a specified alias.

<table id="table_fhk_4bl_3bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aliasId

</td><td>

String

</td><td>

Sys\_id of the connection or credential alias whose OAuth initiator URL you want to retrieve.Table: Connection &amp; Credential Aliases \[sys\_alias\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|OAuth initiator URL for the personal authentication credential associated with the specified alias. If the personal authentication credential doesn't exist for the specified alias, the method returns an empty string.|

The following code example shows how to call this method.

```
var aliasId = "e41b9dd1532102104c4bddeeff7b1250";
var personalAuthAPI = new sn_cc.PersonalAuthAPI();
var result = personalAuthAPI.getInitiatorURL(aliasId);
gs.info(result);
```

Output:

```
/oauth_initiator.do?oauth_requestor_context=oauth_2_0_credentials&oauth_requestor=d84b5115532102104c4bddeeff7b12f2&oauth_provider_profile=d84b5115532102104c4bddeeff7b12ec&response_type=code&personal=true 
```

## PersonalAuthAPI - isTokenValid\(String aliasId\)

Checks whether a valid access/refresh token exists for the personal authorization credential associated with a specified alias.

<table id="table_npq_pk2_3bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aliasId

</td><td>

String

</td><td>

Sys\_id of the connection or credential alias to check for the associated personal authorization credential.Table: Connection &amp; Credential Aliases \[sys\_alias\]

</td></tr></tbody>
</table><table id="table_opq_pk2_3bc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether there's an associated personal authorization credential for the specified alias ID.Possible values:

-   true: A valid personal authorization credential exists.
-   false: A valid personal authorization credential doesn't exist.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var aliasId = "e41b9dd1532102104c4bddeeff7b1250"; 
var personalAuthAPI = new sn_cc.PersonalAuthAPI();  
var result = personalAuthAPI.isTokenValid(aliasId); 
gs.info(result);
```

Output:

```
true
```

## PersonalAuthAPI - revokeToken\(String aliasId\)

Revokes an existing access/refresh token for the personal authentication credential associated with a specified alias.

<table id="table_nsn_nwk_3bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aliasId

</td><td>

String

</td><td>

Sys\_id of the connection or credential alias whose access/refresh token for the personal authorization credential you want to revoke.Table: Connection &amp; Credential Aliases \[sys\_alias\]

</td></tr></tbody>
</table><table id="table_osn_nwk_3bc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object that contains methods that you can call to obtain additional information about the status of the credential and method call. These methods are available until the next time this method is called.-   &lt;object\_name&gt;.getResponseStatus\(\): Returns the status of the revokeToken\(\) method call, either `success` or `fail`. You can find additional information on any error in the error logs.
-   &lt;object\_name&gt;.getExpiryInSeconds\(\): Returns the number of seconds until the associated credential expires. If this value is anything other than zero, the revoke request failed.
-   &lt;object\_name&gt;.isAuthenticated\(\): Returns a Boolean value that indicates whether the personal auth token exists. If the revokeToken\(\) method call was successful, this method should return `false`.
-   &lt;object\_name&gt;.getCredentialId\(\): Returns the sys\_id of the personal authorization credential associated with the token. Located in the OAuth 2.0 Credentials \[oauth\_2\_0\_credentials\] table.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var aliasId = "e41b9dd1532102104c4bddeeff7b1250";
var personalAuthAPI = new sn_cc.PersonalAuthAPI();
var personalAuthResponse = personalAuthAPI.revokeToken(aliasId); 
gs.info(personalAuthResponse.getResponseStatus());
gs.info(personalAuthResponse.getExpiryInSeconds());
gs.info(personalAuthResponse.isAuthenticated());
gs.info(personalAuthResponse.getCredentialId());
```

Output:

```
SUCCESS
0
false
d84b5115532102104c4bddeeff7b12f2
```

