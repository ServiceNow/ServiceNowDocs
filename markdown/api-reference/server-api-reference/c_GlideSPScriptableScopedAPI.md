---
title: GlideSPScriptable - Scoped
description: The GlideSPScriptable API provides methods to interact with data and perform record operations in Service Portal widgets.Returns true if the user can read the specified GlideRecord.Returns true if the user can read the specified GlideRecord.Returns true if the currently logged in user has permission to view the specified page.Returns a model and view model for a sc\_cat\_item or sc\_cat\_item\_guide.Returns a model and view model for a sc\_cat\_item or sc\_cat\_item\_guide.Returns the display value of the specified field \(if it exists and has a value\) from either the widget's sp\_instance or the sp\_portal record.Returns information about the specified field in the specified GlideRecord.Checks the specified list of field names, and returns an array of valid field names.Checks the specified list of field names and returns an object of valid field names.Return the form associated with the passed table name and record sys\_id.Returns KB articles in the specified category and its subcategories.Returns Knowledge Base article summaries in the specified category and its subcategories.Returns the number of articles in the defined Knowledge Base.Returns a list of the specified table's columns in the specified view.Returns an array of menu items for the specified instance.Returns the \(?id=\) portion of the URL based on the sp\_menu type.Returns the value of the specified parameter.Returns the portal record from the Service Portals \[sp\_portal\] table.If parameters are provided, returns the GlideRecord identified by the provided table and Sys ID. If no parameters are provided, returns the record identified by the current URL.Copies display values for the specified fields into the data parameter.For the specified fields, copies the element's name, display value, and value into the data parameter.Copies values for the specified field names from the GlideRecord into the data parameter.Returns Service Catalog variables associated with a record in String format.Returns an array of Service Catalog variables associated with a record.Gets the activity stream for the specified record. This method works on tables that extend the task table.Returns the user's initials.Returns the named value of the JSON request, instance, or portal.Copies values from the request or instance to the data parameter.Returns an array of Service Catalog variables associated with the record in the URL.Gets a widget by id or sys\_id, executes that widget's server script using the provided options, then returns the widget model.Checks whether the associated portal is enabled for right-to-left language \(RTL\) and whether the current user's language is directionally RTL.Returns true if user criteria is enabled.Logs output to the Service Portal Log Entries \[sp\_log\] table. The logged in user must have the sp\_admin or admin role.Transforms a URL requesting a list or form in the platform UI into the URL of the corresponding id=list or id=form Service Portal page.Returns true if the current user can see a search source specified by the searchSourceID.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 17
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideSPScriptable- Scoped

The GlideSPScriptable API provides methods to interact with data and perform record operations in Service Portal widgets.

You access GlideSPScriptable methods by using the global `$sp` object.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideSPScriptable - canReadRecord\(GlideRecord now\_GR\)

Returns true if the user can read the specified GlideRecord.

If the record type is `kb_knowledge`, `sc_cat_item`, or `sc_category`, the method checks if the user can view the item.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|GlideRecord|The GlideRecord to check.|

|Type|Description|
|----|-----------|
|Boolean|True if the record is valid and readable.|

Server script

```
//Server script
data.items = [];
data.userName = gs.getUserDisplayName();
var now_GR = new GlideRecord("sc_cat_item");
now_GR.query();
while(now_GR.next() && data.items.length < 10) {
    if ($sp.canReadRecord(now_GR)) {
    data.items.push(now_GR.getDisplayValue("name"));
    }
}

//HTML template
<div class="panel panel-default">
    <div class="panel-heading">Hi, {{c.data.userName}}!</div>
    <div class="panel-body">
        Here are some things you can order:
        <ul><li ng-repeat="item in c.data.items">{{item}}</li></ul>
    </div>
</div>
```

## GlideSPScriptable - canReadRecord\(String table, String sysId\)

Returns true if the user can read the specified GlideRecord.

If the record type is `kb_knowledge`, `sc_cat_item`, or `sc_category`, the method checks if the user can view the item.

|Name|Type|Description|
|----|----|-----------|
|table|String|Name of the table to query.|
|sysId|String|Sys\_id of the record to query.|

|Type|Description|
|----|-----------|
|Boolean|True if the record is valid and readable.|

## GlideSPScriptable - canSeePage\(String pageID\)

Returns true if the currently logged in user has permission to view the specified page.

