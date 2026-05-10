---
title: JSON Data Retrieval API
description: Query for data by issuing an HTTPS GET request to the instance.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [JSONv2 web service, Inbound, Web services, API implementation, API implementation and reference]
---

# JSON Data Retrieval API

Query for data by issuing an HTTPS GET request to the instance.

By default, a GET request is interpreted as a get function if a **sysparm\_sys\_id** parameter is present. Otherwise, it is interpreted as a getRecords function. You can also specify a URL parameter **sysparm\_action=get**. Query responses are always encapsulated by a records hash of records, where each individual record's values are themselves hashed by field name.

## Return Display Value for Reference Variables

When you are getting a record from a get or getRecords function, all the fields associated with that record are returned. The fields are often reference fields that contain a `sys_id` for another table. The base system behavior is to return the `sys_id` value for those fields. To have the display value for the field returned, use one of these options:

-   Add the property glide.json.return\_displayValue to the system properties, and every JSON request will return a display value for a reference field.
-   Add the parameter **displayvalue=true** to the JSON request URL and JSON requests with that parameter will return a display value instead of the `sys_id` for a reference field. The JSON URL would look like this:

    ```
    https://<instance name>.service-now.com/incident.do?JSON&sysparm_action=getRecords&sysparm_query=active=true^category=hardware&displayvalue=true
    
    ```

-   Add the parameter **displayvalue=all** to the JSON request URL and JSON requests with that parameter return a display value and the `sys_id` for a reference field. The response element name for the display value field will be prefixed with `dv_`, for example `dv_caller_id`.

## Get variables

Use the **displayvariables** query parameter to return an array of variables associated with a Service Catalog item record. To get variables, add the parameter **displayvariables=true** to the JSON request URL. For example, here is a URL to retrieve a record in JSON format that includes Service Catalog variables:

```
https://<your-instance>.servicenow.com/sc_req_item.do?JSONv2&sysparm_action=getRecords&sysparm_query=sys_id=5018da81742bd410f8771974894916fe&displayvariables=true
```

Here is the example response that displays a multi-row variable set from the record:

```
{
   "records":[
      {
         …
         "variables":[
            {
               "display_value":[
                  {
                     "quantity":"1",
                     "color":"Black",
                     "device_type":"Apple iPhone 8",
                     "storage":"64GB"
                  },
                  {
                     "quantity":"1",
                     "color":"Black",
                     "device_type":"Apple iPhone 8",
                     "storage":"64GB"
                  }
               ],
               "columns_meta":[
                  {
                     "name":"device_type",
                     "label":"Device Type",
                     "id":"da7d3f3241411300964ff05369414eca",
                     "type":5,
                     "order":"0"
                  },
                  {
                     "name":"storage",
                     "label":"Storage",
                     "id":"691e337241411300964ff05369414e31",
                     "type":5,
                     "order":"1"
                  },
                  {
                     "name":"color",
                     "label":"Color",
                     "id":"e89fb77241411300964ff05369414e74",
                     "type":5,
                     "order":"2"
                  },
                  {
                     "name":"quantity",
                     "label":"Quantity",
                     "id":"2d5f737241411300964ff05369414eaf",
                     "type":5,
                     "order":"3"
                  }
               ],
               "max_rows":50,
               "name":"mobile_devices_set",
               "id":"e84d3f3241411300964ff05369414e3e",
               "type":"one_to_many",
               "value":[
                  {
                     "quantity":"1",
                     "color":"black",
                     "device_type":"iphone8",
                     "storage":"64GB"
                  },
                  {
                     "quantity":"1",
                     "color":"black",
                     "device_type":"iphone8",
                     "storage":"64GB"
                  }
               ],
               "row_count":2
            },
            {
               "question_text":"Department",
               "name":"department",
               "type":8,
               "value":"Development",
               "order":100
            },
            {
               "question_text":"Who is this request for?",
               "name":"requested_for",
               "type":8,
               "value":"System Administrator",
               "order":100
            },
            {
               "question_text":"When do you need this?",
               "name":"needed_by",
               "type":5,
               "value":"Today",
               "order":200
            },
            {
               "question_text":"Business Justification",
               "name":"business_justification",
               "type":2,
               "value":"Example justification",
               "order":200
            }
         ],
       …
      }
   ]
}
```

The keys in the response are defined as follows:

|Key|Description|
|---|-----------|
|display\_value|Multi-row variable set question display value. Only returned with multi-row variable sets.|
|columns\_meta|Array of multi-row variable set metadata, such as the sys\_id and name of the field. Only returned when the variable contains multiple fields.|
|max\_rows|Maximum rows allowed in the multi-row variable set. Only returned with multi-row variable sets.|
|name|Question name.|
|id|Sys\_id of the multi-row variable set. Only returned with multi-row variable sets.|
|type|Type of question.|
|value|Question value.|
|row\_count|Current number of rows in the multi-row variable set. Only returned with multi-row variable sets.|
|question\_text|Question label. Only returned with single-row variable sets.|
|order|Order of the question.|

## Control the order of records

You can control the order that records appear in the JSON response. To set an order, use the **ORDERBY** or **ORDERBYDESC** clauses in the URL encoded query. For example,

```
sysparm_query=active=true^ORDERBYnumber^ORDERBYDESCcategory
```

filters all active records and orders the results in ascending order by number first, and then in descending order by category. For more information, see [Encoded query strings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_EncodedQueryStrings.md).

## getKeys

Get the `sys_id` of multiple records by specifying an encoded query string in the **sysparm\_query** parameter.

```
https://<instance name>.service-now.com/incident.do?JSONv2&sysparm_action=getKeys&sysparm_query=active=true^category=hardware

```

## get

Get a record directly by specifying the `sys_id` in a **sysparm\_sys\_id** parameter.

```
https://<instance name>.service-now.com/incident.do?JSONv2&sysparm_sys_id=9d385017c611228701d22104cc95c371

```

Optionally, you may also specify the **sysparm\_action** parameter:

```
https://<instance name>.service-now.com/incident.do?JSONv2&sysparm_action=get&sysparm_sys_id=9d385017c611228701d22104cc95c371

```

## getRecords

Get all records by specifying an encoded query string in the **sysparm\_query** parameter.

```
https://<instance name>.service-now.com/incident.do?JSONv2&sysparm_action=getRecords&sysparm_query=active=true^category=hardware

```

**Parent Topic:**[JSONv2 web service](c_JSONv2WebService.md)

