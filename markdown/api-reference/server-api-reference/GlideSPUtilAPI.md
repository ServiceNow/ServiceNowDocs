---
title: GlideSPUtil - Global
description: The GlideSPUtil API provides utility methods to perform common backend functions that support a Service Portal.Instantiates a GlideSPUtil object.Considers ‘id’ query parameter to identify the portal page \(pageGR\) and uses query string of the current transaction to call getHumanReadableUrl\(GlideRecord pageGR, String queryString\) and returns the final human readable.Converts the passed queryParms string parameter into a string map and then resolves the variables in the "Human readable url structure" string provided in the sp\_page record and returns the final human readable part of the URL.Resolves the variables in the Human readable url structure field of the passed-in Service Portal template page object and returns a URL containing the specified query parameters and the resolved human readable parameters.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideSPUtil- Global

The GlideSPUtil API provides utility methods to perform common backend functions that support a Service Portal.

Available utility methods:

-   Resolve variables specified in the Dynamic page variables \[sp\_page\_title\_variable\] table associated with a specified Service Portal page located in the Page \[sp\_page\] table.
-   Other methods

For additional information, see [Service Portal pages](https://servicenow.com/docs/bundle/vancouver-servicenow-platform/page/build/service-portal/task/add-human-readable-keywords-page-urls.html).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideSPUtil - GlideSPUtil\(\)

Instantiates a GlideSPUtil object.

|Name|Type|Description|
|----|----|-----------|
|None| ||

The following code example shows how to instantiate a GlideSPUtil object before calling any of its associated methods.

```
function() {
  var spUtil = new GlideSPUtil();
  var pageGR = spUtil.getPageRecordWithPageRoute('kb_article', '81b75d3147032100ba13a5554ee4902b', false);
  var queryParams = RP.getParameters();
  var hrUrl = spUtil.getHumanReadableUrl(pageGR, queryParams);
}
```

## GlideSPUtil - getHumanReadableUrl\(\)

Considers ‘id’ query parameter to identify the portal page \(pageGR\) and uses query string of the current transaction to call getHumanReadableUrl\(GlideRecord pageGR, String queryString\) and returns the final human readable.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Human readable URL for the specified Service Portal record with the variables replaced with the contents of the **queryParams** string map.|

The following code example shows how to.

```
function() {
  var spUtil = new GlideSPUtil();
  var hrUrl = spUtil.getHumanReadableUrl();
}
```

Output:

```

```

## GlideSPUtil - getHumanReadableUrl\(GlideRecord pageGR, String queryParams\)

Converts the passed **queryParms** string parameter into a string map and then resolves the variables in the "Human readable url structure" string provided in the sp\_page record and returns the final human readable part of the URL.

|Name|Type|Description|
|----|----|-----------|
|pageGR|GlideRecord|GlideRecord object of the record in the Page \[sp\_page\] table on which to resolve the URL variables.|
|queryString|String|Query string.|

|Type|Description|
|----|-----------|
|String|Human readable URL for the specified Service Portal record with the variables replaced with the contents of the **queryParams** string map.|

The following code example shows how to.

```
function() {
  var spUtil = new GlideSPUtil();
  var pageGR = spUtil.getPageRecordWithPageRoute('kb_article', '81b75d3147032100ba13a5554ee4902b', false);
  var queryString = GlideTransaction.get().getRequest().getQueryString();
  var hrUrl = spUtil.getHumanReadableUrl(pageGR, queryParams);
}
```

Output:

```

```

## GlideSPUtil - getHumanReadableUrl\(GlideRecord pageGR, StringMap queryParams\)

Resolves the variables in the **Human readable url structure** field of the passed-in Service Portal template page object and returns a URL containing the specified query parameters and the resolved human readable parameters.

Use human readable keywords in a URL to:

-   Enable your customers to better understand the purpose of the URL when it is not in the context of the associated page.
-   Provide search engines with keywords to better locate the page.

For example, instead of just having a URL that contains unrecognisable key-value pairs such as this:

`https://instance_name.servicenow.com/sp/en?id=sc_cat_item&sys_id=ec80c13297968d1021983d1e6253af32&sysparm_catgory=1e80c15697969f1032083d1e6253be15`

You can add the item name to the URL so it is easier to understand the purpose of the URL:

`https://instance_name.servicenow.com/sp/en/apple-iphone-13?id=sc_cat_item&sys_id=ec80c13297968d1021983d1e6253af32&sysparm_catgory=1e80c15697969f1032083d1e6253be15`

Before you can use this method, you must define the dynamic page variables that are available for each of the Service Portal templates for which you want to include dynamic content in the URL. For details on adding these variables, see Add human readable keywords to page URLs.

<table id="table_dht_dpg_hvb" class="parameters"><thead><tr><th>

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

GlideRecord object of theService Portal template page for which to resolve the dynamic URL variables. Table: Page \[sp\_page\]

</td></tr><tr><td>

queryParams

</td><td>

StingMap

</td><td>

URL query parameters to use to obtain the desired Service Portal page.For example:

```
{
  "id": "sc_cat_item",
  "sys_id": "ec80c13297968d1021983d1e6253af32",
  "sysparm_catgory": "1e80c15697969f1032083d1e6253be15"
}
```

</td></tr></tbody>
</table><table id="table_eht_dpg_hvb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

URL containing the resolved human readable elements for the dynamic variables specified in the Service Portal template page. For example, if the defined dynamic variable is **%item\_name**, the URL contains the name of the item that the user selected, such as "apple-iphone-13, and all of the specified query parameters:

`https://instance_name.servicenow.com/sp/en/apple-iphone-13?id=sc_cat_item&sys_id=ec80c13297968d1021983d1e6253af32&sysparm_catgory=1e80c15697969f1032083d1e6253be15`.

</td></tr></tbody>
</table>The following code example shows how to obtain a specific KB article and call the getHumanReaadableUrl\(\) to apply the associated dynamic variables.

```
function() {
  var spUtil = new GlideSPUtil();
  var pageGR = spUtil.getPageRecordWithPageRoute('kb_article', '81b75d3147032100ba13a5554ee4902b', false);
  var queryParams = RP.getParameters();
  var hrUrl = spUtil.getHumanReadableUrl(pageGR, queryParams);
}
```