The system determines permission using roles and user criteria. For more information, see [Configure page security by role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/configure-page-security.md) and [User criteria for Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/user-criteria.md).

|Name|Type|Description|
|----|----|-----------|
|pageID|String|Page ID from the Pages \[sp\_page\] table.|

<table id="table_tzf_mxq_s3b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the currently logged in user has permissions to view the specified page. Values include:-   true: The user can view the page.
-   false: Either the user cannot view the page, the given pageID is not valid, or the user is not logged in.

</td></tr></tbody>
</table>This example adds a condition to the Knowledge menu item in the SP Header Menu to only show the menu item to users who have permission to view the kb\_view2 page.

```
GlideSPScriptable.canSeePage("kb_view2")
```

## GlideSPScriptable - getCatalogItem\(String sysId\)

Returns a model and view model for a `sc_cat_item` or `sc_cat_item_guide`.

This method is deprecated. Use the getCatalogItem\(String sysId, Boolean isOrdering\) method instead. This method calls the getCatalogItem\(String sysId, Boolean isOrdering\) method with the **isOrdering** parameter set to false, which means that write roles security checking is done.

This method is a quick way to get the data necessary to render and order a catalog item using `<sp-model />`. If you just need to get a catalog item to show its picture or name, use GlideRecord to query the `sc_cat_item` table.

|Name|Type|Description|
|----|----|-----------|
|sysId|String|The sys\_id of the catalog item \(`sc_cat_item`\) or order guide \(`sc_cat_item_guide`\).|

|Type|Description|
|----|-----------|
|Object|An object containing the catalog item variable model, view, sections, pricing, and client scripts.|

```
// Server script
(function() {
    var sys_id = $sp.getParameter("sys_id")
    data.catItem = $sp.getCatalogItem(sys_id);
})();

// Client script
function($http, spUtil) {
    var c = this;
    var submitting = false;
    c.getIt = function() {
        if (submitting) return;
        $http.post(spUtil.getURL('sc_cat_item'), c.data.catItem).success(function(response) {
            if (response.answer) {
                c.req = response.answer;
                c.req.page = c.req.table == 'sc_request' ? 'sc_request' : 'ticket';
            }
        });
    }
}

//SCSS
.img-bg {
    padding: 5px;
    background-color: $brand-primary;
}

.img-responsive {
    margin: 0 auto;
}

.cat-icon {
    display: block;
    margin: -40px auto 0;
}

// HTML template
<div class="col-sm-4">
  <div class="panel panel-default">
    <div class="img-bg">
      <img ng-src="{{::data.catItem.picture}}" class="img-responsive" />
    </div>
    <span class="cat-icon fa fa-stack fa-lg fa-3x hidden-xs">
      <i class="fa fa-circle fa-stack-2x text-success"></i>
      <i class="fa fa-desktop fa-stack-1x fa-inverse"></i>
    </span>
    <div class="panel-body">
      <p class="lead text-center">{{::data.catItem.name}}</p>
      <ul class="list-unstyled">
        <li class="text-center" ng-if="::data.catItem.price">${Price}: {{::data.catItem.price}}</li>
      </ul>
      <sp-model form-model="::data.catItem" mandatory="mandatory"></sp-model>
      <p ng-if="c.req" class="text-center text-success">
        ${Request created!} <a href="?id={{c.req.page}}&table={{c.req.table}}&sys_id={{c.req.sys_id}}">{{c.req.number}}</a>
      </p>
      <button ng-if="!c.req" class="btn btn-default btn-block" ng-click="c.getIt()">${Get it}</button>
    </div>
  </div>
</div>
```

## GlideSPScriptable - getCatalogItem\(String sysId, Boolean isOrdering\)

Returns a model and view model for a `sc_cat_item` or `sc_cat_item_guide`.

<table id="table_xj4_rw2_3z" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysId

</td><td>

String

</td><td>

The sys\_id of the catalog item \(`sc_cat_item`\) or order guide \(`sc_cat_item_guide`\).

</td></tr><tr><td>

isOrdering

</td><td>

Boolean

</td><td>

When true, uses create roles security check. When false, uses write roles security check.When users are ordering an item or have it in their cart, check using the create roles.

 If users are not ordering, for example, somebody is looking at a requested item to see the variables associated with that item, then check using the write roles.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|An object containing the catalog item variable model, view, sections, pricing, and client scripts.|

## GlideSPScriptable - getDisplayValue\(String fieldName\)

