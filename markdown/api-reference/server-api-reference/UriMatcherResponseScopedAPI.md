---
title: UriMatcherResponse - Scoped
description: Provides methods to return information about whether a URI matches specified criteria for scheme, host, path, fragments, and presence of query parameters.Returns messages about any errors that occurred when testing the URI against the specified criteria.Checks if an error occurred when testing the URI against the specified criteria.Checks if the URI matches the criteria for fragments.Checks if the URI matches the criteria for the host.Checks if the URI matches all of the specified criteria.Checks if the URI matches the criteria for the path.Checks if the URI matches the criteria for the scheme.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# UriMatcherResponse- Scoped

Provides methods to return information about whether a URI matches specified criteria for scheme, host, path, fragments, and presence of query parameters.

Use this API with the UriMatcher API. This API doesn't have a constructor. Instead, use the [UriMatcher - match\(\)](../../UriMatcherScoped/concept/UriMatcherScopedAPI.md#) method to instantiate a UriMatcherResponse object.

The UriMatcherResponse API requires the REST API Provider \(com.glide.rest\) plugin, which is activated by default.

This API is provided within the `sn_ws` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## UriMatcherResponse - getErrorMessages\(\)

Returns messages about any errors that occurred when testing the URI against the specified criteria.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Description of the error that occurred. If no error occurred, an empty string is returned.|

This example returns an error because a host wasn't provided in the matching criteria.

```
var uri = "https://example.com";
var scheme = "https";    
var matcher = new sn_ws.UriMatcher();  
var resp = matcher.match(uri, scheme);  

gs.info("Error occurred: " + resp.isError());  
gs.info("Error message: " + resp.getErrorMessages());
```

Output:

```
Error occurred: true
Error message: Hosts rule is null or empty.
```

## UriMatcherResponse - isError\(\)

Checks if an error occurred when testing the URI against the specified criteria.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_nh3_xyt_rdc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether an error occurred.

 Valid values:

-   true: An error occurred.
-   false: No errors occurred.

</td></tr></tbody>
</table>This example returns an error because the URI contains query parameters. The error occurs because the argument passed to match\(\) for **disallowQueryParameters** is `true`.

```
var uri = "https://example.com/path1/more?q=query";
var scheme = "https";  
var allowedHosts = ["example.com", "sample.com"];  
var allowedPaths = ["/path1/more", "/path2/less"];  
var allowedFragments = ["section1", "section2"];  
var noQueryParams = true;
var matcher = new sn_ws.UriMatcher();  
var resp = matcher.match(uri, scheme, allowedHosts, allowedPaths, allowedFragments, noQueryParams);  

gs.info("Error occurred: " + resp.isError());  
gs.info("Error message: " + resp.getErrorMessages());
```

Output:

```
Error occurred: true
Error message: Query parameters are not allowed for matching.
```

## UriMatcherResponse - isFragmentMatches\(\)

Checks if the URI matches the criteria for fragments.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_wls_lzt_rdc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the URI matches the criteria for fragments.

 Valid values:

-   true: The URI matches the criteria for fragments.
-   false: The URI doesn't match the criteria for fragments.

</td></tr></tbody>
</table>This example shows that the URI doesn't match the criteria because it contains a fragment that isn't in the list of allowed fragments.

```
var uri = "https://example.com/path1/more#section3";
var scheme = "https";  
var allowedHosts = ["example.com", "sample.com"];  
var allowedPaths = ["/path1/more", "/path2/less"];  
var allowedFragments = ["section1", "section2"];  
var matcher = new sn_ws.UriMatcher();  
var resp = matcher.match(uri, scheme, allowedHosts, allowedPaths, allowedFragments);  

gs.info("Is URI a match: " + resp.isMatch());  
gs.info("Is scheme a match: " + resp.isSchemeMatches());  
gs.info("Is host a match: " + resp.isHostMatches());  
gs.info("Is path a match: " + resp.isPathMatches());  
gs.info("Is fragment a match: " + resp.isFragmentMatches());
gs.info("Error occurred: " + resp.isError());
```

Output:

```
Is URI a match: false
Is scheme a match: true
Is host a match: true
Is path a match: true
Is fragment a match: false
Error occurred: false
```

## UriMatcherResponse - isHostMatches\(\)

Checks if the URI matches the criteria for the host.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_jgl_hzt_rdc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the URI matches the criteria for the host.

 Valid values:

-   true: The URI matches the criteria for the host.
-   false: The URI doesn't match the criteria for the host.

</td></tr></tbody>
</table>This example checks if the URI matches the specified scheme and host.

```
var uri = "https://example.com/path?q=query";
var scheme = "https";  
var allowedHosts = ["example.com"];  
var matcher = new sn_ws.UriMatcher();  
var resp = matcher.match(uri, scheme, allowedHosts);  

gs.info("Is URI a match: " + resp.isMatch());
gs.info("Is host a match: " + resp.isHostMatches());
```

Output:

```
Is URI a match: true
Is host a match: true
```

## UriMatcherResponse - isMatch\(\)

Checks if the URI matches all of the specified criteria.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_hzs_tyt_rdc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the URI matches all of the specified criteria.

 Valid values:

-   true: The URI matches all of the criteria.
-   false: The URI doesn't match all of the criteria.

</td></tr></tbody>
</table>This example checks if the URI matches the specified scheme and host.

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

## UriMatcherResponse - isPathMatches\(\)

Checks if the URI matches the criteria for the path.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_b5x_3zt_rdc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the URI matches the criteria for the path.

 Valid values:

-   true: The URI matches the criteria for the path.
-   false: The URI doesn't match the criteria for the path.

</td></tr></tbody>
</table>This example checks if the URI matches the specified scheme, host, and path.

```
var uri = "https://example.com/path1/more";
var scheme = "https";  
var allowedHosts = ["example.com", "sample.com"];  
var allowedPaths = ["/path1/more", "/path2/less"];  
var matcher = new sn_ws.UriMatcher();  
var resp = matcher.match(uri, scheme, allowedHosts, allowedPaths);  

gs.info("Is URI a match: " + resp.isMatch());  
gs.info("Is scheme a match: " + resp.isSchemeMatches());  
gs.info("Is host a match: " + resp.isHostMatches());  
gs.info("Is path a match: " + resp.isPathMatches());  
gs.info("Is fragment a match: " + resp.isFragmentMatches());
gs.info("Error occurred: " + resp.isError());
```

Output:

```
Is URI a match: true
Is scheme a match: true
Is host a match: true
Is path a match: true
Is fragment a match: true
Error occurred: false
```

## UriMatcherResponse - isSchemeMatches\(\)

Checks if the URI matches the criteria for the scheme.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_q54_dzt_rdc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the URI matches the criteria for the scheme.

 Valid values:

-   true: The URI matches the criteria for the scheme.
-   false: The URI doesn't match the criteria for the scheme.

</td></tr></tbody>
</table>This example checks if the URI matches the specified scheme and host.

```
var uri = "https://example.com/path?q=query";
var scheme = "https";  
var allowedHosts = ["example.com"];  
var matcher = new sn_ws.UriMatcher();  
var resp = matcher.match(uri, scheme, allowedHosts);  

gs.info("Is URI a match: " + resp.isMatch());
gs.info("Is scheme a match: " + resp.isSchemeMatches());
```

Output:

```
Is URI a match: true
Is scheme a match: true
```

