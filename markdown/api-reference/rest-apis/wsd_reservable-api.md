---
title: WSD Reservable API
description: The Workplace Service Delivery \(WSD\) Reservable API provides endpoints to retrieve details of a reservable, an entity that can be reserved, such as a workplace location, from a ServiceNow instance.Returns the details for one or more specified reservables.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 15
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# WSD Reservable API

The Workplace Service Delivery \(WSD\) Reservable API provides endpoints to retrieve details of a reservable, an entity that can be reserved, such as a workplace location, from a ServiceNow instance.

**Note:** A newer version of this API, [WSD Reservable V2 API](wsd_reservable-V2-api.md#), is available for use. The new version allows you to include all reservables in a POST request to avoid character limitations of the **sys\_Id** parameter.

To access this API, the caller must have the sn\_wsd\_core.workplace\_user role.

This API runs in the `sn_wsd_rsv` namespace. To access this API, the Workplace Reservation Management \(sn\_wsd\_rsv\) plugin must be activated.

For additional information on Workplace Reservation Management, see [Workplace Reservation Management](https://www.servicenow.com/docs/access?context=workplace-rsv-mgmt-feat&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## WSD Reservable - GET /sn\_wsd\_rsv/reservable/list\_reservables/\{sys\_ids\}

Returns the details for one or more specified reservables.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/reservable/list_reservables/{sys_ids}`

Default URL: `/api/sn_wsd_rsv/reservable/list_reservables/{sys_ids}`

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

sys\_ids

</td><td>

Sys\_ids of the reservables whose details to return. If specifying multiple reservables, comma separate the sys\_ids.

Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

include\_flexible\_services

</td><td>

Flag that indicates whether to return the flexible services associated with the reservable in to the response.A flexible service is an additional provision available with a reservable workplace item when a reservation is made. For example, Classroom style - Rows of tables arranged with all participants facing towards the front of the room. For additional information on flexible services, see [Create a flexible service](https://www.servicenow.com/docs/access?context=add-flexible-service&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

Valid values:

-   true: Return the flexible service information.
-   false: Don't return the flexible service information.

Data type: Boolean

Default: false

</td></tr><tr><td>

include\_layouts

</td><td>

Flag that indicates whether to return the location layout information in the response.Location layout information include such things as capacity, max capacity, preparation, and clean up duration. This information is located in the Location Layout \[sn\_wsd\_rsv\_m2m\_location\_layout\] table.

Valid values:

-   true: Return the location layout information.
-   false: Don't return the location layout information.

Data type: Boolean

Default: false

</td></tr><tr><td>

include\_standard\_​services

</td><td id="include_standard_services-reserv-entry">

Flag that indicates whether to return the standard services information in the response. This information is located in the Standard Service \[sn\_wsd\_rsv\_standard\_service\] table.A standard service describes basic provisions available with a reservable workplace item when the reservation is made, such as white boards, additional monitors, and similar services. For additional information on standard services, see [Standard services](https://www.servicenow.com/docs/access?context=standard-service&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

Valid values:

-   true: Return the standard services information.
-   false: Don't return the standard services information.

Data type: Boolean

Default: false

</td></tr><tr><td>

reservable\_module\_sys\_id

</td><td>

Required. Sys\_id of the reservable module.A reservable module groups similar types of workplace items.

For additional information on reservable modules, see [Configure a reservable module](https://www.servicenow.com/docs/access?context=config-reservable-module&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

Data type: String

Table: Reservable Module \[sn\_wsd\_rsv\_reservable\_module\]

</td></tr><tr><td>

reservation\_start\_time

</td><td id="reservation_ids-reserv-start-entry">

Reservation start time to validate the lead time of extra services.Format: UTC format, yyyy-MM-dd HH:mm:ss

Data type: String

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
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Details on each matching reservable.Data type: Array of Objects

 ```
{
  "result": [
    {
      "allow_invitees": Boolean,
      "area": {Object},
      "building": {Object},
      "campus": {Object},
      "capacity": Number,
      "description": "String",
      "display_number_of_attendees": Boolean,
      "display_on_behalf_of": Boolean,
      "display_sensitivity": Boolean,
      "email": "String",
      "employee_override_privacy": Boolean
      "enable_group_reservations": Boolean,
      "enable_reservation_privacy": Boolean,
      "external_id": "String",
      "flexible_services": [Array],
      "floor": {Object},
      "image": {Object},
      "is_reservable": Boolean,
      "layouts": [Array],
      "location_type": {Object},
      "meetingProviders": [Array],
      "moduleType": "String",
      "name": "String",
      "number": "String",
      "order": Number,
      "require_approval": Boolean,
      "requires_check_in": Boolean,
      "require_subject": Boolean,
      "reservable_quantity": Number,
      "site": {Object},
      "standard_services": [Array],
      "sys_id": "String",
      "title": "String",
      "type": "String",
      "tableName": "String"
    }
  ]
}
```

</td></tr><tr><td>

result.allow\_invitees

</td><td id="allow_invitees-reserv_mod-entry">

Flag that indicates whether employees are able to add invitees to the reservation. Valid values:

-   true: Allow employees to add invitees to the reservation.
-   false: Don't allow employees to add invitees to the reservation.

Data type: Boolean

</td></tr><tr><td>

result.area

</td><td>

Area where the reservable is located. Data type: Object

```
"area": {
   "display_value": "String",
   "sys_id": "String"
}
```

Table: Area \[sn\_wsd\_core\_area\]

</td></tr><tr><td>

result.area.display\_value

</td><td>

Display value for the area.Data type: String

</td></tr><tr><td>

result.area.sys\_id

</td><td>

Sys\_id of the associated area record.Data type: String

</td></tr><tr><td>

result.building

</td><td id="building-reserv-entry">

Building where the reservable is located.Data type: Object

```
"building": {
  "display_value": "String",
  "sys_id": "String",
  "timezone": {Object}
}
```

Table: Building \[sn\_wsd\_core\_building\]

</td></tr><tr><td>

result.building.display\_value

</td><td id="building_display_value-reserv-entry">

Display value for the building.Data type: String

</td></tr><tr><td>

result.building.sys\_id

</td><td id="building_sys_id-reserv-entry">

Sys\_id of the associated building record.Data type: String

</td></tr><tr><td>

result.building.timezone

</td><td id="building_timezone-reserv-entry">

Details of the time zone for the building.Data type: Object

```
"timezone": {
  "displayValue": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.building.timezone.display\_value

</td><td id="building_timezone_display_value-reserv-entry">

Display value of the time zone in which the associated building resides.Data type: String

</td></tr><tr><td>

result.building.timezone.value

</td><td id="building_timezone_value-reserv-entry">

Internal value of the time zone in which the associated building resides.Data type: String

</td></tr><tr><td>

result.campus

</td><td>

Campus where the reservable is located. Data type: Object

```
"campus": {
  "display_value": "String",
  "sys_id": "String"
}
```

Table: Campus \[sn\_wsd\_core\_campus\]

</td></tr><tr><td>

result.campus.display\_value

</td><td>

Display value for the campus.Data type: String

</td></tr><tr><td>

result.campus.sys\_id

</td><td>

Sys\_id of the associated campus record.Data type: String

</td></tr><tr><td>

result.capacity

</td><td>

Number of people that the reservable can accommodate.Data type: Number

</td></tr><tr><td>

result.description

</td><td>

Description of the reservable.

 Data type: String

</td></tr><tr><td>

result.display\_number\_of\_attendees

</td><td id="display_number_of_attendees-reserv_mod-entry">

Flag that indicates whether users can specify the number of attendees in the reservation. Valid values:

-   true: Users can specify the number of attendees.
-   false: Users can't specify the display number of attendees.

Data type: Boolean

</td></tr><tr><td>

result.display\_on\_behalf\_of

</td><td id="display_on_behalf_of-reserv_mod-entry">

Flag that indicates whether reservations can be made on behalf of someone else. Valid values:

-   true: On behalf of supported.
-   false: On behalf of not supported.

Data type: Boolean

</td></tr><tr><td>

result.display\_sensitivity

</td><td id="display_sensitivity-reserv_mod-entry">

Flag that indicates whether users can set the sensitivity of the reservation, such as normal or private.Valid values:

-   true: Able to set sensitivity.
-   false: Not able to set sensitivity. Defaults to normal.

Data type: Boolean

</td></tr><tr><td>

result.email

</td><td>

Email address associated with the reservable.Data type: String

</td></tr><tr><td>

result.employee\_override\_privacy

</td><td>

Flag that indicates whether users can override the privacy setting for the associated reservable.For additional information on these privacy settings, see [Location privacy settings and impact](https://www.servicenow.com/docs/access?context=location-privacy-settings-and-impact&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

 Valid values:

-   true: Users can override the privacy setting for the associated reservable.
-   false: Users cannot override the privacy setting for the associated reservable.

</td></tr><tr><td>

result.enable\_group\_reservations

</td><td id="enable_group_reservations-reserv_mod-entry">

Flag that indicates whether users can make a group reservation.Valid values:

-   true: Able to make group reservations.
-   false: Not able to make group reservations.

Data type: Boolean

</td></tr><tr><td>

result.enable\_reservation\_privacy

</td><td>

Flag that indicates the default setting for reservation privacy.

 For additional information on these privacy settings, see [Location privacy settings and impact](https://www.servicenow.com/docs/access?context=location-privacy-settings-and-impact&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

 Possible values:

-   true: Reservations are private by default.
-   false: Reservations are not private by default.

 Data type: Boolean

</td></tr><tr><td>

result.external\_id

</td><td>

External ID of the reservable.Data type: String

</td></tr><tr><td>

result.flexible\_services

</td><td>

Populated only if the **include\_flexible\_services** parameter is set to true and the workplace case management plugin is installed. Description of the flexible services associated with the reservables. There can be a parent flexible service, and several child flexible services. Data type: Object

```
flexible_services": [
  {
    "additional_text": "String",
    "allow_only_single_service_item_selection": Boolean,
    "category": "String",
    "currency_code": "String",
    "flexible_service": [Array],
    "label": "String",
    "sub_category": "String",
    "sub_title": "String",
    "text": "String",
    "title": {Object}
  }
]
```

Table: Workplace Service Item \[sn\_wsd\_case\_workplace\_service\_item\]

</td></tr><tr><td>

result.flexible\_services.additional\_text

</td><td>

Text to prompt user to select additional flexible services. Data type: String

</td></tr><tr><td>

result.flexible\_services.allow\_only\_single\_​service\_item\_selection

</td><td>

Flag that indicates whether users can select only one service item among the group of flexible services within a reservation.Valid values:

-   true: Only able to make a single selection.
-   false: Able to make multiple selections.

Data type: Boolean

</td></tr><tr><td>

result.flexible\_services.category

</td><td>

Category of the flexible services.Data type: String

</td></tr><tr><td>

result.flexible\_services.currency\_code

</td><td>

Currency code used to calculate the amount of currency when ordering flexible services.Data type: String

</td></tr><tr><td>

result.flexible\_services.flexible\_service

</td><td>

Flexible services corresponding to a parent flexible service.Data type: Array of Objects

```
"flexible_service": [
  {
    "flexible_service": [Array],
    "label": "String",
    "sub_category": "String"
 }
]
```

Table: Workplace Service Item \[sn\_wsd\_case\_workplace\_service\_item\]

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service

</td><td>

Details of each flexible service corresponding to a parent flexible service.Data type: Array of Objects

```
"flexible_service": [
  {
    "additional_text": "String",
    "capacity_enabled": Boolean,
    "category": "String",
    "category_label": "String",
    "cleanup_duration": "String",
    "image": "String",
    "max_capacity": Number,
    "name": "String",
    "preparation_duration": "String",
    "price_per_unit": {Object},
    "quantity_enabled": Boolean,
    "quantity_required": Boolean,
    "short_description": "String",
    "sub_category": "String",
    "sub_category_label": "String",
    "sub_title": "String",
    "sys_id": "String",
    "text": "String",
    "title": {Object}
  }
]
```

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service.additional\_text

</td><td>

Text used to prompt a user to select additional flexible services.Data type: String

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service.capacity\_enabled

</td><td>

Flag that indicates whether the capacity of the room should appear in the reservation. If this is set to true, **quantity\_enabled** will always be false.Valid values:

-   true: Capacity should appear.
-   false: Capacity should not appear.

Data type: Boolean

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service.category

</td><td>

Category of the flexible service.Data type: String

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service.category\_label

</td><td>

Category label of flexible service.Data type: String

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service.cleanup\_duration

</td><td>

Amount of time it takes to clean up or remove the service added to the reservable.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service.image

</td><td>

Link to the image of the flexible service.Data type: String

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service.max\_capacity

</td><td>

Maximum number of occupants that the reservable can accommodate.Data type: Number

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service.name

</td><td>

Name of flexible service.Data type: String

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service.preparation\_duration

</td><td>

Amount of time it takes to add the service to the reservable.Data type: String

Unit: Milliseconds

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service.price\_per\_unit

</td><td>

Details of the cost of adding the flexible service to the reservable.Data type: Object

```
"price_per_unit": {
  "code": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service.price\_per\_unit.code

</td><td>

Currency code to use when calculating the cost, such as GBP or USD.Data type: String

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service.price\_per\_unit.value

</td><td>

Cost for each unit of the flexible service in the currency defined in the code parameter.Data type: String

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service.quantity\_enabled

</td><td>

Flag that indicates whether the quantity field should appear in the reservation. If this is set to true, **capacity\_enabled** will always be false.Valid values:

-   true: Quantity should appear.
-   false: Quantity should not appear.

Data type: Boolean

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service.quantity\_required

</td><td>

Flag that indicates whether the quantity is required.Valid values:

-   true: Quantity is required.
-   false: Quantity is not required.

Data type: Boolean

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service.short\_description

</td><td>

Brief description of the flexible service.Data type: String

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service.sub\_category

</td><td>

Sub-category name of the flexible service, such as chair\_layout.Data type: String

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service.sub\_category\_label

</td><td>

Sub-category label of the flexible service, such as Chair layout.Data type: String

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service.sub\_title

</td><td>

Sub-title name of the child flexible service.Data type: String

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service.sys\_id

</td><td>

Sys\_id of flexible service. Data type: String

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service.text

</td><td>

Text used to prompt a user to select flexible services.Data type: String

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service.title

</td><td>

Details for the titles to use when adding and editing the child flexible service in the UI.Data type: Object

```
"title": {
  "add": "String",
  "edit": "String"
}
```

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service.title.add

</td><td>

Title used when adding a child flexible service in the UI.Data type: String

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​flexible\_service.title.edit

</td><td>

Title used when editing a child flexible service in the UI.Data type: String

</td></tr><tr><td>

result.flexible\_services.flexible\_service.label

</td><td>

Flexible service label.Data type: String

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​sub\_category

</td><td>

Sub-category of the parent flexible services, such as additional chair.Data type: String

</td></tr><tr><td>

result.flexible\_services.flexible\_service.​sub\_title

</td><td>

Sub-title name of the parent flexible service.Data type: String

</td></tr><tr><td>

result.flexible\_services.flexible\_service.text

</td><td>

Text used to prompt a user to select a parent flexible services.Data type: String

</td></tr><tr><td>

result.flexible\_services.flexible\_service.title

</td><td>

Details for the titles to use when adding and editing the parent flexible service in the UI.Data type: Object

```
"title": {
  "add": "String",
  "edit": "String"
}
```

</td></tr><tr><td>

result.flexible\_services.flexible\_service.title.​add

</td><td>

Title used when adding a parent flexible service in the UI.Data type: String

</td></tr><tr><td>

result.flexible\_services.flexible\_service.title.​edit

</td><td>

Title used when editing a parent flexible service in the UI.Data type: String

</td></tr><tr><td>

result.floor

</td><td>

Details about the floor on which the reservable is located.Data type: Object

```
"floor": {
  "display_value": "String",
  "sys_id": "String"
}
```

Table: Floor \[sn\_wsd\_core\_floor\]

</td></tr><tr><td>

result.floor.display\_value

</td><td id="floor_display_value-reserv-entry">

Display number of the floor on which the reservable resides, such as 12.Data type: String

</td></tr><tr><td>

result.floor.sys\_id

</td><td>

Sys\_id of the associated record in the Floor table.Data type: String

</td></tr><tr><td>

result.image

</td><td>

Details about an image that represents the associated reservable.Data type: Object

```
"image": {
  "link": "String",
  "sys_id": "String"
}
```

Table: Images \[db\_image\]

</td></tr><tr><td>

result.image.link

</td><td>

Link to an image that represents the reservable.Data type: String

</td></tr><tr><td>

result.image.sys\_id

</td><td>

Sys\_id of the associated image record.Data type: String

</td></tr><tr><td>

result.is\_reservable

</td><td>

Flag that indicates whether the flexible service can be reserved.Valid values:

-   true: Flexible service can be reserved.
-   false: Flexible service can't be reserved.

Data type: Boolean

</td></tr><tr><td>

results.layouts

</td><td id="layouts-reserv-entry">

Only populated if the **include\_layouts** parameter is set to true.List of the layouts associated with the reservable.

Data type: Array of Objects

```
"layouts": [
  {
    "capacity": Number,
    "cleanup_duration": "String",
    "image": {Object},
    "is_default": Boolean,
    "max_capacity": Number,
    "name": "String",
    "preparation_duration": "String",
    "short_description": "String",
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.layouts.capacity

</td><td id="layouts_capacity-reserv-entry">

Number of people that will attend the meeting.Data type: Number

</td></tr><tr><td>

result.layouts.cleanup\_duration

</td><td id="layouts_cleanup_duration-reserv-entry">

Amount of time it takes to clean the reservable for this layout.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

result.layouts.image

</td><td id="layouts_image-reserv-entry">

Details about an image that represents the layout for the associated reservable.Data type: Object

```
"image": {
  "link": "String",
  "sys_id": "String"
}
```

Table: Images \[db\_image\]

</td></tr><tr><td>

result.layouts.image.link

</td><td id="layouts_image_link-reserv-entry">

Link to an image that represents the layout for this reservable.Data type: String

Table: Images \[db\_image\]

</td></tr><tr><td>

result.layouts.image.sys\_id

</td><td id="layouts_image_sys_id-reserv-entry">

Sys\_id of the associated image record.Data type: String

</td></tr><tr><td>

result.layouts.is\_default

</td><td id="layouts_is_default-reserv-entry">

Flag that indicates whether the associated layout is the default for the reservable. Valid values:

-   true: Default.
-   false: Not default.

Data type: Boolean

</td></tr><tr><td>

result.layouts.max\_capacity

</td><td id="layouts_max_capacity-reserv-entry">

Maximum number of people that the layout associated with the reservable can accommodate.Data type: Number

</td></tr><tr><td>

result.layouts.name

</td><td id="layouts_name-reserv-entry">

Name of the location layout. Data type: String

</td></tr><tr><td>

result.layouts.preparation\_duration

</td><td id="layouts_preparation_duration-reserv-entry">

Amount of time it takes to prepare the associated location layout.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

result.layouts.short\_description

</td><td id="layouts_short_description-reserv-entry">

Brief description of the location layout.Data type: String

</td></tr><tr><td>

result.layouts.sys\_id

</td><td id="layouts_sys_id-reserv-entry">

Sys\_id of the location layout.Data type: String

Table: Layout \[sn\_wsd\_rsv\_layout\]

</td></tr><tr><td>

result.location\_type

</td><td id="location_type-reserv-entry">

Details about the type of location of the reservable, such as workplace/desk, cafe, or gym.Data type: Object

```
"location_type": {
  "display_value": "String",
  "sys_id": "String"
}
```

Table: Space Type \[sn\_wsd\_core\_space\_type\]

</td></tr><tr><td>

result.location\_type.display\_value

</td><td id="location_type_display_value-reserv-entry">

Display value of the location type.Data type: String

</td></tr><tr><td>

result.location\_type.sys\_id

</td><td id="location_type_sys_id-reserv-entry">

Sys\_id of the associated record.Data type: String

Table: Space Type \[sn\_wsd\_core\_space\_type\]

</td></tr><tr><td>

result.meetingProviders

</td><td>

Details about the virtual meeting providers associated with the reservable.Data type: Array of Objects

```
"meetingProviders": [
  {
    "display_value": "String",
    "value": "String"
  }
]
```

Table: Virtual Meeting Provider \[sn\_wsd\_rsv\_virtual\_meeting\_provider\]

</td></tr><tr><td>

result.meetingProviders.display\_value

</td><td>

Display value of the virtual provider's name.Data type: String

</td></tr><tr><td>

result.meetingProviders.value

</td><td>

Actual value for the virtual provider's name in the record.Data type: String

</td></tr><tr><td>

result.moduleType

</td><td>

Reservable module associated with the reservable, such as desks or meeting room.Data type: String

</td></tr><tr><td>

result.name

</td><td id="name-reserv-entry">

Name of the reservable.Data type: String

</td></tr><tr><td>

result.number

</td><td id="number-reserv-entry">

Unique identifier of the reservable. This value is more human readable than the sys\_id.Data type: String

</td></tr><tr><td>

result.order

</td><td id="order-reserv-entry">

Order number for the reservable.Data type: Number

</td></tr><tr><td>

result.require\_approval

</td><td id="require_approval-reserv-entry">

Flag that indicates whether reserving the reservable requires an approval.Possible values:

-   true: Approval required.
-   false: Approval isn't required.

Data type: Boolean

</td></tr><tr><td>

result.requires\_check\_in

</td><td id="requires_check_in-reserv-entry">

Flag that indicates whether the reservable requires the user to check in.Valid values:

-   true: Check in required.
-   false: Check in isn't required.

Data type: Boolean

</td></tr><tr><td>

result.require\_subject

</td><td id="require_subject-reserv_mod-entry">

Flag that indicates whether the user must enter a subject when making the reservation.Valid values:

-   true: Subject required.
-   false: Subject isn't required.

Data type: Boolean

</td></tr><tr><td>

result.reservable\_quantity

</td><td id="reservable_quantity-reserv-entry">

Maximum number of times the associated reservable can be reserved for the same time. This value is used when assigning neighborhood spaces to an area.Data type: Integer

</td></tr><tr><td>

result.site

</td><td id="site-reserv-entry">

Details about the site where the reservable resides.Data type: Object

```
"site": {
  "display_value": "String",
  "sys_id": "String"
}
```

Table: Site \[sn\_wsd\_core\_site\]

</td></tr><tr><td>

result.site.display\_value

</td><td id="site_display_value-reserv-entry">

Display value of the site.Data type: String

</td></tr><tr><td>

result.standard\_services

</td><td id="std_serv-reserv-entry">

Only populated if the **include\_standard\_services** parameter is set to true. Associated standard services, such as flip chart, projector screen, and whiteboard and markers.

Data type: Array of Objects

```
"standard_services": [
  {
    "font_awesome_icon": "String",
    "name": "String",
    "short_description": "String",
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.standard\_services.font\_awesome\_icon

</td><td id="std_serv_font-awesome_icon-reserv-entry">

Name of the thumbnail icon associated with the standard service.Data type: String

</td></tr><tr><td>

result.standard\_services.name

</td><td id="std_serv_name-reserv-entry">

Name of the standard service.Data type: String

</td></tr><tr><td>

result.standard\_services.short\_description

</td><td id="std_serv_short_description-reserv-entry">

Brief description of the standard service.Data type: String

</td></tr><tr><td>

result.standard\_services.sys\_id

</td><td id="std_serv_sys_id-reserv-entry">

Sys\_id of the standard service record.Data type: String

Table: Standard Service \[sn\_wsd\_rsv\_standard\_service\]

</td></tr><tr><td>

result.site.sys\_id

</td><td id="site_sys_id-reserv-entry">

Sys\_id of the associated site record.Data type: String

Table: Site \[sn\_wsd\_core\_site\]

</td></tr><tr><td>

result.tableName

</td><td id="tableName-reserv-entry">

Name of the table in which the reservable record resides. Data type: String

</td></tr><tr><td>

result.title

</td><td id="title-reserv-entry">

Title of the reservable.Data type: String

</td></tr><tr><td>

result.type

</td><td id="type-reserv-entry">

Type of a reservable, such as location.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl "http://instance.servicenow.com/api/sn_wsd_rsv/reservable/list_reservables/dad3df5977220110b3d7be377b5a99ce,3ed3139977220110b3d7be377b5a99d1?include_flexible_services=true&include_layouts=false&include_reservable_purposes=true&include_standard_services=true&reservable_module_sys_id=c31241cedb7650106c731dcd13961917" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Return results:

```
{
  "result": [
    {
      "sys_id": "3e41e94adb7210106c731dcd1396198c",
      "external_id": null,
      "wsd_email": null,
      "name": "A1-02-04",
      "title": "A1-02-04",
      "description": "General desk available for reservation.",
      "image": null,
      "number": "SPCE0009004",
      "site": {
        "sys_id": "628eec06db7650106c731dcd139619dd",
        "display_value": "North America"
      },
      "campus": {
        "sys_id": "82b2a0cedb3650106c731dcd139619e9",
        "display_value": "California Campus"
      },
      "building": {
        "sys_id": "94e264cedb3650106c731dcd13961919",
        "display_value": "CAL-B1",
        "timezone": {
          "value": "US/Pacific",
          "displayValue": "US/Pacific"
        }
      },
      "floor": {
        "sys_id": "fc7368cedb3650106c731dcd13961902",
        "display_value": "Floor 1"
      },
      "area": null,
      "capacity": "1",
      "reservable_quantity": null,
      "location_type": {
        "sys_id": "5f017383eb512010b89bfdfc9c5228c8",
        "display_value": "Workspace/Desk"
      },
      "order": null,
      "requires_check_in": null,
      "is_reservable": "1",
      "type": "location",
      "moduleType": "Desks",
      "meetingProviders": [],
      "require_subject": false,
      "allow_invitees": true,
      "display_number_of_attendees": false,
      "display_on_behalf_of": true,
      "display_sensitivity": false,
      "enable_group_reservations": false,
      "enable_reservation_privacy": true,
      "employee_override_privacy": true,
      "tableName": "sn_wsd_core_space",
      "require_approval": false
    },
    {
      "sys_id": "fd41a94adb7210106c731dcd1396195a",
      "external_id": null,
      "wsd_email": null,
      "name": "A1-02-03",
      "title": "A1-02-03",
      "description": "General desk available for reservation.",
      "image": null,
      "number": "SPCE0009003",
      "site": {
        "sys_id": "628eec06db7650106c731dcd139619dd",
        "display_value": "North America"
      },
      "campus": {
        "sys_id": "82b2a0cedb3650106c731dcd139619e9",
        "display_value": "California Campus"
      },
      "building": {
        "sys_id": "94e264cedb3650106c731dcd13961919",
        "display_value": "CAL-B1",
        "timezone": {
          "value": "US/Pacific",
          "displayValue": "US/Pacific"
        }
      },
      "floor": {
        "sys_id": "fc7368cedb3650106c731dcd13961902",
        "display_value": "Floor 1"
      },
      "area": null,
      "capacity": "1",
      "reservable_quantity": null,
      "location_type": {
        "sys_id": "5f017383eb512010b89bfdfc9c5228c8",
        "display_value": "Workspace/Desk"
      },
      "order": null,
      "requires_check_in": null,
      "is_reservable": "1",
      "type": "location",
      "moduleType": "Desks",
      "meetingProviders": [],
      "require_subject": false,
      "allow_invitees": true,
      "display_number_of_attendees": false,
      "display_on_behalf_of": true,
      "display_sensitivity": false,
      "enable_group_reservations": false,
      "enable_reservation_privacy": true,
      "employee_override_privacy": true,
      "tableName": "sn_wsd_core_space",
      "require_approval": false
    }
  ]
}
```

