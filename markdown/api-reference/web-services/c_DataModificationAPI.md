---
title: JSON Data Modification API
description: Modify data using the JSON web service by sending an HTTPS POST request to the instance.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [JSONv2 web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# JSON Data Modification API

Modify data using the JSON web service by sending an HTTPS POST request to the instance.

The HTTP POST must contain a `sysparm_action` parameter to indicate the type of action to be performed, with the incoming JSON object post in the body.

**Note:** The content-type of the POST should be application/json. It cannot be application/x-www-form-urlencoded or multipart/form-data.

## insert

Create a new record in ServiceNow. The JSON object has to be POSTed as the body \(content-type is usually application/json, although not enforced\). The response from the record creation is a JSON object of the incident that was created.

For example, posting the following JSON object:

```
{"short_description":"this is a test","priority":"1"}
```

to the following URL:

```
https://your_instance.service-now.com/incident.do?JSONv2&sysparm_action=insert
```

creates an incident.

Optionally, you may also specify the sysparm\_action in the JSON object. The parameter inside the JSON object takes precedence over the URL parameter. For example:

```
{"sysparm_action":"insert","short_description":"this is a test","priority":"1"}
```

## insertMultiple

To create multiple new records in ServiceNow, the input JSON object for the insert function must be an array. The response from the record creation is a JSON object of the incidents that were created. For example, the following JSON object:

```
{ "records" : [ { "short_description" : "this was inserted with python using JSON 1" , "priority" : "1 - Critical" , "impact" : "1" , "caller_id" : "Fred Luddy" } , { "short_description" : "this was inserted with python using JSON 2" , "priority" : "1 - Critical" , "impact" : "1" , "caller_id" : "Fred Luddy" } ] }
```

posted to one the following URLs:

```
https://<instance name>.service-now.com/incident.do?JSONv2&sysparm_action=insert
https://<instance name>.service-now.com/incident.do?JSONv2&sysparm_action=insertMultiple

```

creates two incidents. Note the fields described as an array value for the **records** field.

## update

Update a record or a list of records filtered by an encoded query string specified by the `sysparm_query` URL parameter. The JSON object has to be posted as the body \(content-type is usually application/json, although not enforced\). The response from the record creation is an array of JSON objects representing the records that were updated.

For example, posting the following JSON object:

```
{"short_description":"this was updated with python", "priority": "3", "impact":"1"}
```

to the following URL:

```
https://instance_name.service-now.com/incident.do?JSONv2&sysparm_query=priority=3&sysparm_action=update

```

updates all incidents with priority 3, and sets the values specified by the JSON object.

## deleteRecord

Delete a single record from the targeted table, identified by a `sysparm_sys_id` parameter. The parameter may be encoded in the input JSON object or given as a URL parameter.

For example, posting:

```
{"sysparm_sys_id":"fd4001f80a0a0b380032ffa2b749927b"}

```

to the following URL:

```
http://instance_name.service-now.com/incident.do?JSONv2&sysparm_action=deleteRecord

```

deletes the incident record identified by the sys\_id fd4001f80a0a0b380032ffa2b749927b.

## deleteMultiple

Delete multiple records from the targeted table, filtered by an encoded query string specified in the `sysparm_query` URL parameter. The filter may also be encoded in the input JSON object.

For example, posting:

```
{"sysparm_query":"short_description=this was updated with python"}
```

to the following URL:

```
http://instance_name.service-now.com/incident.do?JSONv2&sysparm_action=deleteMultiple
```

deletes all incident records where the `short_description` field contains the value "this was updated with python".

**Parent Topic:**[JSONv2 web service](c_JSONv2WebService.md)

