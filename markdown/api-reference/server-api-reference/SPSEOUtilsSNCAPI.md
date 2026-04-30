---
title: SPSEOUtilsSNC - Global
description: The SPSEOUtilsSNC script include provides utility methods that return human-readable URLs for a specific page, or for the current page, based on the transaction request.Returns the human-readable URL for a specified record in the Page \[sp\_page \] table. Uses the passed-in query parameters to resolve any dynamic page variables required by the URL.Returns the human-readable URL for the current Service Portal record.Returns the GlideRecord from the Pages \[sp\_page\] table whose ID field matches the passed ID parameter \(pageId\). Call this method prior to calling the getHumanReadableUrl\(\) method to obtain the desired sp\_pages GlideRecord.Returns the sys\_id of the portal being loaded based on the portal suffix in the request URL. Call this method prior to calling the getPageRecordWithPageRoute\(\) method to obtain the desired Service Portal sys\_id.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SPSEOUtilsSNC- Global

The SPSEOUtilsSNC script include provides utility methods that return human-readable URLs for a specific page, or for the current page, based on the transaction request.

In addition, this API provides other utility methods that you can use to obtain information that is needed to call other human-readable URL methods.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SPSEOUtilsSNC - getHumanReadableUrl\(GlideRecord pageGR, String queryString\)

Returns the human-readable URL for a specified record in the Page \[sp\_page \] table. Uses the passed-in query parameters to resolve any dynamic page variables required by the URL.

<table id="table_vjm_wwg_hvb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

pageGR

</td><td>

GlideRecord

</td><td>

GlideRecord object of the record in the Page \[sp\_page\] table for which to return the human-readable URL.Use the [SPSEOUtilsSNC - getPageRecordWithPageRoute\(GlideRecord pageId, String portalId, Boolean preventReRoute\)](SPSEOUtilsSNCAPI.md#) method to obtain the desired sp\_page GlideRecord.

</td></tr><tr><td>

queryString

</td><td>

String

</td><td>

Query string to use to resolve any parameters that may need to be passed by the URL. For example: `?id=kb_article&sys_id=471ee81eff6002009b20ffffffffff34`

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Human-readable URL for the specified Service Portal record. The URL variables are resolved using the contents of the passed **queryString** parameter.|

The following code example shows how to call this method to obtain the human-readable URL.

```
function() { 
  var util = new global.SPSEOUtilsSNC();
  var portalId = util.getPortalId();
  var pageGR = util.getPageRecordWithPageRoute(
    'kb_article', portalId, false); 
  var queryString = "?id=kb_article&sys_id=471ee81eff6002009b20ffffffffff34"; 
  var hrUrl = util.getHumanReadableUrl(pageGR, queryString);
```

Output:

```
"getting-around-in-windows"
```

## SPSEOUtilsSNC - getHumanReadableUrlForCurrentRequest\(\)

Returns the human-readable URL for the current Service Portal record.

This method replicates the parameters in the cryptic URL of the current page, such as the **id** parameter and the query parameters, when creating this human-readable URL.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Human-readable URL for the current Service Portal record.|

The following code example shows how to call this method. In this example, the current Service Portal record uses the cryptic URL of `<instance-url>/sp?id=kb_article&sys_id=471ee81eff6002009b20ffffffffff34` and is configured to show the short description of a KB article that discusses navigation in Windows. The returned human-readable URL for this cryptic URL is "getting-around-in-windows".

```
// In a script include
function() {
  var util = new global.SPSEOUtilsSNC()
  var hrUrl = util.getHumanReadableUrlForCurrentRequest();
}
```

Output:

```
getting-around-in-windows
```

## SPSEOUtilsSNC - getPageRecordWithPageRoute\(GlideRecord pageId, String portalId, Boolean preventReRoute\)

Returns the GlideRecord from the Pages \[sp\_page\] table whose ID field matches the passed ID parameter \(**pageId**\). Call this method prior to calling the getHumanReadableUrl\(\) method to obtain the desired sp\_pages GlideRecord.

You can also request that the method use the page route maps information to return the GlideRecord of the final Service Portal page associated with the passed Service Portal page ID. For additional information on page route maps, see [Redirect a reference to a page ID](https://www.servicenow.com/docs/access?context=reroute-page&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

<table id="table_hhx_rzn_tvb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

pageId

</td><td>

String

</td><td>

ID of the Pages \[sp\_page\] record to return. Table: In the id field of the Pages \[sp\_page\] table.

</td></tr><tr><td>

portalId

</td><td>

String

</td><td>

Sys\_id of the associated Service Portal \[sp\_portal\] record. Required to return the appropriate login or 404 pages in case the record associated with the passed **pageId** parameter is not accessible or unavailable.Use the [SPSEOUtilsSNC - getPortalId\(\)](SPSEOUtilsSNCAPI.md#) method to obtain the desired Service Portal ID.

</td></tr><tr><td>

preventReRoute

</td><td>

Boolean

</td><td>

Flag that indicates whether to use page route maps to return the GlideRecord for the last sp\_page that the passed page ID resolves to, instead of the matching sp\_page record.Possible values:

-   true: Use the page route maps to return the last sp\_page record that the passed page ID resolves to.
-   false: Return the sp\_page record that the passed page ID matches.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|GlideRecord|Record that matches the query request for the sp\_page record.|

The following code example shows how to call this method prior to calling the getHumanReadableUrl\(\) method.

```
function() { 
  var util = new global.SPSEOUtilsSNC();
  var portalId = util.getPortalId();
  var pageGR = util.getPageRecordWithPageRoute(
    'kb_article', portalId, false); 
  var queryString = "?id=kb_article&sys_id=471ee81eff6002009b20ffffffffff34"; 
  var hrUrl = util.getHumanReadableUrl(pageGR, queryString);
```

## SPSEOUtilsSNC - getPortalId\(\)

Returns the sys\_id of the portal being loaded based on the portal suffix in the request URL. Call this method prior to calling the getPageRecordWithPageRoute\(\) method to obtain the desired Service Portal sys\_id.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the requested Service Portal based on the portal suffix of the request URL.|

The following code example shows how to call this method for a URL such as `<instance-url>/sp?id=index`.

```
function() { 
  var util = new global.SPSEOUtilsSNC();
  var portalId = util.getPortalId();
  var pageGR = util.getPageRecordWithPageRoute(
    'kb_article', portalId, false); 
  var queryString = "?id=kb_article&sys_id=471ee81eff6002009b20ffffffffff34"; 
  var hrUrl = util.getHumanReadableUrl(pageGR, queryString);
```

Output:

```
81b75d3147032100ba13a5554ee4902b
```

