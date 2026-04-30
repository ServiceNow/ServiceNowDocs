---
title: Appointment Open API
description: The Appointment Open API is a telecommunication API that allows you to interact with the appointment booking application. Use this API to book appointments and search available time slots.Deletes an appointment record with a given ID.Retrieves a list of appointment records.Retrieves an appointment record associated with a specified ID.Returns time slots that were configured in the appointment booking service configuration along with their availability.Reschedule appointments with a given ID for a  work order.Enables you to book appointments for a work order.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 28
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Appointment Open API

The Appointment Open API is a telecommunication API that allows you to interact with the appointment booking application. Use this API to book appointments and search available time slots.

The Appointment Open API is a ServiceNow® implementation of the Open API TMForum TMF646 Appointment REST API specification and is conformance certified by TM Forum. This implementation is based on [TMF646 Appointment API REST Specification R16.0.1](https://www.tmforum.org/resources/specification/tmf646-appointment-api-rest-specification-r16-0-1/).

![TMF conformance logo](../image/tmf-conformance.png)

This API requires the following plugins available on the ServiceNow Store.

-   Appointment Booking \(com.snc.appointment\_booking\)
-   Field Service Management \(com.snc.work\_management\)
-   Field Service Management for Telecommunications \(com.sn\_fsmt\)
-   Telecommunication Open APIs \(com.sn\_tmf\_api\)

Before using this API, Appointment Booking Configuration and Service Configuration must be set up. In addition, a task for which the appointment is being booked must exist.

This API is provided within the `sn_tmf_api` namespace. The calling user must have the sn\_tmf\_api.appointment\_integrator role.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Appointment Open - DELETE /api/sn\_tmf\_api/appointment/appointment/\{id\}

Deletes an appointment record with a given ID.

### URL format

Default URL: `/api/sn_tmf_api/appointment/appointment/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the appointment record to delete. Data type: String

Table: Appointment booking \[sn\_apptmnt\_booking\_appointment\_booking\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the request body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|404|Not found. The requested item wasn't found.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

Response message acknowledging successful deletion.Success: "The appointment \(&lt;id&gt;\) is successfully cancelled."

Errors:

-   "Appointment cancellation failed.": The ID can't be found in the system and returns a 404 status code.
-   "Appointment cancellation failed.": The appointment is already in a cancelled or completed state or can't be deleted, and returns a 404 status code.
-   "The appointment \(&lt;id&gt;\) can't be cancelled as it is beyond the Cancel by time.": The appointment is already beyond the ‘cancel by time’, which is configured in the appointment booking service configuration. Returns a 400 status code.

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example deletes an appointment with a specific ID.

```
curl "http://instance.servicenow.com/api/sn_tmf_api/appointment/appointment/68cc0a5a9314521060320dd548373" \ 
--request GET\ 
--user 'username':'password' 
```

Response body:

```
"The appointment (68cc0a5a9314521060320dd548373cbd) is successfully cancelled."
```

## Appointment Open - GET /api/sn\_tmf\_api/appointment/appointment

Retrieves a list of appointment records.

### URL format

Default URL: `/api/sn_tmf_api/appointment/appointment`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table id="id_akz_31d_tcc" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="query-row-category"><td>

category

</td><td>

Filter the appointment by category sys\_id.Data type: String

Table: Location \[cmn\_location\]

Default: Returns all appointments if category sys\_id is not provided.

</td></tr><tr id="query-row-relatedEntity"><td>

relatedEntity

</td><td>

Details about the related entity associated with the work order.Data type: Object

```
"relatedEntity": {
  "id": "String"
}
```

</td></tr><tr id="query-row-relatedEntity.id"><td>

relatedEntity.id

</td><td>

Required. Sys\_id of the related entity.Data type: String

Table: workOrder \[wm\_order\]

Default: Returns all if sys\_id is not provided.

</td></tr><tr id="query-row-relatedParty"><td>

relatedParty

</td><td>

Filter the appointment by the sys\_id of the related party associated with the appointment.Data type: Object

```
"relatedParty": {
  "id": "String",
  "name": "String"
}
```

Default: Returns all appointments if **relatedParty** is not provided.

</td></tr><tr id="query-row-relatedParty.id"><td>

relatedParty.id

</td><td>

Sys\_id of the related party.Data type: String

Table: User \[sys\_user\]

</td></tr><tr id="query-row-relatedParty.name"><td>

relatedParty.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr id="query-row-relatedPlace"><td>

relatedPlace

</td><td>

Filter the appointment by the place where the service or repair is scheduled to happen.Data type: Object

```
"relatedPlace": {
  "id": "String"
}
```

Default: Returns all appointments if **relatedPlace** is not provided.

</td></tr><tr id="query-row-relatedPlace.id"><td>

relatedPlace.id

</td><td>

Sys\_id of the related place.Data type: String

Table: Location \[cmn\_location\]

</td></tr><tr id="query-row-validFor"><td>

validFor

</td><td>

Filter the appointment by a date range that the appointment is valid for.Data type: Object

```
"validFor":
{
  "endDateTime": "String",
  "startDateTime": "String"
}
```

Default: Returns all appointments if **validFor** is not provided.

</td></tr><tr id="query-row-validFor.endDateTime"><td>

validFor.endDateTime

</td><td>

End date and time of the appointment. Only appointments with the specified end date and time are returned in the response.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

Table: Location \[cmn\_location\]

</td></tr><tr id="query-row-validFor.startDateTime"><td>

validFor.startDateTime

</td><td>

Start date and time of the appointment. Only appointments with the specified start date and time are returned in the response. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

Table: Location \[cmn\_location\]

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
|Content-Type|Data format of the request body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|404|Not found. The requested item wasn't found.|

### Response body parameters \(JSON or XML\)

<table id="table_g3p_tyd_wcc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

category

</td><td>

Sys\_id of the record producer configured for the appointment booking service configuration.Data type: String

Stored in: Catalog Item  field of the Appointment Booking Service Configuration \[sn\_apptmnt\_booking\_service\_config\] table.

</td></tr><tr><td>

creationDate

</td><td>

Date and time that the appointment was created.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

</td></tr><tr><td>

href

</td><td>

Hyperlink to the appointment record. Use this link in another Appointment Open API request to reschedule or delete the appointment.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the appointment.Data type: String

Stored in: Appointment Booking Service Configuration \[sn\_apptmnt\_booking\_service\_config\] table

</td></tr><tr><td>

lastUpdate

</td><td>

Date and time the appointment was last updated.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

</td></tr><tr><td>

relatedEntity

</td><td>

Details about the related entity of the appointment.Data type: Array of Objects

```
"relatedEntity": [
 {
  "@referredType": "String",
  "id": "String",
  "role": "String"
  }
]
```

</td></tr><tr><td>

relatedEntity.@referredType

</td><td>

Type of item or service.Data type: String

Stored in: workOrder \[wm\_order\] table

</td></tr><tr><td>

relatedEntity.id

</td><td>

Sys\_id of the related entity.Data type: String

Stored in: workOrder \[wm\_order\] table

</td></tr><tr><td>

relatedEntity.role

</td><td>

Role description of the related entity. Possible value: work order

Data type: String

Stored in: workOrder \[wm\_order\] table

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the appointment. Each contact is an object in the array.Data type: Array of Objects

```
"relatedParty": [
 {
  "@referredType": "String",
  "id": "String",
  "name": " String",
  "role": "String"
 }
]
```

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer.Data type: String

Stored in: Contact \[customer\_contact\] table

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the customer contact associated with the work order.Data type: String

Stored in: Contact \[customer\_contact\] table

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the customer contact.Data type: String

Stored in: Contact \[customer\_contact\] table

</td></tr><tr><td>

relatedParty.role

</td><td>

Role of the customer contact.Possible values:

-   customer: The contact has a customer role.
-   technician: The contact has a technician role.

Data type: String

Stored in: Contact \[customer\_contact\] table

</td></tr><tr><td>

relatedPlace

</td><td>

Location details of the associated appointment.Data type: Object

```
"relatedPlace": {
  "@referredType": "String",
  "id": "String",
  "name": "String",
  "role": "String"
}
```

</td></tr><tr><td>

relatedPlace.@referredType

</td><td>

Geographic address of the appointment. Possible value: GeographicLocation.

Data type: String

Stored in: Location \[cmn\_location\] table

</td></tr><tr><td>

relatedPlace.id

</td><td>

Sys\_id of the location. Data type: String

Stored in: Location \[cmn\_location\] table

</td></tr><tr><td>

relatedPlace.name

</td><td>

Name of the location related to the contact. For example, 100 South Charles Street, Baltimore, MD.Data type: String

Stored in: Location \[cmn\_location\] table

</td></tr><tr><td>

relatedPlace.role

</td><td>

Role of the appointment location as an intervention address.Possible value: InterventionAddress

Data type: String

Stored in: Location \[cmn\_location\] table

</td></tr><tr><td>

validFor

</td><td>

Date range that the appointment is valid for.Data type: Object

```
"validFor": {
 "endDateTime": "String"
 "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date and time of the appointment.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date and time of the appointment.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

</td></tr></tbody>
</table>### cURL request

The following example shows how to return a list of appointments using the GET appointment method.

```
curl "http://instance.servicenow.com/api/sn_tmf_api/appointment/appointment" \ 
--request GET\ 
--user 'username':'password' 
```

The response body contains the details of two different appointments configured in the appointment booking service configuration:

```
[
  {
    "id": "201071ad4f80d210f8992fec52ce0ba9",
    "href": "api/sn_tmf_api/appointment/appointment/201071ad4f80d210f8992fec52ce0ba9",
    "validFor": {
      "startDateTime": "2024-08-16 17:00:00",
      "endDateTime": "2024-08-16 19:00:00"
    },
    "category": "4a34a64d4f4c1210f8992fec52ce0b63",
    "relatedParty": [
      {
        "id": "eaf68911c35420105252716b7d40ddde",
        "name": " null",
        "role": "customer",
        "@referredType": "Individual"
      }
    ],
    "relatedPlace": {
      "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
      "name": "100 South Charles Street, Baltimore,MD",
      "role": "interventionAddress",
      "@referredType": "Individual"
    },
    "relatedEntity": [
      {
        "id": "b440a5694f40d210f8992fec52ce0ba3",
        "role": "work order",
        "@referredType": "WorkOrder"
      }
    ],
    "creationDate": "2024-08-16 00:39:22",
    "lastUpdate": "2024-08-16 00:39:22"
  },
  {
    "id": "25c012c07f5c5610f8994fa63c866523",
    "href": "api/sn_tmf_api/appointment/appointment/25c012c07f5c5610f8994fa63c866523",
    "validFor": {
      "startDateTime": "2024-08-26 17:00:00",
      "endDateTime": "2024-08-26 19:00:00"
    },
    "category": "4a34a64d4f4c1210f8992fec52ce0b63",
    "relatedParty": [
      {
        "id": "eaf68911c35420105252716b7d40ddde",
        "name": " null",
        "role": "customer",
        "@referredType": "Individual"
      }
    ],
    "relatedPlace": {
      "id": "f48b21850a0a0ba7004182b18099696d",
      "name": "11251 Rancho Carmel Drive, San Diego,CA",
      "role": "interventionAddress",
      "@referredType": "Individual"
    },
    "relatedEntity": [
      {
        "id": "c0b09a047f109610f8994fa63c8665b4",
        "role": "work order",
        "@referredType": "WorkOrder"
      }
    ],
    "creationDate": "2024-08-23 22:18:43",
    "lastUpdate": "2024-08-23 22:18:43"
  }
]
```

## Appointment Open - GET /api/sn\_tmf\_api/appointment/appointment/\{id\}

Retrieves an appointment record associated with a specified ID.

### URL format

Default URL: `/api/sn_tmf_api/appointment/appointment/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the appointment to retrieve.Data type: String

Table: Appointment booking \[sn\_apptmnt\_booking\_appointment\_booking\]

</td></tr></tbody>
</table><table id="id_g4x_4zc_tcc" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="query-row-category"><td>

category

</td><td>

Filter the appointment by category sys\_id.Data type: String

Table: Location \[cmn\_location\]

Default: Returns all appointments if category sys\_id is not provided.

</td></tr><tr id="query-row-relatedEntity"><td>

relatedEntity

</td><td>

Details about the related entity associated with the work order.Data type: Object

```
"relatedEntity": {
  "id": "String"
}
```

</td></tr><tr id="query-row-relatedEntity.id"><td>

relatedEntity.id

</td><td>

Required. Sys\_id of the related entity.Data type: String

Table: workOrder \[wm\_order\]

Default: Returns all if sys\_id is not provided.

</td></tr><tr id="query-row-relatedParty"><td>

relatedParty

</td><td>

Filter the appointment by the sys\_id of the related party associated with the appointment.Data type: Object

```
"relatedParty": {
  "id": "String",
  "name": "String"
}
```

Default: Returns all appointments if **relatedParty** is not provided.

</td></tr><tr id="query-row-relatedParty.id"><td>

relatedParty.id

</td><td>

Sys\_id of the related party.Data type: String

Table: User \[sys\_user\]

</td></tr><tr id="query-row-relatedParty.name"><td>

relatedParty.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr id="query-row-relatedPlace"><td>

relatedPlace

</td><td>

Filter the appointment by the place where the service or repair is scheduled to happen.Data type: Object

```
"relatedPlace": {
  "id": "String"
}
```

Default: Returns all appointments if **relatedPlace** is not provided.

</td></tr><tr id="query-row-relatedPlace.id"><td>

relatedPlace.id

</td><td>

Sys\_id of the related place.Data type: String

Table: Location \[cmn\_location\]

</td></tr><tr id="query-row-validFor"><td>

validFor

</td><td>

Filter the appointment by a date range that the appointment is valid for.Data type: Object

```
"validFor":
{
  "endDateTime": "String",
  "startDateTime": "String"
}
```

Default: Returns all appointments if **validFor** is not provided.

</td></tr><tr id="query-row-validFor.endDateTime"><td>

validFor.endDateTime

</td><td>

End date and time of the appointment. Only appointments with the specified end date and time are returned in the response.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

Table: Location \[cmn\_location\]

</td></tr><tr id="query-row-validFor.startDateTime"><td>

validFor.startDateTime

</td><td>

Start date and time of the appointment. Only appointments with the specified start date and time are returned in the response. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

Table: Location \[cmn\_location\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the request body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|404|Not found. The requested item wasn't found.|

### Response body parameters

<table id="table_ybf_bwd_wcc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

category

</td><td>

Sys\_id of the record producer configured for the appointment booking service configuration.Data type: String

Stored in: Catalog Item  field of the Appointment Booking Service Configuration \[sn\_apptmnt\_booking\_service\_config\] table.

</td></tr><tr><td>

creationDate

</td><td>

Date and time that the appointment was created.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

</td></tr><tr><td>

href

</td><td>

Hyperlink to the appointment record. Use this link in another Appointment Open API request to reschedule or delete the appointment.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the appointment.Data type: String

Stored in: Appointment Booking Service Configuration \[sn\_apptmnt\_booking\_service\_config\] table

</td></tr><tr><td>

lastUpdate

</td><td>

Date and time the appointment was last updated.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

</td></tr><tr><td>

relatedEntity

</td><td>

Details about the related entity of the appointment.Data type: Array of Objects

```
"relatedEntity": [
 {
  "@referredType": "String",
  "id": "String",
  "role": "String"
  }
]
```

</td></tr><tr><td>

relatedEntity.@referredType

</td><td>

Type of item or service.Data type: String

Stored in: workOrder \[wm\_order\] table

</td></tr><tr><td>

relatedEntity.id

</td><td>

Sys\_id of the related entity.Data type: String

Stored in: workOrder \[wm\_order\] table

</td></tr><tr><td>

relatedEntity.role

</td><td>

Role description of the related entity. Possible value: work order

Data type: String

Stored in: workOrder \[wm\_order\] table

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the appointment. Each contact is an object in the array.Data type: Array of Objects

```
"relatedParty": [
 {
  "@referredType": "String",
  "id": "String",
  "name": " String",
  "role": "String"
 }
]
```

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer.Data type: String

Stored in: Contact \[customer\_contact\] table

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the customer contact associated with the work order.Data type: String

Stored in: Contact \[customer\_contact\] table

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the customer contact.Data type: String

Stored in: Contact \[customer\_contact\] table

</td></tr><tr><td>

relatedParty.role

</td><td>

Role of the customer contact.Possible values:

-   customer: The contact has a customer role.
-   technician: The contact has a technician role.

Data type: String

Stored in: Contact \[customer\_contact\] table

</td></tr><tr><td>

relatedPlace

</td><td>

Location details of the associated appointment.Data type: Object

```
"relatedPlace": {
  "@referredType": "String",
  "id": "String",
  "name": "String",
  "role": "String"
}
```

</td></tr><tr><td>

relatedPlace.@referredType

</td><td>

Geographic address of the appointment. Possible value: GeographicLocation.

Data type: String

Stored in: Location \[cmn\_location\] table

</td></tr><tr><td>

relatedPlace.id

</td><td>

Sys\_id of the location. Data type: String

Stored in: Location \[cmn\_location\] table

</td></tr><tr><td>

relatedPlace.name

</td><td>

Name of the location related to the contact. For example, 100 South Charles Street, Baltimore, MD.Data type: String

Stored in: Location \[cmn\_location\] table

</td></tr><tr><td>

relatedPlace.role

</td><td>

Role of the appointment location as an intervention address.Possible value: InterventionAddress

Data type: String

Stored in: Location \[cmn\_location\] table

</td></tr><tr><td>

validFor

</td><td>

Date range that the appointment is valid for.Data type: Object

```
"validFor": {
 "endDateTime": "String"
 "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date and time of the appointment.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date and time of the appointment.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

</td></tr></tbody>
</table>### cURL request

The following example returns appointment details according to the given appointment record ID.

```
curl "http://instance.servicenow.com/api/sn_tmf_api/appointment/appointment/201071ad4f80d210f8992fec52ce0ba9" \ 
--request GET\ 
--user 'username':'password'
```

Response body:

```
[
  {
    "id": "201071ad4f80d210f8992fec52ce0ba9",
    "href": "api/sn_tmf_api/appointment/appointment/201071ad4f80d210f8992fec52ce0ba9",
    "validFor": {
      "startDateTime": "2024-08-16 17:00:00",
      "endDateTime": "2024-08-16 19:00:00"
    },
    "category": "4a34a64d4f4c1210f8992fec52ce0b63",
    "relatedParty": [
      {
        "id": "eaf68911c35420105252716b7d40ddde",
        "name": " null",
        "role": "customer",
        "@referredType": "Individual"
      }
    ],
    "relatedPlace": {
      "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
      "name": "100 South Charles Street, Baltimore,MD",
      "role": "interventionAddress",
      "@referredType": "Individual"
    },
    "relatedEntity": [
      {
        "id": "b440a5694f40d210f8992fec52ce0ba3",
        "role": "work order",
        "@referredType": "WorkOrder"
      }
    ],
    "creationDate": "2024-08-16 00:39:22",
    "lastUpdate": "2024-08-16 00:39:22"
  }
]
```

## Appointment Open - GET /api/sn\_tmf\_api/appointment/searchTimeSlot

Returns time slots that were configured in the appointment booking service configuration along with their availability.

### URL format

`/api/sn_tmf_api/appointment/searchTimeSlot`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

catalog\_id

</td><td>

Required. Sys\_id of the record producer configured with an appointment booking service configuration. Data type: String

Table: Record Producer \[sc\_cat\_item\_producer\]

</td></tr><tr id="serviceTest-response-testMeasureDefinition.thresholdRule.consequence.validFor.endDateTime"><td>

end\_date

</td><td>

Required. End date and time of the time period in which you want to search for the appointment.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 12:00:00`.

</td></tr><tr><td>

location

</td><td>

Sys\_id of the appointment's location.Table: Location \[cmn\_location\]

Data type: String

Default: Returns all locations if not specified.

</td></tr><tr><td>

opened\_for

</td><td>

Required. Sys\_id of the user for whom the appointment is being booked.Table: Contact \[customer\_contact\]

Data type: String

</td></tr><tr id="serviceTest-response-testMeasureDefinition.thresholdRule.consequence.validFor.startDateTime"><td>

start\_date

</td><td>

Required. Start date and time of the time period in which you want to search for the appointment.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:00:00`.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

availableTimeSlot

</td><td>

List of appointment slots within the specified block of time requested.Data type: Array of Objects

```
'availableTimeSlot': [
 { 
  "available": Boolean,
  "end_date": "String",
  "end_date_display": "String",
  "end_dateUTC": "String",
  "start_date": "String",
  "start_date_display": "String",
  "start_dateUTC": "String"
 }
]
```

</td></tr><tr><td>

availableTimeSlot.available

</td><td>

Flag that indicates whether the associated time slot is available.Possible values:

-   true: Time slot is available.
-   false: Time slot is unavailable.

Data type: Boolean

</td></tr><tr><td>

availableTimeSlot.end\_date

</td><td>

End date and time of the associated appointment. The time zone is based on the value in the **timeZone** parameter.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

</td></tr><tr><td>

availableTimeSlot.end\_date\_display

</td><td>

Display end date and time of the associated appointment. The time zone is based on the value in the **timeZone** parameter.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

</td></tr><tr><td>

availableTimeSlot.end\_dateUTC

</td><td>

End date and time of the associated appointment.Data type: String

Format: UTC

</td></tr><tr><td>

availableTimeSlot.start\_date

</td><td>

Start date and time of the associated appointment. Reflects the value of the **timeZone** parameter.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

</td></tr><tr><td>

availableTimeSlot.start\_date\_display

</td><td>

Display start date and time of the associated appointment. Reflects the value of the **timeZone** parameter.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

</td></tr><tr><td>

availableTimeSlot.start\_dateUTC

</td><td>

Start date and time of the associated appointment.Data type: String

Format: UTC

</td></tr><tr><td>

hasMore

</td><td>

Flag that indicates whether there are more appointment slots to fetch after returning the limit. The limit is specified in the Appointment Booking property, sn\_apptmnt\_booking.max\_appointments\_returned \(Default: 100\). See [Appointment booking components](https://www.servicenow.com/docs/access?context=appointment-booking-components&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US) for more details about this property.Possible values:

-   true: More appointment slots can be fetched.
-   false: No more appointment slots are available.

Data type: Boolean

</td></tr><tr><td>

noApptAvailable

</td><td>

Flag that indicates whether there are more appointment slots available for the specified date and time.Valid values:

-   true: More appointment slots are available for the specified date and time.
-   false: No more appointment slots are available for the specified date and time.

Data type: Boolean

</td></tr><tr><td>

searchResult

</td><td>

Results for appointment availability within the designated search time slot.Possible values:

-   success
-   fail

Data type: String

</td></tr><tr><td>

status

</td><td>

Completion status of the search for available time slots. For example, done.Data type: String

</td></tr><tr><td>

timeZone

</td><td>

Time zone used when booking or updating the specified appointment slot.Date type: String

Format: Country/city or area format, such as US/Eastern

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl --location --request GET 'https://instance.service-now.com/api/sn_tmf_api/appointment/searchTimeSlot?
start_date=2024-07-10 09:00:00&end_date=2024-07-20 23:00:00&catalog_id=ada50a93f0220210f8776517d8c8e776&
opened_for=51670151c35420105252716b7d40ddfe&location=f48b21850a0a0ba7004182b18099696d ' \
--user 'username':'password'
```

Result:

```
{
  "searchResult": "success",
  "status": "done",
  "availableTimeSlot": [
    {
      "start_date": "2024-07-10 09:00:00",
      "end_date": "2024-07-10 12:00:00",
      "start_date_display": "09:00",
      "end_date_display": "12:00",
      "start_dateUTC": "2024-07-10 16:00:00",
      "end_dateUTC": "2024-07-10 19:00:00",
      "available": false
    },
    {
      "start_date": "2024-07-11 13:00:00",
      "end_date": "2024-07-11 16:00:00",
      "start_date_display": "13:00",
      "end_date_display": "16:00",
      "start_dateUTC": "2024-07-11 20:00:00",
      "end_dateUTC": "2024-07-11 23:00:00",
      "available": true
    },
    {
      "start_date": "2024-07-12 09:00:00",
      "end_date": "2024-07-12 12:00:00",
      "start_date_display": "09:00",
      "end_date_display": "12:00",
      "start_dateUTC": "2024-07-12 16:00:00",
      "end_dateUTC": "2024-07-12 19:00:00",
      "available": true
    },
    {
      "start_date": "2024-07-12 13:00:00",
      "end_date": "2024-07-12 16:00:00",
      "start_date_display": "13:00",
      "end_date_display": "16:00",
      "start_dateUTC": "2024-07-12 20:00:00",
      "end_dateUTC": "2024-07-12 23:00:00",
      "available": true
    },
    {
      "start_date": "2024-07-19 13:00:00",
      "end_date": "2024-07-19 16:00:00",
      "start_date_display": "13:00",
      "end_date_display": "16:00",
      "start_dateUTC": "2024-07-19 20:00:00",
      "end_dateUTC": "2024-07-19 23:00:00",
      "available": true
    }
  ],
  "hasMore": false,
  "noApptAvailable": false,
  "timeZone": "US/Arizona"
}
```

## Appointment Open - PATCH /api/sn\_tmf\_api/appointment/appointment/\{id\}

Reschedule appointments with a given ID for a  work order.

### URL format

Default URL: `PATCH /api/sn_tmf_api/appointment/appointment/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the appointment to reschedule. Data type: String

Table: Appointment booking \[sn\_apptmnt\_booking\_appointment\_booking\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

note

</td><td>

If canceling the appointment, you can add work notes here. Updates the work notes of the work order and the message of the appointment.Data type: Array of Objects

```
"note": [ 
 {
  "author": "String", 
  "date": "String", 
  "text": "String"
 }
]
```

Stored in: Appointment Booking \[sn\_apptmnt\_booking\_appointment\_booking\] table

</td></tr><tr><td>

note.author

</td><td>

Name of the person who writing the note.Data type: String

</td></tr><tr><td>

note.date

</td><td>

Date and time that the note was published. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2018-02-04T11:00:18.071Z.

</td></tr><tr><td>

note.text

</td><td>

Descriptive text about the work order that is attached to the appointment. For example, updates on the work order's progress.Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the appointment.Valid values:

-   cancelled: The appointment reschedule is cancelled.
-   completed: The rescheduled appointment is completed.
-   confirmed: The appointment reschedule is accepted and booked.
-   new: The appointment rescheduling request was recently created.
-   pending: The appointment reschedule is pending.
-   ready: The appointment reschedule is requested.

Data type: String

</td></tr><tr><td>

validFor

</td><td>

Filter the appointment by a date range that the appointment is valid for.Data type: Object

```
"validFor":
{
  "endDateTime": "String",
  "startDateTime": "String"
}
```

Default: Returns all appointments if **validFor** is not provided.

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date and time of the appointment. Only appointments with the specified end date and time are returned in the response.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

Table: Location \[cmn\_location\]

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date and time of the appointment. Only appointments with the specified start date and time are returned in the response. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

Table: Location \[cmn\_location\]

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the request body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

creationDate

</td><td>

Date and time that the appointment was created.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

</td></tr><tr><td>

href

</td><td>

Unique reference link of the appointment. You can use this link in another request to get an appointment.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the appointment that was rescheduled.Data type: String

Stored in: Appointment booking \[sn\_apptmnt\_booking\_appointment\_booking\] table

</td></tr><tr><td>

lastUpdate

</td><td>

Date and time the appointment was last updated.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

</td></tr><tr><td>

reason

</td><td>

Purpose for updating the appointment.Possible values:

-   "Appointment rescheduled.": The PATCH method was used to reschedule the appointment.
-   "The appointment \(id\) is successfully cancelled.": The PATCH method was used to cancel the appointment.

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

Customer details of the associated appointment.Data type: Array of Objects

```
"relatedParty": [
  {
  "@referredType": "String",
  "id": "String",
  "name": "String",
  "role": "String"
  }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the customer contact.Data type: String

Stored in: Contact \[customer\_contact\] table

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the customer contact.Data type: String

</td></tr><tr><td>

relatedPlace.@referredType

</td><td>

Type of customer.Data type: String

Only possible value: Individual

</td></tr><tr><td>

relatedParty.role

</td><td>

Role of the contact.Data type: String

Only possible value: Contact

</td></tr><tr><td>

success

</td><td>

Flag that indicates whether the request was successful.Possible values:

-   true: The appointment was successfully rescheduled.
-   false: The appointment couldn't be rescheduled.

Data type: Boolean

</td></tr></tbody>
</table>### cURL request

The following example demonstrates how to use a PATCH method to reschedule an appointment with a given ID.

```
curl -X POST 'https://instance.service-now.com/api/sn_tmf_api/appointment/appointment/68cc0a5a9314521060320dd548373cbd ' \ 
-H "Accept: application/json" \ 
-H "Content-Type: application/json" \ 
-u "username":"password" \ 
-data {
  "validFor": { 
      "startDateTime": "2024-07-30 00:0:00", 
      "endDateTime": "2024-08-30 00:00:00" 
              }
  "note": {
      "date": "85388c25b71011104eed4643ae11a993",
      "author": "Sarah Johnson",
      "text": "customer"
    }
  "state": "active"
   }
  ]
}
```

The response body shows a success message that the appointment was rescheduled.

```
{
  "relatedParty": [
    {
      "id": "85388c25b71011104eed4643ae11a993",
      "name": "Sarah Johnson",
      "role": "customer",
      "@referredType": "Individual"
    }
  ],
  "success": true,
  "reason": "Appointment rescheduled!",
  "id": "68cc0a5a9314521060320dd548373cbd",
  "href": "api/sn_tmf_api/appointment/appointment/68cc0a5a9314521060320dd548373cbd",
  "creationDate": "2024-08-30 20:56:54",
  "lastUpdate": "2024-08-30 20:56:54"
}
```

## Appointment Open - POST /api/sn\_tmf\_api/appointment/appointment

Enables you to book appointments for a work order.

### URL format

`/api/sn_tmf_api/appointment/appointment`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

category

</td><td>

Required. Sys\_id of the record producer configured for the appointment booking service configuration. Data type: String

Table: In the Catalog Item field of the Appointment Booking Service Configuration \[sn\_apptmnt\_booking\_service\_config\] table.

</td></tr><tr><td>

relatedEntity

</td><td>

Required. List of impacted work orders to associate with the appointment.Data type: Array of Objects

```
"relatedEntity": [
  {
    "@referredType": "String"
    "id": "String",
  }
]
```

</td></tr><tr><td>

relatedEntity.@referredType

</td><td>

Required. Type of item or service. Only valid value: WorkOrder

Data type: String

Table: Work Order \[wm\_order\]

</td></tr><tr><td>

relatedEntity.id

</td><td>

Required. Sys\_id of the related entity.Data type: String

Table: workOrder \[wm\_order\]

Default: Returns all if sys\_id is not provided.

</td></tr><tr><td>

relatedEntity.role

</td><td>

Required. Role description of the related entity. Only valid value: work order

Data type: String

Table: Work Order \[wm\_order\]

</td></tr><tr><td>

relatedParty

</td><td>

Required. List of contacts for the appointment. Each contact is an object in the array. The request must list at least one item which contains customer account information.Data type: Array of Objects

```
"relatedParty": [ 
 {
  "@referredType": "String",
  "id": "String",
  "name": "String",
  "role": "String"
 }
]
```

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer. Only valid value: Individual

Data type: String

</td></tr><tr><td>

relatedParty.id

</td><td>

Required. Sys\_id or external\_id of the contact associated with the work order. Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the contact.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

relatedParty.role

</td><td>

Required. Role of the contact.Possible values:

-   customer: The contact has a customer role.
-   technician: The contact has a technician role.

Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

relatedPlace

</td><td>

Required. List of the locations related to the appointment.Data type: Array of Objects

```
"relatedPlace": [
 {
  "@referredType": "String",
  "id": "String",
  "name": "String",
  "role": "String"
 }
]
```

</td></tr><tr><td>

relatedPlace.@referredType

</td><td>

Required. Type of location. For example, City.Data type: String

Table: Locations \[cmn\_location\]

</td></tr><tr><td>

relatedPlace.id

</td><td>

Required. Sys\_id of the related location.Data type: String

Table: Locations \[cmn\_location\]

</td></tr><tr><td>

relatedPlace.name

</td><td>

Name of the location related to the contact. For example, 251 Reddy St, Darwin, CA 93522.Data type: String

Table: Locations \[cmn\_location\]

</td></tr><tr><td>

relatedPlace.role

</td><td>

Required. Description of the location role. For example, work order.Data type: String

</td></tr><tr><td>

timeZone

</td><td>

Required. Time zone to use when booking the specified appointment slot.Date type: String

Format: Country/city or area format, such as US/Eastern

</td></tr><tr id="serviceTest-response-testMeasureDefinition.thresholdRule.consequence.validFor"><td>

validFor

</td><td>

Required. Date range the appointment is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr id="serviceTest-response-testMeasureDefinition.thresholdRule.consequence.validFor.endDateTime"><td>

validFor.endDateTime

</td><td>

Required. End date and time of the time slot. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

</td></tr><tr id="serviceTest-response-testMeasureDefinition.thresholdRule.consequence.validFor.startDateTime"><td>

validFor.startDateTime

</td><td>

Required. Start date and time of the time slot. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the request body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

category

</td><td>

Sys\_id of the record producer configured for the appointment booking service configuration. Data type: String

Stored in: Catalog Item field of the Appointment Booking Service Configuration \[sn\_apptmnt\_booking\_service\_config\] table.

</td></tr><tr><td>

creationDate

</td><td>

Date and time that the appointment was created.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

</td></tr><tr><td>

href

</td><td>

Hyperlink to the appointment record. Use this link in another Appointment Open API request to reschedule or delete the appointment.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the appointment.Data type: String

Stored in: Appointment Booking Service Configuration \[sn\_apptmnt\_booking\_service\_config\] table

</td></tr><tr><td>

lastUpdate

</td><td>

Date and time the appointment was last updated.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

</td></tr><tr><td>

relatedEntity

</td><td>

Details about the related entity of the appointment.Data type: Array of Objects

```
"relatedEntity": [
 {
  "@referredType": "String",
  "id": "String",
  "role": "String"
  }
]
```

</td></tr><tr><td>

relatedEntity.@referredType

</td><td>

Type of item or service.Data type: String

Stored in: workOrder \[wm\_order\] table

</td></tr><tr><td>

relatedEntity.id

</td><td>

Sys\_id of the related entity.Data type: String

Stored in: workOrder \[wm\_order\] table

</td></tr><tr><td>

relatedEntity.role

</td><td>

Role description of the related entity. Possible value: work order

Data type: String

Stored in: workOrder \[wm\_order\] table

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the appointment. Each contact is an object in the array.Data type: Array of Objects

```
"relatedParty": [
 {
  "@referredType": "String",
  "id": "String",
  "name": " String",
  "role": "String"
 }
]
```

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer.Data type: String

Stored in: Contact \[customer\_contact\] table

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the customer contact associated with the work order.Data type: String

Stored in: Contact \[customer\_contact\] table

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the customer contact.Data type: String

Stored in: Contact \[customer\_contact\] table

</td></tr><tr><td>

relatedParty.role

</td><td>

Role of the customer contact.Possible values:

-   customer: The contact has a customer role.
-   technician: The contact has a technician role.

Data type: String

Stored in: Contact \[customer\_contact\] table

</td></tr><tr><td>

relatedPlace

</td><td>

Location details of the associated appointment.Data type: Object

```
"relatedPlace": {
  "@referredType": "String",
  "id": "String",
  "name": "String",
  "role": "String"
}
```

</td></tr><tr><td>

relatedPlace.@referredType

</td><td>

Geographic address of the appointment. Possible value: GeographicLocation.

Data type: String

Stored in: Location \[cmn\_location\] table

</td></tr><tr><td>

relatedPlace.id

</td><td>

Sys\_id of the location. Data type: String

Stored in: Location \[cmn\_location\] table

</td></tr><tr><td>

relatedPlace.name

</td><td>

Name of the location related to the contact. For example, 100 South Charles Street, Baltimore, MD.Data type: String

Stored in: Location \[cmn\_location\] table

</td></tr><tr><td>

relatedPlace.role

</td><td>

Role of the appointment location as an intervention address.Possible value: InterventionAddress

Data type: String

Stored in: Location \[cmn\_location\] table

</td></tr><tr><td>

success

</td><td>

Flag that indicates whether the request was successful.Possible values:

-   true: Request succeeded.
-   false: Request failed.

Data type: Boolean

</td></tr><tr><td>

timeZone

</td><td>

Time zone used when booking or updating the specified appointment slot.Date type: String

Format: Country/city or area format, such as US/Eastern

</td></tr><tr><td>

validFor

</td><td>

Date range that the appointment is valid for.Data type: Object

```
"validFor": {
 "endDateTime": "String"
 "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date and time of the appointment.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date and time of the appointment.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, 2025-01-31 09:35:43.

</td></tr></tbody>
</table>### cURL request

The following example shows how to create a new appointment booking.

```
curl "https://instance.servicenow.com/api/sn_tmf_api/appointment/appointment" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"validFor\": {
    \"startDateTime\": \"2024-08-19 09:00:00\",
    \"endDateTime\": \"2024-08-19 11:00:00\"
  },
  \"category\": \"e4c1116b3b810300ce8a4d72f3efc40f\",
  \"relatedParty\": [
    {
      \"id\": \"eaf68911c35420105252716b7d40ddde\",
      \"name\": \"Sally Thomas\",
      \"role\": \"customer\",
      \"@referredType\": \"Individual\"
    }
  ],
  \"relatedPlace\": {
    \"id\": \"25ab9c4d0a0a0bb300f7dabdc0ca7c1c\",
    \"name\": \"100 South Charles Street, Baltimore,MD\",
    \"role\": \"interventionAddress\",
    \"@referredType\": \"GeographicAddress\"
  },
  \"relatedEntity\": [
    {
      \"id\": \"48dbfbf9201f0250f877303e8a020dcd\",
      \"role\": \"work order\",
      \"@referredType\": \"WorkOrder\"
    }
  ],
  \"timeZone\": \"US/Arizona\"
}" \
--user 'username':'password'
```

Response:

```
{
  "validFor": {
    "startDateTime": "2024-07-19 09:00:00",
    "endDateTime": "2024-07-19 11:00:00"
  },
  "category": "e4c1116b3b810300ce8a4d72f3efc40f",
  "relatedParty": [
    {
      "id": "eaf68911c35420105252716b7d40ddde",
      "name": "Sally Thomas",
      "role": "customer",
      "@referredType": "Individual"
    }
  ],
  "relatedPlace": {
    "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
    "name": "100 South Charles Street, Baltimore,MD",
    "role": "interventionAddress",
    "@referredType": "GeographicAddress"
  },
  "relatedEntity": [
    {
      "id": "48dbfbf9201f0250f877303e8a020dcd",
      "role": "work order",
      "@referredType": "WorkOrder"
    }
  ],
  "timeZone": "US/Arizona",
  "success": true,
  "id": "feacb7f9201f0250f877303e8a020d38",
  "href": "api/sn_tmf_api/appointment/appointment/feacb7f9201f0250f877303e8a020d38",
  "creationDate": "2024-07-10 22:45:01",
  "lastUpdate": "2024-07-10 22:45:01"
}
```

