---
title: StandardCredentialsProvider - Scoped, Global
description: The StandardCredentialsProvider API provides methods to retrieve credential information.Instantiates a credentials provider object.Returns an array of all credentials that match the specified types and tags.Returns the credential record object through its credential alias \(sys\_alias\).Returns the credential record object identified by the specified sys\_id.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# StandardCredentialsProvider - Scoped, Global

The StandardCredentialsProvider API provides methods to retrieve credential information.

You can use this API in scoped applications or within the global scope. In scoped scripts, use the `sn_cc` namespace identifier.

This API provides methods to retrieve credential information by sys\_id and by specified credential attributes.

```
//Get a single credential

var provider = new sn_cc.StandardCredentialsProvider();
var credential = provider.getCredentialByID("f43c6d40a0a0b5700c77f9bf387afe3");
var userName = credential.getAttribute("user_name");
var password = credential.getAttribute("password");
//using getAttribute for new keys in extended tables, for example 
//cloud management credential has the "user_public_key" attribute
var userPublicKey = credential.getAttribute("user_public_key");

//Get a list of SSH credentials

var provider = new sn_cc.StandardCredentialsProvider();
var credentials = provider.getCredentials(["ssh"]);
for (var i = 0; i < credentials.length; i++) {
  var credential = credentials[i];
  gs.info(credential.getAttribute("name"));
}
```

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## StandardCredentialsProvider - StandardCredentialsProvider\(\)

Instantiates a credentials provider object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var provider = new sn_cc.StandardCredentialsProvider();
var credentials = provider.getCredentialByID("ef43c6d40a0a0b5700c77f9bf387afe3");
```

## StandardCredentialsProvider - getCredentials\(String types, String tags\)

Returns an array of all credentials that match the specified types and tags.

<table id="table_xxn_xq2_qbb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

tags

</td><td>

String

</td><td>

Optional. Comma-separated list of tag names. For example, "ssh, jdbc".Examples of valid calls:

-   `var credentials = provider.getCredentials(null, null);`
-   `var credentials = provider.getCredentials(["ssh"], "");`
-   `var credentials = provider.getCredentials(new ArrayList<String>(), "ssh,admin");`

</td></tr><tr><td>

types

</td><td>

Array

</td><td>

Optional. Credential type names. For example, \["ssh", "windows"\]**Note:** If **types** is null or empty, any match returns a credential. If **types** is specified, the credentials whose type matches one of the types is returned.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|StandardCredential|Credential record object.|

This code example shows how to get the provider credentials for "ssh" credential types.

```
var provider = new sn_cc.StandardCredentialsProvider();
var credentials = provider.getCredentials(["ssh"]);
```

This code example shows how to get the provider credentials for "ssh" and "windows" credential types that have tags of "admin".

```
var provider = new sn_cc.StandardCredentialsProvider();
ArrayList<String> types = new ArrayList<>();
types.add("ssh");
types.add("windows");
JSONArray jsonArray = provider.getCredentials(types, "admin");
```

## StandardCredentialsProvider - getCredentialByAliasID\(String sys\_id\)

Returns the credential record object through its credential alias \(sys\_alias\).

This method is specifically for use with credential types. For information, see [Credential aliases for Discovery](https://www.servicenow.com/docs/access?context=discovery-credential-alias&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|sys\_id|String|Sys\_id of the credential alias record in the Connection &amp; Credential Aliases \[sys\_alias\] table.|

|Type|Description|
|----|-----------|
|StandardCredential|Credential record object.|

The following example retrieves a credential using the alias ID and displays the user name.

```
var provider = new sn_cc.StandardCredentialsProvider();
var aliasCred = provider.getCredentialByAliasID("752a91887740001038e286a2681061fb");
gs.info("User name: " + aliasCred.getAttribute("user_name"));
```

Output for a credential record with a user name:

```
User name: Dara Lee
```

## StandardCredentialsProvider - getCredentialByID\(String sys\_id\)

Returns the credential record object identified by the specified sys\_id.

<table id="table_xxn_xq2_qbb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sys\_id

</td><td>

String

</td><td>

Sys\_id of the credential record. Table: Credentials \[discovery\_credentials\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|StandardCredential|Credential record object.|

The following example retrieves a credential and displays the user name.

```
var provider = new sn_cc.StandardCredentialsProvider();
var credentials = provider.getCredentialByID("ef43c6d40a0a0b5700c77f9bf387afe3");
gs.info("User name: " + credentials.getAttribute("user_name"));
```

Output for a credential record with a user name:

```
User name: Dara Lee
```

