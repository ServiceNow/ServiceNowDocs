---
title: RTETransformer - Scoped
description: The RTETransformer API provides a method to transform and store an array of messages into a record in the associated ServiceNow instance based on a provided extract, transform, and load \(ETL\) definition.Instantiates an RTETransformer object.Transforms and stores an array of messages into a record in the associated ServiceNow instance based on a provided extract, transform, and load \(ETL\) definition.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# RTETransformer- Scoped

The RTETransformer API provides a method to transform and store an array of messages into a record in the associated ServiceNow instance based on a provided extract, transform, and load \(ETL\) definition.

For example, you can use this API when you have JSON payload\(s\) that contain user information and you want to transform that information into the sys\_user table using the Robust Transform Engine \(RTE\).

Use the `sn_impex` namespace when accessing this API.

For additional information, see Define Robust Transform Engine operations.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## RTETransformer - RTETransformer\(String transformDefinitionId, Boolean verboseLogging, String source, Number batchSize\)

Instantiates an RTETransformer object.

<table id="table_rsd_fk2_jtb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

transformDefinitionId

</td><td>

String

</td><td>

Sys\_id of the extract, transform, and load \(ETL\) definition to use for the transform.For information on creating an ETL, see Create Extract Transform Load \(ETL\) definitions.

Table: ETL Definitions \[sys\_rte\_eb\_etl\_definition\]

</td></tr><tr><td>

verboseLogging

</td><td>

Boolean

</td><td>

Flag that indicates whether to enable verbose logging and the creation of import set rows for debugging.Valid values:

-   true: Enable logging and import set row creation.
-   false: Don't enable logging and import set row creation.

</td></tr><tr><td>

source

</td><td>

String

</td><td>

Name field of the import set record.

</td></tr><tr><td>

batchSize

</td><td>

Number

</td><td>

Number of messages to process at one time \(batch\). For example, if there are 10 messages in a payload, and this value is set to 2, the method runs five separate batch jobs to process all messages in the payload.

</td></tr></tbody>
</table>The following code example shows how to instantiate an RTETransformer object for the source `testSourceRecord` that has a batch size of 10.

```
(function(/*CTIOperationRequest*/ request, /*CTIOperationResponse*/ response, /*Context*/ ctx) {    
  // Uses an ETL definition with a target table of incident, and mappings for the number and short description field
  var transformer = new sn_impex.RTETransformer("c58f1c6377110110f5455d14cd5a998b", true, "testSourceRecord", 10);
  var messages = ["{\"number\":\"testnumber\",\"short_description\":\"testdesc\"}"];
  var results = transformer.transform(messages);

  for (var i = 0; i < results.length; i++) {
    var dataList = results[i].data.incident;
    gs.log("source record id: " + results[i].sourceRecordSysId);
    gs.log("status: " + results[i].status);
    for (var j = 0; j < dataList.length; j++) {
      gs.log("number:" + dataList[j].number);
      gs.log("short desc:" + dataList[j].short_description);
    }
  }
})(request, response, ctx);
```

## RTETransformer - transform\(Array message\)

Transforms and stores an array of messages into a record in the associated ServiceNow instance based on a provided extract, transform, and load \(ETL\) definition.

For example, if you want to transform user information into a sys\_user record, you can create a message array with a single message and pass it into this transform method.

<table id="table_xsb_bq2_jtb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

Array of Objects

</td><td>

Stringified JSON objects representing the records to transform based on the ETL definition.For example, if you want to transform a single user with the data active, email, first name, and last name to the sys\_user table, the message would look similar to this:

```
[
  {  
    "active":"true",
    "email":"example@servicenow.com",
    "first_name":"Jane",
    "last_name":"Doe" 
  }
]
```

**Note:** The field names must match the field/path of the source entity fields.

</td></tr></tbody>
</table><table id="table_ysb_bq2_jtb" class="returns"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data

</td><td>

Data for the transformed records, organized by table name. The returned record data matches the mapped fields specified in the ETL definition.Data type: Object

 ```
"data": {
  "tableName": []
}
```

</td></tr><tr><td>

data.tableName

</td><td>

Details of the table containing the records.Data type: Array of Objects

 ```
"tableName": [{
  "sys_id": String,
   // Other data for a single transformed record
  }]
}
```

 For example:

```
"sys_user": [{ 
  "sys_id":"b29e629877130110f5455d14cd5a99ad",
  "active": "true",
  "email": "example@servicenow.com",
  "first_name": "Jane",
  "last_name": "Doe"
}]
```

</td></tr><tr><td>

data.tableName.sys\_id

</td><td>

Sys\_id of the record within the table.Data type: String

</td></tr><tr><td>

data.tableName.&lt;other\_ETL\_info&gt;

</td><td>

Additional fields that were specified in the passed ETL.Data type: Any

</td></tr><tr><td>

message

</td><td>

If an error occurs while transforming the specified record, a message that describes the error. Null if the transform is successful.Data type: String

</td></tr><tr><td>

sourceRecordSysId

</td><td>

Sys\_id of the import set table record. The import set table name is JSON Event Sink \[imp\_json\_event\_sink\].Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the transform, such as processed or error.Data type: String

</td></tr></tbody>
</table>The following code example shows how to transform and store a record in the User \[sys\_user\] table.

```
(function(/*CTIOperationRequest*/ request, /*CTIOperationResponse*/ response, /*Context*/ ctx) { 
  // Uses an ETL definition with a target table of sys_user, and mappings for the active, 
  //email, first name, and last name fields
  var transformer = new sn_impex.RTETransformer("c58f1c6377110110f5455d14cd5a998b", true, "testSourceRecord", 10);
  var messages = [JSON.stringify({
    "active":"true",
    "email":"example@servicenow.com",
    "first_name":"Jane",
    "last_name":"Doe"
  }), 
  JSON.stringify({
    "active":"true",
    "email":"example2@servicenow.com",
    "first_name":"John",
    "last_name":"Deer"
  })];
  var results = transformer.transform(messages);

  for (var i = 0; i < results.length; i++) { 
    var dataList = results[i].data.sys_user;
    gs.log("source record id: " + results[i].sourceRecordSysId); gs.log("status: " + results[i].status);
    for (var j = 0; j < dataList.length; j++) { 
      gs.log("First Name: " + dataList[j].first_name);
      gs.log("Last Name: " + dataList[j].last_name);
      gs.log("Email: " + dataList[j].email;
      gs.log("Active: " + dataList[j].active;
    }
  }
}
```

Results:

```
source record id: b29e629877130110f5455d14cd5a99ad
status: PROCESSED
First Name: Jane
Last Name: Doe
Email: example@servicenow.com
Active: true
First Name: John
Last Name: Deer
Email: example2@servicenow.com
Active: true
```

