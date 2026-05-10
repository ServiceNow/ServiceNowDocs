---
title: Knowledge Management REST API
description: The Knowledge Management API provides endpoints for searching, viewing, and fetching lists of the most-viewed and featured knowledge articles.Returns a list of knowledge base \(KB\) articles which can be searched and filtered using various parameters.Returns a knowledge article attachment as a file.Returns a list of the most-viewed knowledge articles and featured knowledge articles.Returns specific knowledge article content and its field values.Returns a list of knowledge articles prioritized by most-viewed.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 27
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Knowledge Management REST API

The Knowledge Management API provides endpoints for searching, viewing, and fetching lists of the most-viewed and featured knowledge articles.

You can only use this API when the Knowledge API \(sn\_km\_api\) plugin is activated. The Knowledge Management REST API was originally released in Orlando using the Knowledge API app available in the ServiceNow Store.

**Note:** The Knowledge Management REST API is publicly accessible and makes any knowledge base that is publicly accessible available to all users, including unauthenticated users. For version 1.0.1 and later, the API was made editable, allowing admins to configure each endpoint to disallow unauthenticated access by selecting the **Requires Authentication** flag on the Scripted REST Service Security tab associated with the API.

To enable other domains to use Knowledge Management REST API endpoints, define a Cross-Origin Resource Sharing \(CORS\) rule. For more information, see [Define a CORS rule](../task/t_DefineACORSRule.md).

To view an article from the scoped knowledge base using this REST API, allow the sn\_km\_api scope read access from the requesting scope in the Restricted Caller Access Privileges \[sys\_restricted\_caller\_access\] table. For more information, see [Define cross-scope access to an application resource](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/set-RCA-level.md).

By default, this API has a rate limit of 500 per hour for unauthenticated and snc\_external users. For more information about rate limiting, see [Inbound REST API rate limiting](inbound-REST-API-rate-limiting.md).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Knowledge Management - GET /knowledge/articles

Returns a list of knowledge base \(KB\) articles which can be searched and filtered using various parameters.

### URL format

Versioned URL: `/api/sn_km_api/{api_version}/knowledge/articles`

Default URL: `/api/sn_km_api/knowledge/articles`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

filter

</td><td>

Encoded query to use to filter the result set. Syntax: `filter=<attr><operator><value>`.

 -   `<attr>`: Name of the table column.
-   `<operator>`:

Valid values:

    -   =: Exactly matches &lt;value&gt;.
    -   !=: Does not match &lt;value&gt;.
    -   ^: Enables you to specify more than one condition and logically AND them.
    -   ^OR: Enables you to specify more than one condition and logically OR them.
    -   LIKE: &lt;attr&gt; contains the specified string. Only works for &lt;attr&gt; fields whose data type is string.
    -   STARTSWITH: &lt;attr&gt; starts with the specified string. Only works for &lt;attr&gt; fields whose data type is string.
    -   ENDSWITH: &lt;attr&gt; ends with the specified string. Only works for &lt;attr&gt; fields whose data type is string.
-   `<value>`: Value to match against.

 All parameters are case-sensitive. Query can contain more than one entry, such as `filter=<attr><operator><value>[<operator><attr><operator><value>]`.

 Data type: String

 Default: empty

</td></tr><tr><td>

fields

</td><td>

Comma-separated list of fields from the Knowledge \[kb\_knowledge\] table to show details in results.Data type: String

 Default: None

</td></tr><tr><td>

kb

</td><td>

Comma-separated list of knowledge base sys\_ids from the Knowledge Bases \[kb\_knowledge\_base\] table to restrict results to.Data type: String

</td></tr><tr id="km-api-parm-lang"><td>

language

</td><td>

List of comma-separated languages in two-letter ISO 639-1 language code format to restrict results to. Alternatively type 'all' to search in all valid installed languages on an instance.Data type: String

 Default: User's session language or en

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. Unusually large **limit** values can impact system performance. For requests that exceed this number of records, use the **offset** parameter to paginate record retrieval.Data type: Number

 Default: 30

</td></tr><tr id="km-api-parm-off"><td>

offset

</td><td>

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time this endpoint is called, **offset** is set to "0". To page through all available records, use `offset=offset+limit` until the end of the all records is reached.

 Data type: Number

 Default: 0

</td></tr><tr><td>

query

</td><td>

Text to search for, can be empty.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

articles

</td><td>

