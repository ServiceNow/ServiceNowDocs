---
title: SecretsAPI - Scoped
description: The SecretsAPI provides an entry point for delivering credentials to a MID Server without requiring the caller to know the underlying storage mechanism. This scoped API enforces a comprehensive authorization chain before decrypting and returning secret values.Retrieves a single secret by alias, resolving the alias into a table/field/record coordinate and running the authorization chain before decrypting and returning the value.Retrieves every secret belonging to a named alias group in one call, returning a pre-partitioned result with successes and per-alias failures so the caller does not have to loop and catch individually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/server-api-reference/SecretsAPI.html
release: brazil
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-10-04"
reading_time_minutes: 5
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SecretsAPI- Scoped

The SecretsAPI provides an entry point for delivering credentials to a MID Server without requiring the caller to know the underlying storage mechanism. This scoped API enforces a comprehensive authorization chain before decrypting and returning secret values.

The primary consumer of this API is MID Server credential delivery. The API allows MID Server callers to set a caller-identity property on the session before calling getSecret\(\) or getSecrets\(\). This enables alias groups configured with `filter_mode="mid_scoped"` to restrict which credentials a given MID agent is allowed to see. This API is intended for use by internal platform scripts and MID Server credential delivery.

Every call to getSecret\(\) or getSecrets\(\) passes through a seven-step authorization chain \(banned table, lockdown, type compatibility, table ACL, row ACL, consumer grant, MAP policy\) before any secret value is decrypted. Denial at any step exits immediately with no secret material touched. All denials return a uniform error to the caller. The specific reason is recorded only in the audit log \(enable with`glide.usg.audit.trace=true`\) and is never exposed to callers.

The API returns one of two shapes:

