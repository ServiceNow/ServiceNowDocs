---
title: UriMatcher - Scoped
description: Provides a method to check if a URI matches specified criteria for scheme, host, path, fragments, and presence of query parameters.Instantiates a new UriMatcher object.Checks if a URI matches specified criteria for scheme, host, path, fragments, and presence of query parameters.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# UriMatcher- Scoped

Provides a method to check if a URI matches specified criteria for scheme, host, path, fragments, and presence of query parameters.

The UriMatcher API requires the REST API Provider \(com.glide.rest\) plugin, which is activated by default.

This API is provided within the `sn_ws` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## UriMatcher - UriMatcher\(\)

Instantiates a new UriMatcher object.

|Name|Type|Description|
|----|----|-----------|
|None| ||

Instantiates a UriMatcher object.

```
var matcher = new sn_ws.UriMatcher();
```

## UriMatcher - match\(String uri, String scheme, Array hosts, Array paths, Array fragments, Boolean disallowQueryParameters\)

Checks if a URI matches specified criteria for scheme, host, path, fragments, and presence of query parameters.

<table id="table_ejx_wjw_qdc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

uri

</td><td>

String

</td><td>

URI to test against the specified criteria.

</td></tr><tr><td>

scheme

</td><td>

String

</td><td>

Protocol used in the URI.Valid values:

-   http
-   https

</td></tr><tr><td>

hosts

</td><td>

Array

</td><td>

List of allowed hosts in the URI.The URI must use one of the allowed hosts to be considered a match.

</td></tr><tr><td>

paths

</td><td>

Array

</td><td>

Optional. List of allowed paths in the URI.The URI must use one of the allowed paths to be considered a match, and the allowed path must be the full path used in the URI. For example, if the allowed path is `/path1`, a URI with the path `/path1/more` isn't considered a match.

**Note:** Paths must start with `/`.

Default: Any path is allowed.

</td></tr><tr><td>

fragments

</td><td>

Array

</td><td>

Optional. List of allowed fragments in the URI. The URI is considered a match even if it doesn't contain any of the allowed fragments. The URI is only considered not matching if it contains fragments that aren't in the allowed list.

Default: Any fragment is allowed.

</td></tr><tr><td>

disallowQueryParameters

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether query parameters are allowed in the URI.Valid values:

-   true: Query parameters aren't allowed. If query parameters are included in the URI, an error occurs.
-   false: Query parameters are allowed.

Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|[UriMatcherResponse](../../UriMatcherResponseScoped/concept/UriMatcherResponseScopedAPI.md#)|UriMatcherResponse object with methods for returning detailed information about the match.|

This example checks if the URI matches the specified scheme and host.

```
var uri = "https://example.com/path?q=query";
var scheme = "https";  
var allowedHosts = ["example.com"];  
var matcher = new sn_ws.UriMatcher();  
var resp = matcher.match(uri, scheme, allowedHosts);  

gs.info("Is URI a match: " + resp.isMatch());
```

Output:

```
Is URI a match: true
```

This example checks if the URI matches the specified scheme, host, path, fragments, and presence of query parameters.

```
var uri = "https://example.com/path1/more";
var scheme = "https";  
var allowedHosts = ["example.com", "sample.com"];  
var allowedPaths = ["/path1/more", "/path2/less"];  
var allowedFragments = ["section1", "section2"];  
var noQueryParams = true;
var matcher = new sn_ws.UriMatcher();  
var resp = matcher.match(uri, scheme, allowedHosts, allowedPaths, allowedFragments, noQueryParams);  

gs.info("Is URI a match: " + resp.isMatch());  
gs.info("Is scheme a match: " + resp.isSchemeMatches());  
gs.info("Is host a match: " + resp.isHostMatches());  
gs.info("Is path a match: " + resp.isPathMatches());  
gs.info("Is fragment a match: " + resp.isFragmentMatches());
gs.info("Error occurred: " + resp.isError());  
gs.info("Error message: " + resp.getErrorMessages());
```

Output:

```
Is URI a match: true
Is scheme a match: true
Is host a match: true
Is path a match: true
Is fragment a match: true
Error occurred: false
Error message:
```