Returns the display value of the specified field \(if it exists and has a value\) from either the widget's `sp_instance` or the `sp_portal` record.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Name of the field|

|Type|Description|
|----|-----------|
|String|The display value from either the `sp_instance` or `sp_portal` record.|

```
//Server script
(function() {
    data.title = $sp.getDisplayValue("title");
    data.catalog = $sp.getDisplayValue("sc_catalog");
})();

//HTML template
<div>
    <h1>sp_instance.title: {{::data.title}}</h1>
    <h1>sp_portal.sc_catalog: {{::data.catalog}}</h1>
</div>
```

## GlideSPScriptable - getField\(GlideRecord now\_GR, String fieldName\)

Returns information about the specified field in the specified GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|GlideRecord|The GlideRecord to check|
|fieldName|String|The field to find information for|

|Type|Description|
|----|-----------|
|Object|An object containing the field's label, value, displayValue, and type. Returns null if the GlideRecord of field name are not valid, or if the field is not readable.|

## GlideSPScriptable - getFields\(GlideRecord now\_GR, String fieldNames\)

Checks the specified list of field names, and returns an array of valid field names.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|GlideRecord|The GlideRecord to check|
|field Names|String|A comma separated list of field names.|

|Type|Description|
|----|-----------|
|Array|An array of valid fields.|

## GlideSPScriptable - getFieldsObject\(GlideRecord now\_GR, String fieldNames\)

Checks the specified list of field names and returns an object of valid field names.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|GlideRecord|The GlideRecord to check|
|field Names|String|A comma separated list of field names.|

|Type|Description|
|----|-----------|
|Object|An object containing valid field names.|

## GlideSPScriptable - getForm\(String tableName, String sysId\)

Return the form associated with the passed table name and record sys\_id.

**Note:** The method enforces cross-scope access privileges to the specified table and associated record.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Name of the table in which the form resides.|
|sysId|String|Sys\_id of the form.|

|Type|Description|
|----|-----------|
|Object|Requested form.|

```
var sp = new GlideSPScriptable('');
var res = sp.getForm('sys_user', '6816f79cc0a8016401c5a33be04be441');    // User sys ID information
gs.info('Name: ' + res._fields.name.value);
gs.info('E-mail: ' + res._fields.email.value);
```

Output:

```
Name: Harry Jones
 E-mail: harryjones@gmail.com
```

## GlideSPScriptable - getKBCategoryArticles\(String sys\_id, Number limit\)

Returns KB articles in the specified category and its subcategories.

To avoid performance issues, do not use this method to return articles in large categories or articles with inline images. Instead, use getKBArticleSummaries\(\).

|Name|Type|Description|
|----|----|-----------|
|sys\_id|String|Sys\_id of the KB article category.|
|limit|Number|Maximum number of KB articles returned.|

<table id="table_l14_331_xbb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

The articles within the category and its subcategories with: -   A **workflow\_state** of **published**.
-   A **valid\_to** date greater than or equal to the current date.

</td></tr></tbody>
</table>```
//Server script 
(function() {
    data.kbs = $sp.getKBCategoryArticles("0ac1bf8bff0221009b20ffffffffffec", 5);
})();

//HTML template
<div>
articles: {{::data.kbs}}
</div>

```

## GlideSPScriptable - getKBCategoryArticleSummaries\(String sys\_id, Number limit, Number maxChars\)

Returns Knowledge Base article summaries in the specified category and its subcategories.

|Name|Type|Description|
|----|----|-----------|
|sys\_id|String|Sys\_id of the KB article category.|
|limit|Number|Maximum number of KB articles returned.|
|maxChars|Number|Maximum number of characters to return from the article text. For full article text, set the value to `-1`.|

<table id="table_k44_gjh_xbb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

The articles within the category and its subcategories with: -   A **workflow\_state** of **published**.
-   A **valid\_to** date greater than or equal to the current date.

</td></tr></tbody>
</table>```
//Server script 
(function() {
    data.summary = $sp.getKBCategoryArticleSummaries("0ac1bf8bff0221009b20ffffffffffec", 5, 200);
})();

//HTML template
<div>
articles: {{::data.summary}}
</div>

```

## GlideSPScriptable - getKBCount\(String sys\_id\)

Returns the number of articles in the defined Knowledge Base.

|Name|Type|Description|
|----|----|-----------|
|sys\_id|String|Sys\_id of a Knowledge Base record.|

