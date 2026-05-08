---
title: REST APIs
description: REST \(REpresentational State Transfer\) is a simple stateless architecture that provides standards between computer systems on the web, making it easier for them to communicate with each other.
locale: en-US
release: australia
product: REST API Explorer
classification: rest-api-explorer
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 17
breadcrumb: [Web services, API implementation, API implementation and reference]
---

# REST APIs

REST \(REpresentational State Transfer\) is a simple stateless architecture that provides standards between computer systems on the web, making it easier for them to communicate with each other.

The ServiceNow AI Platform provides various REST APIs, which are active by default. These APIs provide the ability to interact with various ServiceNow functionality within your application. Such functionality includes the ability to perform create, read, update, and delete \(CRUD\) operations on existing tables \(Table API\), insert data into, retrieve information from, and run transforms against a MetricBase database \(MetricBase Time Series API, and many others.

For a list of available REST APIs, see [REST API reference](../../../build/applications/concept/api-rest.md).

**Note:** You can view inbound API transactions in the Transaction logs. Use a link like the one below to view the transactions for the current day:

`https://<instancename>.service-now.com/syslog_transaction_list.do?sysparm_query=sys_created_onONToday%40javascript%3Ags.beginningOfToday()%40javascript%3Ags.endOfToday()%5Etype%3Drest`

## REST URI format and available parameters

ServiceNow REST APIs follow standard REST API protocol. They also provide "custom" URI and query parameters to ensure backwards compatibility and provide additional functionality such as paginating long lists of results. The following sections describe the functionality behind these custom parameters, which are all optional.

## REST API versioning

ServiceNow REST API URIs may include a version number, such as `/api/now/v1/table/{tableName}`. Version numbers identify the endpoint version that a URI accesses. By specifying a version number in your URIs, you can ensure that future updates to the REST API do not negatively impact your integration.

URIs that do not specify a version number in the URI, such as `/api/now/table/{tableName}`, use the latest REST endpoint for your instance version.

## Supported HTTP request methods

-   GET
-   DELETE
-   HEAD
-   PATCH
-   POST
-   PUT

For details on these methods, refer to the [RFC-2616 Hypertext Transfer Protocol](https://www.rfc-editor.org/rfc/rfc2616#page-51) document.

**Note:**

-   You can use the HEAD methods in place of GET methods to return a response without a response body.
-   You cannot pass multiple records in POST, PUT, and PATCH operations. If you do, only the first record is processed, the rest are ignored.
-   You cannot use POST, PUT, and PATCH to insert or update records into a Database view, as Database views are read-only.

## Data format headers

REST APIs require the **Accept** and **Content-Type** request headers for proper data formatting for requests that contain a request body or response body. POST, PUT, PATCH, and DELETE operations require you to provide both headers. GET and HEAD operations require only the **Accept** header. Failing to provide the required headers results in a `400 Bad Request` error.

For most ServiceNow REST APIs these request headers support the following values:

-   Accept: **application/json**, **application/xml**
-   Content-Type: **application/json**, **application/xml**

For the list of specific values supported by each endpoint, refer to the [REST API reference](../../../build/applications/concept/api-rest.md).

## Other headers

All requests may contain an authentication header that specifies the user credentials to use for authentication.

You can also override HTTP methods, such as GET or POST, by setting the **X-http-method-override** header.

## Special data handling

The following describes some of the data handling nuances within the REST API.

-   How to clear a data field: Except for choice fields, you can pass an empty value in the parameter to clear the value in the database. For example, sending `{"short description":""}` clears the **short\_description** field for the specified record.
-   How currency fields are handled: Returned currency values are converted to the local currency based on the user’s locale. When inserting data, no conversion is performed. This behavior applies to fields of the types `Currency` or `Price`.

    For example, if a user in the UK locale queries records with currency values in USD, the returned values are converted to GBP. However, if this user adds a new record with the currency field value in GBP, the value is stored in GBP without being converted to USD. This GBP value appears in USD if queried by a user in the US locale.

-   UI data display versus values passed in a REST endpoint: The UI shows the database display value, which is manipulated data. A REST endpoint, by default, inserts and updates the actual values, which can be different from the display value. You can force a REST endpoint to treat passed values as display values by setting the [sysparm\_input\_display\_value](c_RESTAPI.md#REST-sysparm_input_display_value-row) request parameter to true.

## Custom query parameters

The ServiceNow REST APIs use the following query parameters across many of the available APIs, providing consistent behavior across the APIs. Use these parameters to paginate large record sets, filter results, and restrict the number of records returned in a single query.

<table id="table_z1v_znb_zhb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

sysparm\_limit

</td><td id="sysparm_limit-entry-RESTAPI">

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. This limit is applied before ACL evaluation. If no records return, including records you have access to, rearrange the record order so records you have access to return first.

**Note:** Unusually large **sysparm\_limit** values can impact system performance.

Data type: Number

Default: 10000

</td></tr><tr><td>

sysparm\_fields

</td><td id="sysparm_fields_entry-RESTAPI">

Comma-separated list of fields to return in the response. Invalid fields are ignored.Data type: String

Default: Return all fields.

</td></tr><tr id="REST-sysparm_input_display_value-row"><td>

sysparm\_input\_display\_value

</td><td id="entry-sysparm_input_display_value-REST_API">

Flag that indicates whether to set field values using the display value or the actual value. Depending on the different types of fields, the endpoint may manipulate the passed in display values to store the proper values in the database. For example, if you send the display name for a reference field, the endpoint stores the sys\_id for that value in the database. For date and time fields, when this parameter is true, the date and time value is adjusted for the current user's timezone. When false, the date and time value is inserted using the GMT timezone.Valid values:

-   true: Treats input values as display values and they are manipulated so they are stored properly in the database.
-   false: Treats input values as actual values and stores them in the database without manipulation.

Data type: Boolean

Default: false - This matches the data type that is returned during data retrieval \(GET methods\), which is the actual values.

**Note:** To set the value of an encrypted field, you must set this parameter to `true`. If this parameter is not set to true, values submitted to encrypted fields are not saved. Additionally, the requesting user must have the appropriate encryption context prior to submitting the request. Encrypted fields are hidden for users without the appropriate encryption context. For more information on field encryption see Encryption.

</td></tr><tr><td>

sysparm\_offset

</td><td id="sysparm_offset-entry-RESTAPI">

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Don't pass a negative number in the **sysparm\_offset** parameter.Data type: Number

Default: 0

</td></tr><tr><td>

sysparm\_query

</td><td id="sysparm-query-RESTAPI">

Encoded query used to filter the result set. You can use a UI filter to obtain a properly encoded query.Syntax: `sysparm_query=<col_name><operator><value>`. Column names, operators, and values are case-sensitive.

-   &lt;col\_name&gt;: Name of the table column to filter on.
-   &lt;operator&gt;: Supports the following values:
    -   `=`: &lt;col\_name&gt; exactly matches &lt;value&gt;.
    -   `!=`: &lt;col\_name&gt; does not match &lt;value&gt;.
    -   `LIKE`: &lt;col\_name&gt; contains the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `STARTSWITH`: &lt;col\_name&gt; starts with the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `ENDSWITH`: &lt;col\_name&gt; ends with the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `^`: AND operator to add an additional query condition. Records included in the result set match both conditions.
    -   `^OR`: OR operator to add an additional query condition. Records included in the result set match at least one of the conditions.
-   &lt;value&gt;: Value to filter on.

For more information about operators, see Operators available for filters and queries.

Queries can contain multiple conditions. For example, the following query returns records where the caller is the current user and the record is active.

`sysparm_query=caller_id=javascript:gs.getUserID()^active=true`

Encoded queries also support order by ascending and descending functionality. To sort responses based on certain fields, use the `ORDERBY` and `ORDERBYDESC` clauses in **sysparm\_query**.

Syntax:

-   `ORDERBY<col_name>`
-   `ORDERBYDESC<col_name>`

For example, the following query gets all active records and orders the results in ascending order by number, and then in descending order by category.

`sysparm_query=active=true^ORDERBYnumber^ORDERBYDESCcategory`

By default, if part of a query is invalid, such as an invalid field name, the instance ignores the invalid part. It then returns rows using only the valid portion of the query. Set the property **glide.invalid\_query.returns\_no\_rows** to `true` to instead return no rows on an invalid query.

**Note:** The **glide.invalid\_query.returns\_no\_rows** property controls the behavior of all queries across the instance, such as in lists, scripts \(GlideRecord.query\(\)\), and web service APIs.

Data type: String

</td></tr><tr><td>

sysparm\_view

</td><td id="sysparm_view-entry-RESTAPI">

UI view for which to render the data. Determines the fields returned in the response.Valid values:

-   desktop
-   mobile
-   both

If you also specify the **sysparm\_fields** parameter, it takes precedent.

Data type: String

</td></tr></tbody>
</table>## Dot-walking in REST API requests

You can use dot-walking when specifying the **sysparm\_query** or **sysparm\_fields** parameters in requests to REST APIs that support those parameters.

**Note:** The Import Set API does not support dot-walking.

## Dot-walking in sysparm\_query

You can filter queries using related record values by dot-walking in the **sysparm\_query** parameter. For example, you can retrieve all incident records where the incident **Company** has a specific **Stock symbol** value.

`https://<instance>.service-now.com/api/now/table/incident?sysparm_query=company.stock_symbol=NYX`

## Dot-walking in sysparm\_fields

You can view field values from multiple tables by dot-walking in the **sysparm\_fields** parameter. For example, you can retrieve the **Name**, **Sys\_id**, and **Department** of each user that has certain roles, as well as the role **Name**.

The request runs on the User Roles \[sys\_user\_has\_role\] table which defines a many-to-many relationship between users and roles. The response includes field values from the User \[sys\_user\] and Roles \[sys\_user\_role\] tables.

`https://<instance>.service-now.com/api/now/table/sys_user_has_role?sysparm_fields=role%2Crole.name%2Cuser%2Cuser.name%2Cuser.sys_id%2Cuser.department&sysparm_query=role%3D3d43716d0f6002003a2d47bce1050e0d%5EORrole%3Dac73b52d0f6002003a2d47bce1050eec&sysparm_display_value=true`

```
{
"result": [
  {
   "user.name": "Fred Johnson",
   "user.sys_id": "f5a3716d0f6002003a2d47bce1050ed4",
   "role.name": "support",
   "user.department": {
      "display_value": "Accounting",
      "link": "https://<instance>.service-now.com/api/now/table/cmn_department/5b3b13530f58c2003a2d47bce1050e96"
    },
   "role": {
      "display_value": "support",
      "link": "https://<instance>.service-now.com/api/now/table/sys_user_role/3d43716d0f6002003a2d47bce1050e0d"
    },
   "user": {
      "display_value": "Fred Johnson",
      "link": "https://<instance>.service-now.com/api/now/table/sys_user/f5a3716d0f6002003a2d47bce1050ed4"
    }
  },
  {
   "user.name": "Fred Johnson",
   "user.sys_id": "f5a3716d0f6002003a2d47bce1050ed4",
   "role.name": "asset_mgmt",
      "user.department": {
      "display_value": "Accounting",
      "link": "https://<instance>.service-now.com/api/now/table/cmn_department/5b3b13530f58c2003a2d47bce1050e96"
     },
    "role": {
       "display_value": "asset_mgmt",
       "link": "https://<instance>.service-now.com/api/now/table/sys_user_role/ac73b52d0f6002003a2d47bce1050eec"
      },
    "user": {
       "display_value": "Fred Johnson",
       "link": "https://<instance>.service-now.com/api/now/table/sys_user/f5a3716d0f6002003a2d47bce1050ed4"
       }
    }
  ]
}
```

## REST API HTTP response codes

Calls made to REST endpoints return HTTP response codes. You can use these response codes to ensure that the REST API executed properly. If it did not, the endpoint returns an error response code. Use the information in the error response to troubleshoot issues with your call format. For a list of standard response codes that an endpoint may return, see [REST API HTTP response codes](../reference/r_RESTAPIHTTPResponseCodes.md). For the list of response codes returned by a specific ServiceNow REST API, see the [REST API reference](../../../build/applications/concept/api-rest.md).

## REST API security

By default, ServiceNow REST APIs use basic authentication or OAuth to authorize user access to REST APIs/endpoints. You can also configure your instance to use [multi-factor authentication](c_RESTAPI.md#multi-factor-auth-inbound-REST) to access REST APIs.

The user ID that you specify in a REST endpoint call is subject to access control in the same way as an interactive user. Each request requires the proper authentication information, such as user name and password. Ensure that each endpoint request includes an Authorization header with sufficient credentials to access the endpoint.

ServiceNow REST APIs also support cookies that enable binding to the existing session.

To use the certificate to call the API and information on mutual authentication, see Certificate-based authentication.

REST API access policies with the filter criterias such as IP, role, group and restrict the scope of API you can use the REST API Auth Scope. To know more about REST API access policy, see REST API access policies.

You can craft one single policy to block the incoming request, at a global REST API level by using the REST API Access policy from outside trusted network and at a basic REST authentication levels.

## REST API roles

In addition to user authentication, each REST endpoint can have different requirements for the roles required to access the endpoint. Some require the admin role and others require API specific roles. Role requirements are specified in the access control list \(ACL\) associated with the REST API/endpoint. For specifics on the valid roles for each REST API/endpoint, refer to the [REST API reference](../../../build/applications/concept/api-rest.md) or locate the associated ACL for the API/endpoint within an instance through **System Security** &gt; **Access Control \(ACL\)**.

## REST API ACLs

REST API ACLs define criteria, such as the roles needed and conditions that a user must meet to access a ServiceNow REST API or endpoint. A single ACL may be defined for an entire REST API, such as the Table API and Attachment API ACLs, or for an individual endpoint, such as the clotho\_rest\_put ACL that only applies to MetricBase PUT methods.

The following ServiceNow REST API ACLs are available in the base system but are deactivated by default. All other ServiceNow REST API ACLs are active by default.

-   Table API
-   Aggregate API
-   Import Set API
-   Attachment API

For additional information on ACLs, see Access control list rules.

**Important:** You should never modify the names of REST API ACLs.

## REST API table access

By default, all tables, including base system tables, global tables, and scoped tables are accessible through web services. You must fulfill any web service security requirements, such as basic authentication and ACLs to access tables through web services. Fields for which the calling entity does not have rights to because of ACLs are not returned in a REST query response.

To allow access to tables without any authentication or authorization, add the table name to the Public Pages \[sys\_public\] table with a status of **Active**. The REST interface still enforces any defined ACLs on associated tables. If ACL enforcement is not the desired behavior, you must deactivate the ACLs on the tables. However, making your APIs public is not suggested because doing so allows the public access to update data in the instance.

You can also control direct web service access to tables using the **Allow access to this table via web services** check box on the table application access settings. You must select this check box to enable web service interaction with the table.

**Note:** The application access fields controlling CRUD operations, such as **Can read** or **Can create** do not apply to web service requests.

## Multi-factor authentication for inbound REST

From Yokohama release, Multi-factor authentication \(MFA\) is not required by default for REST API authentication using Basic Authentication. To know more, see this [KB article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1745551).

## Multi-factor authentication REST responses

The response to an MFA authentication request varies depending on the validity of the provided credentials and MFA token.

|Result|Description|
|------|-----------|
|Basic auth credentials and MFA token are valid|User is authenticated and the session created. The request is processed normally.|
|Basic auth credentials are valid but MFA token is invalid or missing|Response returns error 401. The response includes the X-MFA\_TOKEN header with the value **invalid**.|
|Basic auth credentials are invalid|Response returns error 401. The X-MFA\_TOKEN header is not included in the response.|

## REST API CORS support

The REST API supports cross-origin resource sharing \(CORS\) security. CORS support allows you to define which domains can access each REST API. By defining a CORS rule for a domain, you can allow cross-origin requests from that domain. Cross-origin requests cannot be made from domains without a CORS rule.

**Note:** CORS support applies only to REST APIs, including scripted REST web services. Other web service APIs, such as the SOAP API, do not support CORS.

You can configure CORS to allow access to only certain APIs/endpoints, HTTP methods, and headers from other domains. For example, you can limit requests to the Table API from a specific domain to allow only GET operations.

To view the CORS rules defined on your instance, navigate to **System Web Services** &gt; **CORS Rules**.

You can disable CORS support for an instance by setting the **glide.rest.cors.enabled** property to **false**. When **false**, no CORS evaluation is performed on incoming REST requests. This property is **true** by default.

## REST API Explorer

The REST API Explorer is a ServiceNow tool that uses information from your instance to provide a list of endpoints, methods, and variables that you can use to build and send REST requests.

After you build the request, the REST API Explorer provides code samples in multiple programming languages that you can use to initiate the request, and detailed request and response information.

To access the REST API Explorer, in your instance, navigate to **System Web Services** &gt; **REST API Explorer**. You must have the rest\_api\_explorer role to access the REST API Explorer. For additional information, see [Use the REST API Explorer](use-REST-API-Explorer.md).

**Warning:** The REST API Explorer interacts with data on the current instance. Use caution when working with requests that create, edit, or delete data on a production instance.

## Automated Test Framework support

The Automated Test Framework \(ATF\) supports inbound REST test steps. You can create automated tests for custom inbound REST APIs that you create. Creating tests for your custom REST APIs simplifies upgrade testing, and makes it possible to verify that modifications to a REST API are backward compatible.

## Example REST client applications

Several example REST client applications and source code are available to demonstrate integrations using REST web services. The example REST client applications demonstrate how to use the ServiceNow REST API with an external application, such as a NodeJS or iOS application.

**Important:** These applications are provided only as a demonstration of the REST functionality and are not officially supported.

The examples are open source and available to the community. You can use these example applications to help familiarize yourself with the REST functionality, or use them as a starting point to create your own REST client applications.

Users with the rest\_api\_explorer role can access the list of available client applications by navigating to **System Web Services** &gt; **REST** &gt; **Example Client Apps**.

When viewing the list of applications, click an application to view the source code and additional documentation hosted on GitHub.

## Developer training

On the ServiceNow® Developer Site, you can get training for [Inbound REST integrations](https://developer.servicenow.com/app.do#!/training/article/app_store_learnv2_rest_rome_inbound_rest_integrations/app_store_learnv2_rest_rome_inbound_integrations_in_servicenow_objectives?v=vancouver) and [Outbound REST integrations](https://developer.servicenow.com/app.do#!/training/article/app_store_learnv2_rest_rome_outbound_rest_integrations/app_store_learnv2_rest_rome_outbound_integrations_in_servicenow_objectives?v=vancouver).

## Additional information

The remainder of the REST API section contains "how to" topics that describe specific implementations using the ServiceNow REST API and provides reference information that describes various data elements used by the ServiceNow REST API.

-   **[Use the REST API Explorer](use-REST-API-Explorer.md)**  
In this tutorial you will use the REST API Explorer to test the ServiceNow REST APIs.
-   **[Inbound REST API rate limiting](inbound-REST-API-rate-limiting.md)**  
To prevent excessive inbound REST API requests, set rules that limit the number of inbound REST API requests processed per hour. You can create rules to limit requests for specific users, users with specific roles, or all users.
-   **[Debug in-bound REST queries](debugging-rest-queries.md#)**  
You can debug in-bound REST queries by reviewing the session debug log.
-   **[Return session debug logs in a REST response](rest-session-debug-header.md)**  
You can include session debug logs in a REST response body by passing the X-WantSessionDebugMessages header in the request.
-   **[CORS domain requirements](../reference/r_CORSDomainRequirements.md)**  
When you define a cross-origin resource sharing \(CORS\) rule, the value you enter in the **Domain** field must meet certain requirements. Each CORS rule supports a single wildcard to match incoming Origin headers.
-   **[Define a CORS rule](../task/t_DefineACORSRule.md)**  
You can define a CORS rule to control which domains can access REST API endpoints and other web resources.
-   **[Enable OAuth with inbound REST](../task/t_EnableOAuthWithREST.md)**  
Using OAuth, you can pass a user ID and password once, and then use a token for subsequent REST requests instead of submitting credentials with each request.
-   **[REST API HTTP response codes](../reference/r_RESTAPIHTTPResponseCodes.md)**  
REST messages sent to an instance return a specific HTTP response code.
-   **[Scripted REST APIs](../../custom-web-services/concept/c_CustomWebServices.md)**  
The scripted REST API feature allows application developers to build custom web service APIs.

**Parent Topic:**[Web services](../../web-services/reference/r_AvailableWebServices.md)

**Related topics**  


[REST API FAQ](https://support.servicenow.com/kb_view.do?sysparm_article=KB0535048)