-   A plain decrypted value \(Password2 field — for example, a credential's password\).
-   A full credential record \(`value_field="*"` groups — every field of a credential, each decrypted\).

## Access instructions and requirements

The SecretsAPI is supported by the Unified Secrets Gateway \(USG\) product and is available with the USG plugin \(com.glide.usg.global\) and requires the com.glide.kmf.global plugin. The API is provided within the sn\_usg\_ns namespace.

To access this API, use `var api = new sn_usg_ns.SecretsAPI();` with no constructor arguments.

The sn\_kmf.cryptographic\_manager role is required to configure sys\_secret\_alias\_group and sys\_secret\_alias\_consumer records.

**Parent Topic:**[Server API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/api-server.md)

## SecretsAPI - getSecret\(String alias\)

Retrieves a single secret by alias, resolving the alias into a table/field/record coordinate and running the authorization chain before decrypting and returning the value.

This method identifies the calling context \(including the MID agent identity if set\), then runs the authorization chain \(table ACL, row ACL, consumer grant if applicable\) before decrypting and returning the value. Returns a JSON string that must be parsed by the caller.

<table id="table_getsecret_params" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

alias

</td><td>

String

</td><td>

Required. The secret alias to resolve. Must not be empty.Valid formats:

-   Direct: `"<table>.<field>.<sys_id>"`. For example `"discovery_credentials.password.<sys_id>"`.
-   Group: `"<groupName>.<alias>"`. For example`"mid_creds.host1"`.

Default value \(or behavior if not provided\): throws rather than returning nothing.

</td></tr></tbody>
</table><table id="table_getsecret_returns" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

JSON string \(must be parsed by caller\) containing one of two shapes: -   For a Password2 field:

    ```
{"alias": "String", "value": "String"}
    ```

-   For a full credential \(value\_field="\*" alias groups\):

    ```
{"alias": "String", "fields": {"<fieldName>": "String", ...}}
    ```


On failure, the scripted wrapper returns null rather than throwing. Every failure mode \(bad alias, access denied, record not found\) collapses to the same null. This is intended behavior to prevent probing for configuration or secrets.

</td></tr></tbody>
</table>This example shows two variants: retrieving a plain secret \(Password2 field\) and retrieving a full credential record.

```
var api = new sn_usg_ns.SecretsAPI();

// Variant A — plain Secret (alias group's value_field is a specific field, e.g. "password")
var rawA = api.getSecret('discovery_credentials.password.' + credentialSysId);
if (rawA) {
    var secretResult = JSON.parse(rawA);
    gs.info('Fetched credential for alias: ' + secretResult.alias);
    // secretResult.value — the decrypted password
}

// Variant B — Credential, full record (alias group's value_field is "*") — per KB0562777
var rawB = new sn_usg_ns.SecretsAPI().getSecret('mid_creds.host1');
if (rawB) {
    var credentialResult = JSON.parse(rawB);
    var password = credentialResult.fields['password'];
    // credentialResult.fields — every decrypted field on the credential record
}
```

Output:

```
Fetched credential for alias: discovery_credentials.password.3f412b8a...
```

## SecretsAPI - getSecrets\(String groupName\)

Retrieves every secret belonging to a named alias group in one call, returning a pre-partitioned result with successes and per-alias failures so the caller does not have to loop and catch individually.

This is the bulk MID-credential-delivery shape. A MID agent can fetch every credential it is scoped to from one mid\_scoped group in a single round trip. The method returns a JSON string that must be parsed by the caller.

<table id="table_getsecrets_params" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

groupName

</td><td>

String

</td><td>

Required. The alias group to fetch. Must not be empty. Valid values: any existing Alias Group Name. For example a MID-scoped credential group such as `"mid_credentials"`.

Table: Secret Alias Group \[sys\_secret\_alias\_group\], Field: Alias Group Name

Default value or behavior if not provided: throws rather than defaulting to any group.

</td></tr></tbody>
</table><table id="table_getsecrets_returns" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

JSON string \(must be parsed by caller\) containing a successful array or two distinct failure levels.

 Data type: Object

 ```
{"successful": [<secret objects, same shapes as getSecret's return>], 
 "failed": [{"alias": "String", "error": "String"}, ...]}
```

 Possible values:

-   Success: The `"successful"` array contains entries matching getSecret's Password2 or Credential shapes.
-   Failure: The `"failed"` array contains entries for aliases that could not be fetched, identifying the alias and the reason \(for example, ACCESS\_DENIED, RECORD\_NOT\_FOUND\). A failure array contains two distinct levels:
    -   Group-level failure: If the named group does not exist, the entire call fails and the scripted wrapper returns null, exactly like getSecret\(\)'s failure case. Nothing is returned, not even a failed array.
    -   Per-alias failure: If the group exists but one or more members can't be fetched, the call still succeeds and returns a normal object. The failing aliases appear in the failed array instead of successful. A caller receives a usable response in this case and must check the failed array explicitly, since a non-null result does not indicate that every member succeeded.

</td></tr></tbody>
</table>This example shows batch retrieval of credentials from a named alias group. The result is checked for successful entries.

```
var json = new sn_usg_ns.SecretsAPI().getSecrets('mid_credentials');
var result = JSON.parse(json);
result.successful.forEach(function(secret) {
    gs.log('Alias: ' + secret.alias);
});
```

Output:

```
Alias: mid_credentials.3f412b8a...
```

### Troubleshooting

<table id="table_qx1_sc4_5kc"><thead><tr><th>

Error

</th><th>

Likely cause / fix

</th></tr></thead><tbody><tr><td>

ACCESS\_DENIED with no context

</td><td>

Enable `glide.usg.audit.trace=true` \(reloads live, no restart\) to see the denying gate in the audit log. Never exposed to the caller directly. Common causes:

-   Missing Row ACL,
-   Missing Consumer Grant \(external/MID callers\),
-   MAP Policy denial,
-   The alias group is in a LOCKDOWN state.

</td></tr><tr><td>

RECORD\_NOT\_FOUND

</td><td>

The alias\_field value doesn't exist in the target table, or for `filter_mode=mid_scoped`, the record doesn't have `applies_to="all"` or the calling MID Server's ID in `mid_list`.

</td></tr><tr><td>

INVALID\_FORMAT

</td><td>

Alias string doesn't match either addressing mode: -   Tier 3 `"table.field.sys_id"`
-   Tier 2 `"group_name.alias"`

</td></tr></tbody>
</table>