<table id="table_l1v_js1_xbb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Number of knowledge articles in the defined Knowledge Base with: -   A **workflow\_state** of **published**.
-   A **valid\_to** date greater than or equal to the current date.

</td></tr></tbody>
</table>```
//Server script 
(function() {
    data.count = $sp.getKBCount("a7e8a78bff0221009b20ffffffffff17");
})();

//HTML template
<div>
articles: {{::data.count}}
</div>

```

## GlideSPScriptable - getListColumns\(String tableName, String view\)

Returns a list of the specified table's columns in the specified view.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Name of the table|
|view|String|The view by which to filter the columns|

|Type|Description|
|----|-----------|
|Object|An object containing the column names.|

## GlideSPScriptable - getMenuItems\(String sysId\)

Returns an array of menu items for the specified instance.

|Name|Type|Description|
|----|----|-----------|
|sysId|String|sysId of the instance|

|Type|Description|
|----|-----------|
|Array|Menu items for the specified instance|

## GlideSPScriptable - getMenuHREF\(GlideRecord page\)

Returns the \(?id=\) portion of the URL based on the sp\_menu type.

|Name|Type|Description|
|----|----|-----------|
|page|GlideRecord|The page|

|Type|Description|
|----|-----------|
|String|The href portion of the URL.|

## GlideSPScriptable - getParameter\(String name\)

Returns the value of the specified parameter.

|Name|Type|Description|
|----|----|-----------|
|name|String|The name of the key from the query string or post body.|

|Type|Description|
|----|-----------|
|Object|Returns the specified parameter as an object. Returns null if there is no request, JSON request, or widget.|

## GlideSPScriptable - getPortalRecord\(\)

Returns the portal record from the Service Portals \[sp\_portal\] table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideRecord|The portal record for the current portal from the Service Portals \[sp\_portal\] table.|

```
//Server script
(function() {
    var portalGr = $sp.getPortalRecord();
    data.logo = portalGr.getDisplayValue("logo");
    data.homepage = portalGr.getDisplayValue("homepage.id");
})();

//HTML template
<div>
    <img ng-src="{{::c.data.logo}}" />
    <a href="?id={{::c.data.homepage}}">Click here to go home</a>
</div>
```

## GlideSPScriptable - getRecord\(String table, String sys\_id\)

If parameters are provided, returns the GlideRecord identified by the provided table and Sys ID. If no parameters are provided, returns the record identified by the current URL.

|Name|Type|Description|
|----|----|-----------|
|table|String|Optional. The table of the record to return. If no parameters are included, returns the table and Sys ID identified by the current URL.|
|sys\_id|String|Optional. The Sys ID of the record to return. If no parameters are included, returns the record identified by the current URL.|

<table id="table_nzs_gfh_jw" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

GlideRecord

</td><td>

If parameters are provided, returns the record identified by the provided table and Sys ID. If no parameters are provided, returns the record identified by the current URL.

 Returns null if the widget is embedded by another widget, or if the record for the provided parameters is not found.

</td></tr></tbody>
</table>```
//Server script 
(function(){ 
var now_GR = $sp.getRecord(); 
data.tableLabel = now_GR.getLabel(); 
})(); 

//HTML template 
<div class="panel-heading"> 
<h4 class="panel-title">${{{data.tableLabel}} details}</h4> 
</div>
```

## GlideSPScriptable - getRecordDisplayValues\(Object data, GlideRecord from, String names\)

Copies display values for the specified fields into the data parameter.

|Name|Type|Description|
|----|----|-----------|
|data|Object|The display values for the specified fields are copied to this object.|
|from|GlideRecord|The GlideRecord to process.|
|names|String|A comma-separated list of field names.|

|Type|Description|
|----|-----------|
|void| |

## GlideSPScriptable - getRecordElements\(Object data, GlideRecord from, String names\)

For the specified fields, copies the element's name, display value, and value into the data parameter.

|Name|Type|Description|
|----|----|-----------|
|data|Object|The element's name, display value, and value for the specified fields are copied to this object.|
|from|GlideRecord|The GlideRecord to process.|
|names|String|A comma-separated list of field names.|

|Type|Description|
|----|-----------|
|void| |

## GlideSPScriptable - getRecordValues\(Object data, GlideRecord from, String names\)

Copies values for the specified field names from the GlideRecord into the data parameter.