List of articles returned in response.Data type: Array

 ```
"articles": [
  {
    "fields": {Object},
    "link": "String",
    "id": "String",
    "number": "String",
    "rank": Number,
    "score": Number,
    "snippet": "String",
    "title": "String"
  }
]
```

</td></tr><tr><td>

articles.fields

</td><td id="km-resp-fields">

Values of requested fields, if any.Data type: Object

 ```
"fields": {
  "<field_name>": {Object}
}
```

</td></tr><tr><td>

articles.fields.&lt;field\_name&gt;

</td><td id="km-resp-fields_fieldname">

Lists each field requested using the fields parameter, if any.Data type: Object

 ```
"<field_name>": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

articles.fields.&lt;field\_name&gt;.display\_value

</td><td id="km-resp-fieldName-display">

Display value of the requested field.Data type: String

</td></tr><tr><td>

articles.fields.&lt;field\_name&gt;.label

</td><td id="km-resp-fieldName-label">

Label representing the requested field. For example, `Knowledge`.Data type: String

</td></tr><tr><td>

articles.fields.&lt;field\_name&gt;.name

</td><td id="km-resp-fieldName-name">

Name of the requested field. Matches **&lt;field\_name&gt;**.Data type: String

</td></tr><tr><td>

articles.fields.&lt;field\_name&gt;.type

</td><td id="km-resp-fieldName-type">

Data type of requested field.Data type: String

</td></tr><tr><td>

articles.fields.&lt;field\_name&gt;.value

</td><td id="km-resp-fields-fieldName-val">

Value of the requested field.Data type: String

</td></tr><tr><td>

articles.id

</td><td id="km_kb_id">

Knowledge article sys\_id from the Knowledge \[kb\_knowledge\] table.Data type: String

</td></tr><tr><td>

articles.link

</td><td>

Link to the article.Data type: String

</td></tr><tr><td>

articles.number

</td><td>

Knowledge article number.Data type: String

</td></tr><tr><td>

articles.rank

</td><td>

Search rank of article specific to this search.Data type: Number \(Float\)

</td></tr><tr><td>

articles.snippet

</td><td>

Text showing a small portion of the knowledge article.Data type: String

</td></tr><tr><td>

articles.score

</td><td>

Relevancy score, results sorted in descending order by score.Data type: String

</td></tr><tr><td>

articles.title

</td><td id="km_kb_sdesc">

Short description or title of the knowledge article.Data type: String

</td></tr><tr><td>

meta

</td><td>

Meta information of the results and request parameters.Data type: Object

 ```
"meta": {
  "count": Number,
  "end": Number,
  "fields": "String",
  "filter": "String",
  "kb": "String",
  "language": "String",
  "query": "String",
  "start": Number,
  "status": {Object},
  "ts_query_id": "String"
}
```

</td></tr><tr><td>

meta.count

</td><td>

Number of available KB articles.Data type: Number

</td></tr><tr><td>

meta.end

</td><td>

Ending index of the result set.Data type: Number

</td></tr><tr><td>

meta.fields

</td><td>

Fields in the article.Data type: String

</td></tr><tr><td>

meta.filter

</td><td>

Filter used to acquire the data.Data type: String

</td></tr><tr><td>

meta.kb

</td><td>

List of knowledge base article sys\_ids.Data type: String

</td></tr><tr><td>

meta.language

</td><td>

List of comma-separated languages of the KB articles that were requested.Data type: String

</td></tr><tr><td>

meta.query

</td><td>

Specified request query.Data type: String

</td></tr><tr><td>

meta.start

</td><td>

Starting index of result set.Data type: Number

</td></tr><tr><td>

meta.status

</td><td>

Status of the call.Data type: String

</td></tr><tr><td>

meta.ts\_query\_id

</td><td>

Sys\_id of the query.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_km_api/knowledge/articles?query=Windows&limit=2&fields=short_description&fields=sys_class_name" \
--request GET \
--header "Accept:application/xml" \
--user "username":"password"
```

