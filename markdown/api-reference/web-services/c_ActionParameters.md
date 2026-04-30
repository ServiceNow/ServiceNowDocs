---
title: Action parameters
description: Action parameters are separate and different from data parameters because they specify the action to take when the JSON object parameter is part of an HTTP GET or POST request.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [JSONv2 web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Action parameters

Action parameters are separate and different from data parameters because they specify the action to take when the JSON object parameter is part of an HTTP GET or POST request.

The parameters can also be specified as a field in the supplied JSON object. They have the effect of triggering an action in the case of `sysparm_action`, or filtering the results of an update or query in the case of `sysparm_query`.

## sysparm\_action

The following are the valid values for `sysparm_action` and the corresponding action triggered by the API.

|Method Summary|Description|
|--------------|-----------|
|getKeys|Query the targeted table using an encoded query string and return a comma delimited list of `sys_id` values.|
|getRecords|Query the targeted table using an encoded query string and return all matching records and their fields.|
|get|Query a single record from the targeted table by specifying the `sys_id` in the `sysparm_sys_id` URL parameter, and return the record and its fields.|

|Method Summary|Description|
|--------------|-----------|
|insert|Create one or more new records for the table targeted in the URL.|
|insertMultiple|Create multiple new records for the table targeted in the URL.|
|update|Update existing records in the targeted table in the URL, filtered by an encoded query string.|
|deleteRecord|Delete a record from the table targeted in the URL by specifying its `sys_id` in the `sysparm_sys_id` URL parameter.|
|deleteMultiple|Delete multiple records from the table targeted in the URL, filtered by an encoded query string.|

## sysparm\_query

Specify an encoded query string to be used in get, getRecords, update or deleteMultiplesysparm\_action value.

## sysparm\_view

Specify a form view to customize the return values for get and getRecords function calls. When using a view, the query returns only the fields defined in the view, including referenced values. If there is no view name, or if the view name is not valid, then the query returns all field names that are marked active in the dictionary.

## sysparm\_sys\_id

Specify a target sys\_id during a get or delete function call \(`sysparm_action` value\).

## sysparm\_record\_count

Specify an integer value to limit the number of records retrieved for this request. Note that this value is capped by the**glide.processor.json.row\_limit** system property.

## displayvalue

Get the display value of a reference field, if any are in the record. For example, the Incident record can have an `assigned_to` field that is a reference to a user record. Instead of sending the sys\_id of the user record, the user name is sent.

The displayvalue parameter can have three values: **true**, **false**, or **all**.

-   **true**: All the references fields show the display value instead of `sys_id`.
-   **false** \(default\): All reference fields show `sys_ids`.
-   **all**: The display value and the `sys_id` are shown. For example, the assignedto field in the Incident record is sent back as assigned\_to:1234556, dv\_assigned\_to:Fred Luddy.

## displayvariables

Set this boolean value to **true** during a get or getRecords function call to retrieve all variables attached to this record.

**Parent Topic:**[JSONv2 web service](c_JSONv2WebService.md)