|Name|Type|Description|
|----|----|-----------|
|data|Object|The value for the specified fields are copied to this object.|
|from|GlideRecord|The GlideRecord to process.|
|names|String|A comma-separated list of field names.|

|Type|Description|
|----|-----------|
|void| |

## GlideSPScriptable - getRecordVariables\(GlideRecord now\_GR, Boolean includeNilResponses\)

Returns Service Catalog variables associated with a record in String format.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|GlideRecord|The record to retrieve Service Catalog variables for. Must be a record with Service Catalog variables defined, such as a requested item \[sc\_req\_item\] record or an incident submitted through a record producer.|
|includeNilResponses|Boolean|Optional. If true, the API includes variables with no user-defined value.|

|Type|Description|
|----|-----------|
|String|Service Catalog variables associated with the record.|

```
//Server script 
(function() {
var itemsGR = new GlideRecord("sc_req_item");
itemsGR.get('585d1bc44f4f13008a959a211310c77d');
	
data.scVars = $sp.getRecordVariables(itemsGR);

})();

//HTML template
<div>
Requested item variables: {{::data.scVars}}
</div>
```

Output:

```
Requested item variables: [
  {
    "display_value":"MetroPCS",
    "name":"carrier",
    "visible_summary":true,
    "id":"585d1bc44f4f13008a959a211310c77c",
    "label":"Allocated carrier",
    "type":"5",
    "value":"metropcs",
    "visible_standalone":true,
    "visible_guide":true
  },
  {
    "display_value":"Unlimited",
    "name":"data_plan",
    "visible_summary":true,
    "id":"d05d1bc44f4f13008a959a211310c77c",
    "label":"Monthly data allowance",
    "type":"5",
    "value":"unlimited",
    "visible_standalone":true,
    "visible_guide":true
  },
  {
    "display_value":"12 Months",
    "name":"duration",
    "visible_summary":true,
    "id":"d85d1bc44f4f13008a959a211310c77c",
    "label":"Contract duration",
    "type":"5",
    "value":"twelve_months",
    "visible_standalone":true,
    "visible_guide":true
  },
  {
    "display_value":"Slate",
    "name":"color",
    "visible_summary":true,
    "id":"545d1bc44f4f13008a959a211310c77c",
    "label":"Color",
    "type":"5",
    "value":"slate",
    "visible_standalone":true,
    "visible_guide":true
  },
  {"display_value":"64GB",
    "name":"storage",
    "visible_summary":true,
    "id":"d45d1bc44f4f13008a959a211310c77c",
    "label":"Storage",
    "type":"5",
    "value":"sixtyfour",
    "visible_standalone":true,
    "visible_guide":true
  }
]
```

## GlideSPScriptable - getRecordVariablesArray\(GlideRecord now\_GR, Boolean includeNilResponses\)

Returns an array of Service Catalog variables associated with a record.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|GlideRecord|The record to retrieve Service Catalog variables for. Must be a record with Service Catalog variables defined, such as a requested item \[sc\_req\_item\] record or an incident submitted through a record producer.|
|includeNilResponses|Boolean|Optional. If true, the API includes variables with no user-defined value.|

|Type|Description|
|----|-----------|
|Object|Array of Service Catalog variables associated with the record.|

```
//Server script 
(function() {
var itemsGR = new GlideRecord("sc_req_item");
itemsGR.get('585d1bc44f4f13008a959a211310c77d');
	
data.scVars = $sp.getRecordVariablesArray(itemsGR);

})();

//HTML template
<div>
Requested item variables: {{::data.scVars}}
</div>
```

Output:

```
Requested item variables: [
  {
    "display_value":"MetroPCS",
    "name":"carrier",
    "visible_summary":true,
    "id":"585d1bc44f4f13008a959a211310c77c",
    "label":"Allocated carrier",
    "type":"5",
    "value":"metropcs",
    "visible_standalone":true,
    "visible_guide":true
  },
  {
    "display_value":"Unlimited",
    "name":"data_plan",
    "visible_summary":true,
    "id":"d05d1bc44f4f13008a959a211310c77c",
    "label":"Monthly data allowance",
    "type":"5",
    "value":"unlimited",
    "visible_standalone":true,
    "visible_guide":true
  },
  {
    "display_value":"12 Months",
    "name":"duration",
    "visible_summary":true,
    "id":"d85d1bc44f4f13008a959a211310c77c",
    "label":"Contract duration",
    "type":"5",
    "value":"twelve_months",
    "visible_standalone":true,
    "visible_guide":true
  },
  {
    "display_value":"Slate",
    "name":"color",
    "visible_summary":true,
    "id":"545d1bc44f4f13008a959a211310c77c",
    "label":"Color",
    "type":"5",
    "value":"slate",
    "visible_standalone":true,
    "visible_guide":true
  },
  {"display_value":"64GB",
    "name":"storage",
    "visible_summary":true,
    "id":"d45d1bc44f4f13008a959a211310c77c",
    "label":"Storage",
    "type":"5",
    "value":"sixtyfour",
    "visible_standalone":true,
    "visible_guide":true
  }
]
```