```
{
  "result": {
    "meta": {
      "start": 0,
      "end": 2,
      "fields": "short_description,sys_class_name",
      "query": "Windows",
      "filter": "",
      "kb": "",
      "language": "en",
      "count": 19,
      "ts_query_id": "7976f36129c30410f877796e70786991",
      "status": {
        "code": 200
      }
    },
    "articles": [
      {
        "link": "?sys_kb_id=9e528db1474321009db4b5b08b9a71a6&id=kb_article_view&sysparm_rank=1&sysparm_tsqueryId=7976f36129c30410f877796e70786991",
        "rank": 1,
        "id": "kb_knowledge:9e528db1474321009db4b5b08b9a71a6",
        "title": "Windows: Should I upgrade to Windows 8.x?",
        "snippet": "    Should I upgrade to <B>Windows</B> 8.x? <B>Windows</B> 8.x is designed for using touch, mouse, and keyboard the <B>Windows</B> Store and access apps such as Calendar, Mail, and Messaging. By most accounts, <B>Windows</B> boot times, smaller memory footprint, and more free memory for the programs you run. <B>Windows</B>",
        "score": 14.869,
        "number": "KB0000020",
        "fields": {
          "short_description": {
            "display_value": "Windows: Should I upgrade to Windows 8.x?\n\t\t",
            "name": "short_description",
            "label": "Short description",
            "type": "string",
            "value": "Windows: Should I upgrade to Windows 8.x?\n\t\t"
          },
          "sys_class_name": {
            "display_value": "Knowledge",
            "name": "sys_class_name",
            "label": "Class",
            "type": "sys_class_name",
            "value": "kb_knowledge"
          }
        }
      },
      {
        "link": "?sys_kb_id=3b07857187032100deddb882a2e3ec20&id=kb_article_view&sysparm_rank=2&sysparm_tsqueryId=7976f36129c30410f877796e70786991",
        "rank": 2,
        "id": "kb_knowledge:3b07857187032100deddb882a2e3ec20",
        "title": "What is the Windows key?",
        "snippet": "What is the <B>Windows</B> key? The <B>Windows</B> key is a standard key on most keyboards on computers built to use a <B>Windows</B> operating system. It is labeled with a <B>Windows</B> logo, and is usually placed between on the right side as well. Pressing Win (the <B>Windows</B> key) on its own will do the following: <B>Windows</B> 8.x: Toggle",
        "score": 13.4826,
        "number": "KB0000017",
        "fields": {
          "short_description": {
            "display_value": "What is the Windows key?\t\t",
            "name": "short_description",
            "label": "Short description",
            "type": "string",
            "value": "What is the Windows key?\t\t"
          },
          "sys_class_name": {
            "display_value": "Knowledge",
            "name": "sys_class_name",
            "label": "Class",
            "type": "sys_class_name",
            "value": "kb_knowledge"
          }
        }
      }
    ]
  }
}

```

## Knowledge Management - GET /knowledge/articles/\{article\_sys\_id\}/attachments/\{attachment\_sys\_id\}

Returns a knowledge article attachment as a file.

### URL format

Versioned URL: `/api/sn_km_api/{api_version}/knowledge/articles/{article_sys_id}/attachments/{attachment_sys_id}`

Default URL: `/api/sn_km_api/knowledge/articles/{article_sys_id}/attachments/{attachment_sys_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

article\_sys\_id

</td><td>

Sys\_id of the knowledge article with the attachment you intend to retrieve.Data type: String

Table: Knowledge Bases \[kb\_knowledge\]

</td></tr><tr><td>

attachment\_sys\_id

</td><td>

Sys\_id of record to which the attachment belongs.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|Content-Type|The content type of the response, for example, `image/gif` or `*/*`.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

|Name|Description|
|----|-----------|
|File is returned as a response.| |

### Sample cURL request

```
curl "https://instance.service-now.com/api/sn_km_api/knowledge/articles/0b48fd75474321009db4b5b08b9a71c2/attachments/fedf5614294f4010f877796e70786956" \
--request GET \
--header "Accept:*/*" \
--user "username":"password"
```

```
Binary response not shown (file is returned as a response).
```

## Knowledge Management - GET /knowledge/articles/featured

Returns a list of the most-viewed knowledge articles and featured knowledge articles.

### URL format

Versioned URL: `/api/sn_km_api/{api_version}/knowledge/articles/featured`

Default URL: `/api/sn_km_api/knowledge/articles/featured`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="km-api-parm-fields"><td>

fields

</td><td>

Comma-separated list of fields from the Knowledge \[kb\_knowledge\] table to show details in results.Data type: String

 Default: None

</td></tr><tr id="km-api-parm-kb"><td>

kb

</td><td>

Comma-separated list of knowledge base sys\_ids from the Knowledge Bases \[kb\_knowledge\_base\] table to restrict results to.Data type: String

</td></tr><tr id="km-api-parm-lang"><td>

language

</td><td>

List of comma-separated languages in two-letter ISO 639-1 language code format to restrict results to. Alternatively type 'all' to search in all valid installed languages on an instance.Data type: String

 Default: User's session language or en

</td></tr><tr id="km-api-parm-limit"><td>

limit

</td><td>

Maximum number of records to return. Unusually large **limit** values can impact system performance. For requests that exceed this number of records, use the **offset** parameter to paginate record retrieval.Data type: Number

 Default: 30

</td></tr><tr id="km-api-parm-off"><td>

offset

</td><td>

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time this endpoint is called, **offset** is set to "0". To page through all available records, use `offset=offset+limit` until the end of the all records is reached.

 Data type: Number

 Default: 0

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

articles

</td><td>

List of articles returned in response.Data type: Array

 ```