## GlideSPScriptable - getStream\(String table, String sysId\)

Gets the activity stream for the specified record. This method works on tables that extend the task table.

|Name|Type|Description|
|----|----|-----------|
|table|String|The table name|
|sysID|String|The sys\_id of the record|

<table id="table_h5b_jmh_jw" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

If a table extending the task table is specified, contains the display\_value, sys\_id, short\_description,number, entries, user\_sys\_id, user\_full\_name, user\_login, label, table, and journal\_fields properties; otherwise contains the table and sys\_id properties.**Note:** The user\_login property contains the User ID of the current user. The user\_sys\_id and iser\_full\_name properties reference the creator of the queried record.

</td></tr></tbody>
</table>## GlideSPScriptable - getUserInitials\(\)

Returns the user's initials.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The user's initials|

## GlideSPScriptable - getValue\(String name\)

Returns the named value of the JSON request, instance, or portal.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the JSON request, instance, or portal.|

|Type|Description|
|----|-----------|
|Object|Value of the specified parameter. Null if the specified entity does not exist or has no such parameter.|

```
//Server script
(function() {
    data.title = $sp.getValue("title");
    data.catalog = $sp.getValue("sc_catalog");
})();

//HTML templage
<div>
    <h1>sp_instance.title: {{::data.title}}</h1>
    <h1>sp_portal.sc_catalog: {{::data.catalog}}</h1>
</div>
```

## GlideSPScriptable - getValues\(Object data, String names\)

Copies values from the request or instance to the data parameter.

|Name|Type|Description|
|----|----|-----------|
|data|Object|Receives the parameter values.|
|names|String|Comma-separated string of field names.|

|Type|Description|
|----|-----------|
|void| |

## GlideSPScriptable - getVariablesArray\(Boolean includeNilResponses\)

Returns an array of Service Catalog variables associated with the record in the URL.

For example, if the URL includes the parameters `id=form&table=sc_req_item&sys_id=832e9620db4f330083766b984b9619cf`, the API returns the variables associated with the given record in the Requested item \[sc\_req\_item\] table. Must be a record with Service Catalog variables defined, such as a requested item \[sc\_req\_item\] record or an incident submitted through a record producer.

|Name|Type|Description|
|----|----|-----------|
|includeNilResponses|Boolean|Optional. If true, the API includes variables with no user-defined value.|

|Type|Description|
|----|-----------|
|Object|Array of variables associated with the table.|

```
//Server script 
(function() {	
data.scVars = $sp.getVariablesArray();
})();

//HTML template
<div
Current record variables: {{::data.scVars}}
</div>
```

Output:

```
Current record variables: [
  {
    "display_value":"unlimited",
    "name":"data","visible_summary":
    true,"id":"472e5620db4f330083766b984b96198a",
    "label":"Data",
    "type":"6",
    "value":"unlimited",
    "visible_standalone":true,
    "visible_guide":true
  },
  {
    "display_value":"Black",
    "name":"color",
    "visible_summary":true,
    "id":"c72e5620db4f330083766b984b96198a",
    "label":"Color",
    "type":"6",
    "value":"Black",
    "visible_standalone":true,
    "visible_guide":true
  }
] 
```

## GlideSPScriptable - getWidget\(String sysID, Object options\)

Gets a widget by id or sys\_id, executes that widget's server script using the provided options, then returns the widget model.

<table id="table_vms_1ph_jw" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysID

</td><td>

String

</td><td>

The widget sys\_id or widget\_id

</td></tr><tr><td>

options

</td><td>

Object

</td><td>