"articles":[
  {
    "fields": {Object},
    "id": "String",
    "link": "String",
    "number": "String",
    "rank": Number,
    "score": Number,
    "snippet": "String",
    "title": "String"
  }
]
```

</td></tr><tr><td>

articles.fields

</td><td id="km-resp-fields">

Values of requested fields, if any.Data type: Object

 ```
"fields": {
  "<field_name>": {Object}
}
```

</td></tr><tr><td>

articles.fields.&lt;field\_name&gt;

</td><td id="km-resp-fields_fieldname">

Lists each field requested using the fields parameter, if any.Data type: Object

 ```
"<field_name>": {
  "display_value": "String",
  "name": "String",
  "label": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

articles.fields.&lt;field\_name&gt;.display\_value

</td><td id="km-resp-fieldName-display">

Display value of the requested field.Data type: String

</td></tr><tr><td>

articles.fields.&lt;field\_name&gt;.name

</td><td id="km-resp-fieldName-name">

Name of the requested field. Matches **&lt;field\_name&gt;**.Data type: String

</td></tr><tr><td>

articles.fields.&lt;field\_name&gt;.label

</td><td id="km-resp-fieldName-label">

Label representing the requested field. For example, `Knowledge`.Data type: String

</td></tr><tr><td>

articles.fields.&lt;field\_name&gt;.type

</td><td id="km-resp-fieldName-type">

Data type of requested field.Data type: String

</td></tr><tr><td>

articles.fields.&lt;field\_name&gt;.value

</td><td id="km-resp-fields-fieldName-val">

Value of the requested field.Data type: String

</td></tr><tr><td>

articles.id

</td><td id="km_kb_id">

Knowledge article sys\_id from the Knowledge \[kb\_knowledge\] table.Data type: String

</td></tr><tr><td>

articles.link

</td><td>

Link to the article.Data type: String

</td></tr><tr><td>

articles.number

</td><td>

Knowledge article number.Data type: String

</td></tr><tr><td>

articles.rank

</td><td>

Search rank of article specific to this search.Data type: Number \(Float\)

</td></tr><tr><td>

articles.score

</td><td>

Relevancy score, results sorted in descending order by score.Data type: String

</td></tr><tr><td>

articles.snippet

</td><td>

Text showing a small portion of the knowledge article.Data type: String

</td></tr><tr><td>

articles.title

</td><td id="km_kb_sdesc">

Short description or title of the knowledge article.Data type: String

</td></tr><tr><td>

meta

</td><td>

Meta information of the results and request parameters.Data type: Object

 ```
"meta": {
  "count": Number,
  "end": Number,
  "fields": "String",
  "filter": "String",
  "kb": "String",
  "language": "String",
  "query": "String",
  "start": Number,
  "status": {Object},
  "ts_query_id": "String"
}
```

</td></tr><tr><td>

meta.count

</td><td>

Number of available KB articles.Data type: Number

</td></tr><tr><td>

meta.end

</td><td>

Ending index of the result set.Data type: Number

</td></tr><tr><td>

meta.fields

</td><td>

Fields in the article.Data type: String

</td></tr><tr><td>

meta.filter

</td><td>

Filter used to acquire the data.Data type: String

</td></tr><tr><td>

meta.kb

</td><td>

List of knowledge base article sys\_ids.Data type: String

</td></tr><tr><td>

meta.language

</td><td>

List of comma-separated languages of the KB articles that were requested.Data type: String

</td></tr><tr><td>

meta.query

</td><td>

Specified request query.Data type: String

</td></tr><tr><td>

meta.start

</td><td>

Starting index of result set.Data type: Number

</td></tr><tr><td>

meta.status

</td><td>

HTTP status of the call.Data type: String

</td></tr><tr><td>

meta.ts\_query\_id

</td><td>

Sys\_id of the query.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_km_api/knowledge/articles/featured?fields=short_description&limit=3" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  "result": {
    "meta": {
      "start": 0,
      "end": 3,
      "fields": "short_description",
      "query": "homepage",
      "filter": "",
      "kb": "",
      "language": "en",
      "status": {
        "code": 200
      },
      "count": 2
    },
    "articles": [
      {
        "link": "?id=kb_article_view&sys_kb_id=f27d7f79c0a8011b0018f9d700d2b9aa",
        "id": "kb_knowledge:f27d7f79c0a8011b0018f9d700d2b9aa",
        "title": "Email Interruption Tonight at 11:00 PM Eastern",
        "snippet": " If the site is UP but you cant access the page, try one of the below solutions: Browser Related Problems Force a full refresh for the site. This can be achieved by pressing CTRL + F5 keys at the same time on your favourite browser (Firefox, Chrome, Explorer, etc.) Try alternative urls such as m.outlook.com Clear the temporary cache and cookies ",
        "score": -1,
        "number": "KB0000002",
        "fields": {
          "short_description": {
            "display_value": "Email Interruption Tonight at 11:00 PM Eastern\n\t\t",
            "name": "short_description",
            "label": "Short description",
            "type": "string",
            "value": "Email Interruption Tonight at 11:00 PM Eastern\n\t\t"
          }
        }
      },
      {
        "link": "?id=kb_article_view&sys_kb_id=f2765f9fc0a8011b0120ec1b352bf09b",
        "id": "kb_knowledge:f2765f9fc0a8011b0120ec1b352bf09b",
        "title": "Sales Force Automation is DOWN",
        "snippet": "  On Friday, January 20th, we experienced a widespread outage that affected all Zoho services. The outage started around 8:13 am Pacific Time. Zoho services started coming back online for customer use at 3:49 pm, and all services were fully restored at 6:22 pm PST. We absolutely realize how important our services are for businesses and users who",
        "score": -1,
        "number": "KB0000001",
        "fields": {
          "short_description": {
            "display_value": "Sales Force Automation is DOWN",
            "name": "short_description",
            "label": "Short description",
            "type": "string",
            "value": "Sales Force Automation is DOWN"
          }
        }
      }
    ]
  }
}

```

## Knowledge Management - GET /knowledge/articles/\{id\}

Returns specific knowledge article content and its field values.

### URL format

Versioned URL: `/api/sn_km_api/{api_version}/knowledge/articles/{id}`

Default URL: `/api/sn_km_api/knowledge/articles/{id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id or knowledge base \(KB\) number of a knowledge article.Data type: String

Table: Knowledge \[kb\_knowledge\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="km-api-parm-fields"><td>

fields

</td><td>

Comma-separated list of fields from the Knowledge \[kb\_knowledge\] table to show details in results.Data type: String

Default: None

</td></tr><tr><td>

language

</td><td>

Two letter ISO 639-1 language code; for example, "fr" for French. Results display only when searches use the knowledge article KB number as the **id** and a translated version of the article is available in the language specified.**Note:** Only valid when setting the **id** parameter as a KB number \(not sys\_id\).

Data type: String

</td></tr><tr><td>

search\_id

</td><td>

Optional unless using **search\_rank**. Unique identifier of search that returned this article.You can retrieve **search\_id** using one of the following APIs that returns the **articles.id** element:

-   [Knowledge Management - GET /knowledge/articles](knowledge-api.md#)
-   [Knowledge Management - GET /knowledge/articles/featured](knowledge-api.md#)
-   [Knowledge Management - GET knowledge/articles/most\_viewed](knowledge-api.md#)

Passing the **search\_id** and **search\_rank** parameter increments the article view count and records an entry for the article in the Knowledge Use \[kb\_use\] table. You can also verify incremented view counts in Knowledge Base \[kb\_view2\] page.

Data type: String

</td></tr><tr><td>

search\_rank

</td><td>

Optional unless using **search\_id**. Article [search rank](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/c_DocumentScoring.md) by click-rate that you can retrieve using one of the following APIs that returns the **articles.rank** element:-   [Knowledge Management - GET /knowledge/articles](knowledge-api.md#)
-   [Knowledge Management - GET /knowledge/articles/featured](knowledge-api.md#)
-   [Knowledge Management - GET knowledge/articles/most\_viewed](knowledge-api.md#)

Data type: Number

</td></tr><tr><td>

update\_view

</td><td>

Update view count and record an entry for the article in the Knowledge Use \[kb\_use\] table. True whether present as a standalone parameter or set to true. **Note:** If you pass **update\_view** with **search\_id** and **search\_rank**, **update\_view** is ignored because the view count will already be incremented.

Data type: Boolean that is always handled as true when passed whether set to `"true"`, `"false"`, or not set at all.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attachments

</td><td>

Provides attachment details for each instance if attachment exists.Only displays if `display_attachments = true`.

Data type: Array of Objects

```
"attachments": [
  {
    "file_name": "String",
    "size_bytes": "String",
    "state": "String",
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

attachments.file\_name

</td><td>

File name of attachment.Data type: String

</td></tr><tr><td>

attachments.size\_bytes

</td><td>

File size.Data type: String

Unit: Bytes

</td></tr><tr><td>

attachments.state

</td><td>

State.Possible values:

-   available
-   available\_conditionally
-   not\_available
-   pending

Data type: String

</td></tr><tr><td>

attachments.sys\_id

</td><td>

Sys\_id of the attachment.Data type: String

</td></tr><tr><td>

content

</td><td>

Entire HTML content of the article.Data type: String

</td></tr><tr><td>

display\_attachments

</td><td>

Flag that indicates whether the **display\_attachments** flag is active for that article. Attachments are returned only if **display\_attachments** is true \(active\) in the knowledge article record.-   true: **display\_attachments** is active.
-   false: **display\_attachments** is inactive.

Data type: Boolean

</td></tr><tr><td>

embedded\_content

</td><td>

Lists each attachment containing embedded content by sys\_id and includes relevant attachment information.Only displays if `display_attachments = true`.

Data type: Array of Objects

```
"attachments": [
  {
    "file_name": "String",
    "size_bytes": "String",
    "state": "String",
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

embedded\_content.file\_name

</td><td>

File name of the attachment.Data type: String

</td></tr><tr><td>

embedded\_content.size\_bytes

</td><td>

Size of the attachment.Data type: String

Unit: Bytes

</td></tr><tr><td>

embedded\_content.state

</td><td>

State of the attachment. Possible values:

-   available
-   available\_conditionally
-   not\_available
-   pending

Data type: String

</td></tr><tr><td>

embedded\_content.sys\_id

</td><td>

Sys\_id of the attachment.Data type: String

</td></tr><tr><td>

fields

</td><td>

Values of requested fields \(if any\).Data type: Object

```
"fields": {
  "<field_name>": {Object}
}
```

</td></tr><tr><td>

fields.&lt;field\_name&gt;

</td><td>

Lists each field requested using the fields parameter, if any.Data type: Object

```
"<field_name>": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

fields.&lt;field\_name&gt;.display\_value

</td><td>

Display value of the requested field.Data type: String

</td></tr><tr><td>

fields.&lt;field\_name&gt;.label

</td><td>

Label representing the requested field. For example, `Knowledge`.Data type: String

</td></tr><tr><td>

fields.&lt;field\_name&gt;.name

</td><td>

Name of the requested field. Matches **&lt;field\_name&gt;**.Data type: String

</td></tr><tr><td>

fields.&lt;field\_name&gt;.type

</td><td>

Data type of requested field.Data type: String

</td></tr><tr><td>

fields.&lt;field\_name&gt;.value

</td><td>

Value of the requested field.Data type: String

</td></tr><tr><td>

language

</td><td>

Two-letter ISO 639-1 language code for the current article \(if translation is available\).Data type: String

</td></tr><tr><td>

languages

</td><td>

For each translated version of a knowledge article \(if translated\):```
"languages": [
  {
    "label": "String",
    "language": "String",
    "sys_id": "String"
  }
]
```

 Data type: Array

</td></tr><tr><td>

languages.label

</td><td>

String representation for language.Data type: String

</td></tr><tr><td>

languages.language

</td><td>

Two-letter ISO 639-1 code language.Data type: String

</td></tr><tr><td>

languages.sys\_id

</td><td>

Unique identifier for translated version of knowledge article.Data type: String

</td></tr><tr><td>

number

</td><td>

Article number.Data type: String

</td></tr><tr><td>

short\_description

</td><td>

Short description or title of the knowledge article.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Knowledge article sys\_id from the Knowledge \[kb\_knowledge\] table.Data type: String

</td></tr><tr><td>

template

</td><td>

Flag that indicates whether a returned article is a template.Possible values:

-   true: Article is a template.
-   false: Article is not a template.

 Data type: Boolean

</td></tr><tr><td>

template\_table

</td><td>

Name of template table, only returns if knowledge article is a template.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_km_api/knowledge/articles/0b48fd75474321009db4b5b08b9a71c2?search_id=spam&search_rank=26.426" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  "result": {
    "content": "<p><span style=\"font-size: 18pt;\"><strong>How to Deal with Spam</strong></span></p>\r\n<p>Spam has increasingly become a problem on the Internet. While every Internet user receives some spam, email  addresses posted to web sites or in newsgroups and chat rooms attract the most spam.</p>\r\n<p>To reduce the amount of spam you receive:</p>\r\n<p>
    "template": false,
    "number": "KB0000011",
    "sys_id": "0b48fd75474321009db4b5b08b9a71c2",
    "short_description": "How to Deal with Spam",
    "display_attachments": true,
    "attachments": [
      {
        "sys_id": "dc27ae18294f4010f877796e707869c8",
        "file_name": "image.jpg",
        "size_bytes": "66792",
        "state": "available_conditionally"
      },
      {
        "sys_id": "fedf5614294f4010f877796e70786956",
        "file_name": "attachment.txt",
        "size_bytes": "75",
        "state": "available_conditionally"
      }
    ],
    "embedded_content": []
  }
}
```

### Sample cURL request \(update\_view\)

```
curl "https://instance.servicenow.com/api/sn_km_api/knowledge/KB0000020?update_view=' \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  "result": {
    "content": "<p> </p>\r\n<p> </p>\r\n<p><strong><span style=\"font-size: 18pt;\">Should I upgrade to Windows 8.x?</span></strong></p>\r\n<p>Windows 8.x is designed for using touch, mouse, and keyboard together, on hardware ranging from touch-enabled tablets and laptops to PCs and all-in-one computers...(intentionally truncated)</p>",
    "template": false,
    "number": "KB0000020",
    "sys_id": "9e528db1474321009db4b5b08b9a71a6",
    "short_description": "Windows: Should I upgrade to Windows 8.x?\t\t",
    "display_attachments": true,
    "attachments": [],
    "embedded_content": []
  }
}
```

## Knowledge Management - GET knowledge/articles/most\_viewed

Returns a list of knowledge articles prioritized by most-viewed.

### URL format

Versioned URL: `/api/sn_km_api/{api_version}/knowledge/articles/most_viewed`

Default URL: `/api/sn_km_api/knowledge/articles/most_viewed`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td>

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="km-api-parm-fields"><td>

fields

</td><td>

Comma-separated list of fields from the Knowledge \[kb\_knowledge\] table to show details in results.Data type: String

 Default: None

</td></tr><tr id="km-api-parm-kb"><td>

kb

</td><td>

Comma-separated list of knowledge base sys\_ids from the Knowledge Bases \[kb\_knowledge\_base\] table to restrict results to.Data type: String

</td></tr><tr id="km-api-parm-lang"><td>

language

</td><td>

List of comma-separated languages in two-letter ISO 639-1 language code format to restrict results to. Alternatively type 'all' to search in all valid installed languages on an instance.Data type: String

 Default: User's session language or en

</td></tr><tr id="km-api-parm-limit"><td>

limit

</td><td>

Maximum number of records to return. Unusually large **limit** values can impact system performance. For requests that exceed this number of records, use the **offset** parameter to paginate record retrieval.Data type: Number

 Default: 30

</td></tr><tr id="km-api-parm-off"><td>

offset

</td><td>

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time this endpoint is called, **offset** is set to "0". To page through all available records, use `offset=offset+limit` until the end of the all records is reached.

 Data type: Number

 Default: 0

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

articles

</td><td>

List of articles returned in response.Data type: Array

 ```
[
  {
    "fields": {Object},
    "id": "String",
    "link": "String",
    "number": "String",
    "rank": Number,
    "score": Float,
    "snippet": "String",
    "title": "String"
  }
]
```

</td></tr><tr><td>

articles.fields

</td><td id="km-resp-fields">

Values of requested fields \(if any\).Data type: Object

 ```
"fields": {
  "<field_name>": {Object}
}
```

</td></tr><tr><td>

articles.fields.&lt;field\_name&gt;

</td><td id="km-resp-fields_fieldname">

Lists each field requested using the fields parameter, if any.Data type: Object

 ```
"<field_name>": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

articles.fields.&lt;field\_name&gt;.display\_value

</td><td id="km-resp-fieldName-display">

Display value of the requested field.Data type: String

</td></tr><tr><td>

articles.fields.&lt;field\_name&gt;.label

</td><td id="km-resp-fieldName-label">

Label representing the requested field. For example, `Knowledge`.Data type: String

</td></tr><tr><td>

articles.fields.&lt;field\_name&gt;.name

</td><td id="km-resp-fieldName-name">

Name of the requested field. Matches &lt;field\_name&gt;.Data type: String

</td></tr><tr><td>

articles.fields.&lt;field\_name&gt;.type

</td><td id="km-resp-fieldName-type">

Data type of requested field.Data type: String

</td></tr><tr><td>

articles.fields.&lt;field\_name&gt;.value

</td><td id="km-resp-fields-fieldName-val">

Value of the requested field.Data type: String

</td></tr><tr><td>

articles.id

</td><td id="km_kb_id">

Knowledge article sys\_id from the Knowledge \[kb\_knowledge\] table.Data type: String

</td></tr><tr><td>

articles.link

</td><td>

Link to the article.Data type: String

</td></tr><tr><td>

articles.number

</td><td>

Knowledge article number.Data type: String

</td></tr><tr><td>

articles.rank

</td><td>

Search rank of article specific to this search.Data type: Float

</td></tr><tr><td>

articles.score

</td><td>

Relevancy score, results sorted in descending order by score.Data type: String

</td></tr><tr><td>

articles.snippet

</td><td>

Text showing a small portion of the knowledge article.Data type: String

</td></tr><tr><td>

articles.title

</td><td id="km_kb_sdesc">

Short description or title of the knowledge article.Data type: String

</td></tr><tr><td>

meta

</td><td>

Meta information of the results and request parameters.Data type: Object

 ```
"meta": {
  "count": Number,
  "end": Number,
  "fields": "String",
  "filter": "String",
  "kb": "String",
  "language": "String",
  "query": "String",
  "start": Number,
  "status": {Object},
  "ts_query_id": "String"
}
```

</td></tr><tr><td>

meta.count

</td><td>

Number of available KB articles.Data type: Number

</td></tr><tr><td>

meta.end

</td><td>

Ending index of the result set.Data type: Number

</td></tr><tr><td>

meta.fields

</td><td>

Fields in the article.Data type: String

</td></tr><tr><td>

meta.filter

</td><td>

Filter used to acquire the data.Data type: String

</td></tr><tr><td>

meta.kb

</td><td>

List of knowledge base article sys\_ids.Data type: String

</td></tr><tr><td>

meta.language

</td><td>

List of comma-separated languages of the KB articles that were requested.Data type: String

</td></tr><tr><td>

meta.query

</td><td>

Specified request query.Data type: String

</td></tr><tr><td>

meta.start

</td><td>

Starting index of result set.Data type: Number

</td></tr><tr><td>

meta.status

</td><td>

HTTP status of the call.Data type: String

</td></tr><tr><td>

meta.ts\_query\_id

</td><td>

Sys\_id of the query.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_km_api/knowledge/articles/most_viewed?limit=5" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  "result": {
    "meta": {
      "start": 0,
      "end": 5,
      "fields": "",
      "query": "",
      "filter": "workflow_state=published^valid_to>=javascript:gs.beginningOfToday()^active=true^sys_class_name!=kb_knowledge_block^sys_view_count>0^ORDERBYDESCsys_view_count^ORDERBYshort_description",
      "kb": "",
      "count": 2,
      "status": {
        "code": 200
      },
      "language": "en"
    },
    "articles": [
      {
        "link": "?id=kb_article_view&sys_kb_id=0b48fd75474321009db4b5b08b9a71c2",
        "id": "kb_knowledge:0b48fd75474321009db4b5b08b9a71c2",
        "title": "How to Deal with Spam",
        "snippet": "How to Deal with Spam Spam has increasingly become a problem on the Internet. While every Internet user receives some spam, email addresses posted to web sites or in newsgroups and chat rooms attract the most spam. To reduce the amount of spam you receive: Don't reply to spam Be careful releasing your email address, and know how it will be used ",
        "score": 7,
        "tags": [],
        "number": "KB0000011"
      },
      {
        "link": "?id=kb_article_view&sys_kb_id=c85cd2519f77230088aebde8132e70c2",
        "id": "kb_knowledge:c85cd2519f77230088aebde8132e70c2",
        "title": "Microsoft Outlook Issues",
        "snippet": "Microsoft Outlook Issues This article explains how to use automatic replies in Outlook 2010 for Exchange accounts. Setting Up Automatic Replies Click the File tab. Click Automatic Replies. Select Send automatic replies. If desired, select the Only send during this time range check box to schedule when your out of office replies are active. If yo",
        "score": 6,
        "tags": [],
        "number": "KB99999999"
      }
    ]
  }
}
```