An object to pass to the widget's server script. Refer to this object as `options` in your server script.**Note:** Any options passed into this function will only be available in the embedded widget's server script on the **first execution** of that script. Any subsequent calls into the server script from the embedded widget will not contain the object properties passed in.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|A widget model to be used with sp-widget.|

```
//Server script
data.myWidget = $sp.getWidget('widget_id', {p1: param1, p2: param2});

//HTML
<sp-widget widget="c.data.myWidget"></sp-widget>
```

## GlideSPScriptable - isRTLEnabled\(\)

Checks whether the associated portal is enabled for right-to-left language \(RTL\) and whether the current user's language is directionally RTL.

Use this method to determine if there’s a need for a RTL-specific CSS in the portal UI.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_gtx_1c3_yxb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the RTL flag is enabled and the current user's session language is directionally RTL.Possible values:

-   true: The RTL flag is enabled.
-   false: The RTL flag isn’t enabled.

Data type: Boolean

</td></tr></tbody>
</table>The following code example shows how to use this method to determine the type of icon to display on the portal page.

```
// Server script  
(function() {
  data.isRTLEnabled = $sp.isRTLEnabled();
 })(); 

// HTML template 
<div> <i ng-class="c.data.isRTLEnabled ? 'fa fa-arrow-right' : 'fa fa-arrow-left'"></i> </div> 
```

## GlideSPScriptable - isUserCriteriaEnabled\(\)

Returns true if user criteria is enabled.

This method returns true if the **Service Portal User Criteria Support** plugin \(com.glide.service-portal.user-criteria\) is active and the **Enable use of User Criteria records instead of Roles fields for Service Portal entitlements** \(glide.service\_portal.user\_criteria\_enabled\) system property is set to true.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if user criteria is enabled.|

## GlideSPScriptable - log\(Object message\)

Logs output to the Service Portal Log Entries \[sp\_log\] table. The logged in user must have the sp\_admin or admin role.

|Name|Type|Description|
|----|----|-----------|
|message|Object|JavaScript object or string representing the message to send as output on a Service Portal page.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to log a predefined error if it occurs.

```
var demo_data = null;
var params = null;
if (gr.getValue("demo_data")) {
   try {
	demo_data = JSON.parse(gr.getValue("demo_data"));
	params = (demo_data.options) ? demo_data.options : null;
	} catch(e) {
	$sp.log(e);
   }
}
```

## GlideSPScriptable - mapUrlToSPUrl\(String url\)

Transforms a URL requesting a list or form in the platform UI into the URL of the corresponding `id=list` or `id=form` Service Portal page.

Use this method to perform tasks such as redirecting a user after login to the correct Service Portal page when they request a platform UI form or list URL. Note that the `id=list` and `id=form` page targets are not customizable.

**Note:** Table, sys\_id, and sysparm\_query values are preserved from the original URL; sysparm\_view is not.

|Name|Type|Description|
|----|----|-----------|
|url|String|Platform UI URL|

<table id="table_pdb_whn_p2b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Transformed Service Portal URL.If the passed-in URL does not request a list or a form in the platform UI, a null value is returned.

</td></tr></tbody>
</table>List example

```
GlideSPScriptable().mapUrlToSPUrl("http://demo.service-now.com/task_list.do?sysparm_userpref_module=1523b8d4c611227b00be8216ec331b9a&sysparm_query=assigned_to=javascript:getMyAssignments()&sysparm_clear_stack=true"))
```

Returns

```
id=list&table=task&filter=assigned_to=javascript:getMyAssignments()&sys_id=&v=
```

Form example

```
GlideSPScriptable().mapUrlToSPUrl("incident.do?sys_id=12bc12bc12bc12bc12bc12bc12bc12bc")
```

Returns

```
id=form&table=incident&filter=&sys_id=12bc12bc12bc12bc12bc12bc12bc12bc&v=
```

## GlideSPScriptable - userCanSeeSearchSourceByCriteria\(String searchSourceID\)

Returns true if the current user can see a search source specified by the searchSourceID.

Returns true if the user is not restricted by user criteria. For more detail on how user criteria affects Service Portal assets, see [User criteria for Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/user-criteria.md).

**Note:** This method does not evaluate role-based permissions of the search source, and should only be used if User Criteria is enabled.

|Name|Type|Description|
|----|----|-----------|
|searchSourceID|String|Sys\_id of the search source record.|

|Type|Description|
|----|-----------|
|Boolean|True if current user has read access to the search source.|

