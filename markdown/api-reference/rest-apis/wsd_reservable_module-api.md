---
title: WSD Reservable Module API
description: The Workplace Service Delivery \(WSD\) Reservable Module API provides endpoints to retrieve details of a reservable module from a ServiceNow instance.Returns the details for a specified reservable module.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 17
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# WSD Reservable Module API

The Workplace Service Delivery \(WSD\) Reservable Module API provides endpoints to retrieve details of a reservable module from a ServiceNow instance.

A reservable module groups similar types of workplace items. Employees can view these similar items in a single category. For example, a room is a reservable module and it contains similar workplace items such as meeting rooms, conference rooms, and other rooms.

To access this API, the caller must have the sn\_wsd\_core.workplace\_user role and the Workplace Reservation Management \(sn\_wsd\_rsv\) plugin must be activated. This API runs in the `sn_wsd_rsv` namespace.

For additional information on Workplace Reservation Management, see [Workplace Reservation Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/workplace-rsv-mgmt-feat.md).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## WSD Reservable Module - GET /sn\_wsd\_rsv/reservable\_module/\{sys\_id\}

Returns the details for a specified reservable module.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/reservable_module/{sys_id}`

Default URL: `/api/sn_wsd_rsv/reservable_module/{sys_id}`

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

sys\_id

</td><td>

Sys\_id of the reversable module record to retrieve.Data type: String

Table: Reservable Module \[sn\_wsd\_rsv\_reservable\_module\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

is\_buildings\_tree\_data\_required

</td><td>

Flag that indicates whether to return the building data associated with the reservable model.Valid values:

-   true: Return the building data.
-   false: Don't return the building data.

Data type: Boolean

Default: false

</td></tr><tr><td>

neighborhood

</td><td>

Only available if the Space Management \(sn\_wsd\_spc\_mgmt\_neighborhood\) plugin is activated.

Sys\_id of the neighborhood record to use in the encoded query.

For additional information on neighborhood space reservations, see [Create neighborhood reservations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/create-neighborhood-reservations.md).

 The endpoint checks if the neighborhood is valid and then retrieves the data required for the browse-by-neighborhood path.

 Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_l3d_swn_1yb" class="rest_api_request_headers"><thead><tr><th>

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

### Response body parameters \(JSON or XML\)

<table id="id_w24_zwn_1yb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

results

</td><td>

Details for the requested reservable module.Data type: Object

```
{
  "result": {
    "allow_invitees": Boolean,
    "allow_whole_day": Boolean,
    "apply_to_shift": Boolean,
    "browse_by_area_enabled": Boolean,
    "browse_by_neighborhood_enabled": Boolean,
    "browse_near_a_person_enabled": Boolean,
    "buildingsTreeData": [Array],
    "buildingSysIds": [Array],
    "checkin_before_minutes": Number,
    "display_number_of_attendees": Boolean,
    "display_on_behalf_of": Boolean,
    "display_sensitivity": Boolean,
    "display_value": "String",
    "enable_browse_by_area": Boolean,
    "enable_browse_by_neighborhood": Boolean,
    "enable_browse_near_a_person": Boolean,
    "enable_facet_filter": Boolean,
    "enable_group_reservations": Boolean,
    "enable_ical_generation": Boolean,
    "font_awesome_icon": "String",
    "inline_title": "String",      
    "layout_mapping": {JSON Object},
    "max_days_in_future": Number,
    "max_occurrences": Number,
    "name": "String",
    "nbhBuildingIds": [Array],
    "nbhBuildingsData": [Array];
    "nbhBuildingsTreeData": [Array],
    "override_approval_policy": "String",
    "require_cancel_notes": Boolean,
    "require_cc_dept_check": Boolean,
    "require_subject": Boolean,
    "reservable_columns": [Array],
    "reservable_container_field": "String",
    "reservable_filter": "String",
    "reservable_quantity_field": "String",
    "reservable_table": "String",
    "reservable_type": "String",
    "reservable_views": [Array],
    "reservation_paths": [Array],
    "search_limit": Number,
    "selection_type": "String",
    "short_description": "String",
    "show_map_view": Boolean,
    "sys_id": "String",
    "timeSlots": [Array],
    "title": "String",
    "virtual_meeting_provider": {Object}
  }
}
```

</td></tr><tr id="allow_invitees-reserv_mod-row"><td>

result.allow\_invitees

</td><td id="allow_invitees-reserv_mod-entry">

Flag that indicates whether employees are able to add invitees to the reservation. Valid values:

-   true: Allow employees to add invitees to the reservation.
-   false: Don't allow employees to add invitees to the reservation.

Data type: Boolean

</td></tr><tr id="allow_whole_day-reserv_mod-row"><td>

result.allow\_whole\_day

</td><td id="allow_whole_day-reserv_mod-entry">

Flag that indicates whether users can reserve the reservable for the entire day. Valid values:

-   true: Allow users to reserve for the entire day.
-   false: Don't allow users to reserve for the entire day.

Data type: Boolean

</td></tr><tr id="apply_to_shift-reserv_mod-row"><td>

result.apply\_to\_shift

</td><td id="apply_to_shift-reserv_mod-entry">

Flag that indicates whether shift-based reservations are enabled for the reservable module. Valid values:

-   true: Allow shift-based reservations.
-   false: Don't allow shift-based reservations.

Data type: Boolean

</td></tr><tr id="browse_by_area_enabled-reserv_mod-row"><td>

result.browse\_by\_area\_enabled

</td><td id="browse_by_area_enabled-reserv_mod-entry">

Flag that indicates whether users are able to search for reservable modules by area.Valid values:

-   true: Allow users to browse reservable modules by area.
-   false: Don't allow users to browse reservable modules by area.

Data type: Boolean

</td></tr><tr><td>

result.browse\_by\_neighborhood\_enabled

</td><td>

Only available if the Space Management - sn\_wsd\_spc\_mgmt plugin is installed.Flag that indicates whether users are able to search in the reservable modules by neighborhood.

Valid values:

-   true: Allow users to browse reservable modules by neighborhood.
-   false: Don't allow users to browse reservable modules by neighborhood.

Data type: Boolean

</td></tr><tr id="browse_near_a_person_enabled-reserv_mod-row"><td>

result.browse\_near\_a\_person\_enabled

</td><td id="browse_near_a_person_enabled-reserv_mod-entry">

Flag that indicates whether users are able to search for reservable modules located by a specified person.Valid values:

-   true: Allow users to browse reservable modules near a person.
-   false: Don't allow users to browse reservable modules near a person.

Data type: Boolean

</td></tr><tr id="buildingTreeData-reserv_mod-row"><td>

result.buildingTreeData

</td><td>

Only returned if the **is\_buildings\_tree\_data\_required** query parameter is set to `true`. Hierarchy of the buildings associate with the reservable module.Hierarchy order:

-   Region: Located in the Region \[sn\_wsd\_core\_region\] table.
-   Site: Located in the Site \[sn\_wsd\_core\_site\] table.
-   Campus: Located in the Campus \[sn\_wsd\_core\_campus\] table.
-   Building: Located in the Building \[sn\_wsd\_core\_building\] table.

Each `children[ ]` node reflects a different building level/hiearchy:

-   buildingsTreeData: Region
-   buildingsTreeData.children: Site
-   buildingsTreeData.children.children: Campus
-   buildingsTreeData.children.children.children: Building

Data type: Array of Objects

```
"buildingsTreeData": [
  {
    "children": [Array],
    "data": {Object},
    "isSelectable": Boolean,
    "isValid": Boolean,
    "label": "String",
    "uId": "String"
  }
]
```

</td></tr><tr><td>

result.buildingsTreeData.children

</td><td>

Details on the site, campus, or building associated with the reservable module. Each of the parameters in all `children[ ]` nodes are the same. They just apply to different building entities and are only described one time in this section.Data type: Array of Objects

```
"children": [
  {
    "children": [Array],
    "data": {Object},
    "isSelectable": Boolean,
    "isValid": Boolean,
    "label": "String",
    "uId": "String"
  }
]
```

</td></tr><tr><td>

result.buildingsTreeData.children.data

</td><td>

Details about the building entity.Data type: Object

```
"data": {
  "sysId": "String",
  "table": "String",
  "timezone": {Object}
}
```

</td></tr><tr><td>

result.buildingsTreeData.children.data.sys\_id

</td><td>

Sys\_id of the associated building entity.Data type: String

</td></tr><tr><td>

result.buildingsTreeData.children.data.table

</td><td>

Name of the table in which the building entity record identified in the sys\_id is located.Data type: String

</td></tr><tr><td>

result.buildingsTreeData.children.data.​timezone

</td><td>

Details about the time zone of the building entity.```
"timezone": {
  "displayValue": "String",
  "value":  "String"
}
```

</td></tr><tr><td>

result.buildingsTreeData.children.data.​timezone.displayValue

</td><td>

Display value in the record for the time zone.Data type: String

</td></tr><tr><td>

result.buildingsTreeData.children.data.​timezone.value

</td><td>

Internal value in the record for the time zone.Data type: String

</td></tr><tr><td>

result.buildingsTreeData.children.isSelectable

</td><td>

Flag that indicates whether the associated building entity is available \(selectable\) for the reservable model.Valid values:

-   true: Building entity is available for the reservable module.
-   false: Building entity isn't available for the reservable module.

Data type: Boolean

</td></tr><tr><td>

result.buildingsTreeData.children.isValid

</td><td>

Flag that indicates whether the associated building entity is valid for the reservable model.Valid values:

-   true: Building entity is valid for the reservable module.
-   false: Building entity isn't valid for the reservable module.

Data type: Boolean

</td></tr><tr><td>

result.buildingsTreeData.children.label

</td><td>

Name of the building entity.Data type: String

</td></tr><tr><td>

result.buildingsTreeData.children.uId

</td><td>

Sys\_id of the associated building entity record.Data type: String

</td></tr><tr id="buildingSysIds-reserv_mod-row"><td>

result.buildingSysIds

</td><td id="buildingSysIds-reserv_mod-entry">

List of sys\_ids of the buildings associated with the reservable module.Data type: Array of Strings

</td></tr><tr id="checkin_before_minutes-reserv_mod-row"><td>

result.checkin\_before\_minutes

</td><td id="checkin_before_minutes-reserv_mod-entry">

Amount of time before a reservation starts that a user can check into their reservation.Unit: Minutes

Data type: Number

</td></tr><tr id="display_number_of_attendees-reserv_mod-row"><td>

result.display\_number\_of\_attendees

</td><td id="display_number_of_attendees-reserv_mod-entry">

Flag that indicates whether users can specify the number of attendees in the reservation. Valid values:

-   true: Users can specify the number of attendees.
-   false: Users can't specify the display number of attendees.

Data type: Boolean

</td></tr><tr id="display_on_behalf_of-reserv_mod-row"><td>

result.display\_on\_behalf\_of

</td><td id="display_on_behalf_of-reserv_mod-entry">

Flag that indicates whether reservations can be made on behalf of someone else. Valid values:

-   true: On behalf of supported.
-   false: On behalf of not supported.

Data type: Boolean

</td></tr><tr id="display_sensitivity-reserv_mod-row"><td>

result.display\_sensitivity

</td><td id="display_sensitivity-reserv_mod-entry">

Flag that indicates whether users can set the sensitivity of the reservation, such as normal or private.Valid values:

-   true: Able to set sensitivity.
-   false: Not able to set sensitivity. Defaults to normal.

Data type: Boolean

</td></tr><tr id="display_value-reserv_mod-row"><td>

result.display\_value

</td><td id="display_value-reserv_mod-entry">

Display value of the reservable module.Data type: String

</td></tr><tr id="enable_browse_by_area-reserv_mod-row"><td>

result.enable\_browse\_by\_area

</td><td id="enable_browse_by_area-reserv_mod-entry">

Flag that indicates whether users are able to search for reservable modules by area. Same as **browse\_by\_area\_enabled**.Valid values:

-   true: Allow users to browse reservable modules by area.
-   false: Don't allow users to browse reservable modules by area.

Data type: Boolean

</td></tr><tr><td>

result.enable\_browse\_by\_neighborhood

</td><td>

Flag that indicates whether users are able to search for reservable modules by neighborhood.Valid values:

-   true: Allow users to browse reservable modules by neighborhood.
-   false: Don't allow users to browse reservable modules by neighborhood.

Data type: Boolean

</td></tr><tr id="enable_browse_by_person-reserv_mod-row"><td>

result.enable\_browse\_near\_a\_person

</td><td id="enable_browse_near_a_person-reserv_mod-entry">

Flag that indicates whether users are able to search for reservable modules located by a specified person. Same as**browse\_near\_a\_person\_enabled**.Valid values:

-   true: Allow users to browse reservable modules near a person.
-   false: Don't allow users to browse reservable modules near a person.

Data type: Boolean

</td></tr><tr id="enable_facet_filter-reserv_mod-row"><td>

result.enable\_facet\_filter

</td><td id="enable_facet_filter-reserv_mod-entry">

Flag that indicates whether facet filtering on workplace items is enabled. When enabled, the filter options that appear are based on the search results. Only the items that are available in the generated search result are available to users for selection in the filter.Valid values:

-   true: Facet filters are enabled.
-   false: Facet filters aren't enabled.

Data type: Boolean

</td></tr><tr id="enable_group_reservations-reserv_mod-row"><td>

result.enable\_group\_reservations

</td><td id="enable_group_reservations-reserv_mod-entry">

Flag that indicates whether users can make a group reservation.Valid values:

-   true: Able to make group reservations.
-   false: Not able to make group reservations.

Data type: Boolean

</td></tr><tr id="enable_ical_generation-reserv_mod-row"><td>

result.enable\_ical\_generation

</td><td id="enable_ical_generation-reserv_mod-entry">

Flag that indicates whether users can generate an iCalendar for the reservation.Valid values:

-   true: iCalendar generation allowed.
-   false: iCalendar generation isn't allowed.

Data type: Boolean

</td></tr><tr id="font_awesome_icon-reserv_mod-row"><td>

result.font\_awesome\_icon

</td><td id="font_awesome_icon-reserv_mod-entry">

Name of the font icon attached to the reservable module.Data type: String

</td></tr><tr id="inline_title-reserv_mod-row"><td>

result.inline\_title

</td><td id="inline_title-reserv_mod-entry">

Inline title of the reservable module. The title appears in line with the descriptive text on the Workplace service portal.Data type: String

</td></tr><tr id="layout_mapping-reserv_mod-row"><td>

result.layout\_mapping

</td><td id="layout_mapping-reserv_mod-entry">

Details about the structure of the layout mapping of locations. Use this data to lay out the information in the UI. Data type: Object

```
"layout_mapping": {
  "body": [Array],
  "description": [Array],
  "image": "String",
  "subtitle": [Array],
  "subtitle_asc": [Array],
  "title": [Array]
}
```

</td></tr><tr id="layout_mapping_body-reserv_mod-row"><td>

result.layout\_mapping.body

</td><td id="layout_mapping_body-reserv_mod-entry">

Placeholder for mapping the front-end UI data.Data type: Array of Objects

```
"body": [
  {
    "field": "String",
    "field_to_display": "String",
    "icon": "String",
    "label": "String"
  }
]
```

</td></tr><tr id="layout_mapping_body_field-reserv_mod-row"><td>

result.layout\_mapping.body.field

</td><td id="layout_mapping_body_field-reserv_mod-entry">

Placeholder for mapping the front-end UI data.Data type: String

</td></tr><tr id="layout_mapping_body_field_to_display-reserv_mod-row"><td>

result.layout\_mapping.body.field\_to\_display

</td><td id="layout_mapping_body_field_to_display-reserv_mod-entry">

Placeholder for mapping the front-end UI data.Data type: String

</td></tr><tr id="layout_mapping_body_icon-reserv_mod-row"><td>

result.layout\_mapping.body.icon

</td><td id="layout_mapping_body_icon-reserv_mod-entry">

Placeholder for mapping the front-end UI data.Data type: String

</td></tr><tr id="layout_mapping_body_label-reserv_mod-row"><td>

result.layout\_mapping.body.label

</td><td id="layout_mapping_body_label-reserv_mod-entry">

Placeholder for mapping the front-end UI data.Data type: String

</td></tr><tr id="layout_mapping_description-reserv_mod-row"><td>

result.layout\_mapping.description

</td><td id="layout_mapping_description-reserv_mod-entry">

Placeholder for mapping the front-end UI data. Description of the layout mapping.Data type: Array

</td></tr><tr id="layout_mapping_image-reserv_mod-row"><td>

result.layout\_mapping.image

</td><td id="layout_mapping_image-reserv_mod-entry">

Placeholder for mapping the front-end UI data.Data type: String

</td></tr><tr id="layout_mapping_subtitle-reserv_mod-row"><td>

result.layout\_mapping.subtitle

</td><td id="layout_mapping_subtitle-reserv_mod-entry">

Placeholder for mapping the front-end UI data.Data type: Array

</td></tr><tr id="layout_mapping_subtitle_asc-reserv_mod-row"><td>

result.layout\_mapping.subtitle\_asc

</td><td id="layout_mapping_subtitle_asc-reserv_mod-entry">

Placeholder for mapping the front-end UI data.Data type: Array

</td></tr><tr id="layout_mapping_title-reserv_mod-row"><td>

result.layout\_mapping.title

</td><td id="layout_mapping_title-reserv_mod-entry">

Placeholder for mapping the front-end UI data.Data type: Array

</td></tr><tr id="max_days_in_future-reserv_mod-row"><td>

result.max\_days\_in\_future

</td><td id="max_days_in_future-reserv_mod-entry">

Maximum number of the days in the future that a user can reserve the reservable module.Data type: Number

</td></tr><tr id="max_occurrences-reserv_mod-row"><td>

result.max\_occurrences

</td><td id="max_occurrences-reserv_mod-entry">

Maximum number of recurring reservation occurrences if recurring reservations are available for the reservable module.Data type: Number

</td></tr><tr id="name-reserv_mod-row"><td>

result.name

</td><td id="name-reserv_mod-entry">

Name of the reservable module.Data type: String

</td></tr><tr><td>

result.nbhBuildingIds

</td><td>

Only returned if the Space Management plugin is installed, the **browse\_by\_neighborhood\_enabled** parameter is set to `true`, and the **neighborhood** parameter is passed in the query parameters.List of sys\_ids of the buildings associated with the reservable module and configured for the neighborhood.

Data type: Array of Strings

</td></tr><tr><td>

result.nbhBuildingsData

</td><td>

Only returned if the Space Management plugin is installed, the **browse\_by\_neighborhood\_enabled** parameter is set to `true`, and the **neighborhood** parameter is passed in the query parameters.List of sys\_ids of the buildings associated with the reservable module and configured for the neighborhood. Each building element also contains a list of sys\_ids of the corresponding floors available for the building.

For example:

```
"nbhBuildingsData": {
  "4703a4cedb3650106c731dcd13961945": [
    "0f9e304edb7650106c731dcd13961911"
  ],
  "6c0364cedb3650106c731dcd13961927": [
    "b23328cedb3650106c731dcd139619f9"
  ]
}
```

Data type: Array of Objects

Table: Records associated with the building sys\_ids are located in the Building \[sn\_wsd\_core\_building\] table. Records associated with the floor sys\_ids are located in the Floor \[sn\_wsd\_core\_floor\] table.

</td></tr><tr><td>

result.nbhBuildingsTreeData

</td><td>

Only returned if the Space Management plugin is installed, the **browse\_by\_neighborhood\_enabled** parameter is set to `true`, and the **neighborhood** parameter is passed in the query parameters.Hierarchy of the buildings associate with the reservable module and neighborhood.

Data type: Array of Objects

```
"buildingsTreeData": [
  {
    "children": [Array],
    "data": {Object},
    "isSelectable": Boolean,
    "isValid": Boolean,
    "label": "String",
    "uId": "String"
  }
]
```

Hierarchy order:

-   Region: Located in the Region \[sn\_wsd\_core\_region\] table.
-   Site: Located in the Site \[sn\_wsd\_core\_site\] table.
-   Campus: Located in the Campus \[sn\_wsd\_core\_campus\] table.
-   Building: Located in the Building \[sn\_wsd\_core\_building\] table.

</td></tr><tr><td>

result.nbhBuildingsTreeData.children

</td><td>

Describes the hierarchy of the children associated with the building.Each `children[]` node reflects a different building level/hierarchy:

-   buildingsTreeData: Region
-   buildingsTreeData.children: Site
-   buildingsTreeData.children.children: Campus
-   buildingsTreeData.children.children.children: Building

Data type: Array of Objects

```
"children": [
  {
    "children": [Array],
    "data": {Object},
    "isSelectable": Boolean,
    "isValid": Boolean,
    "label": "String",
    "uId": "String"
  }
]
```

The parameters in the `children[]` array are the same as those in the **nbhBuildingsTreeData** object, just for the associated location type; region, site, campus, or building.

</td></tr><tr><td>

result.nbhBuildingsTreeData.data

</td><td>

Details about the associated entity; region, site, campus, or building.Data type: Object

```
"data": {
  "sys_id": "String",
  "table": "String",
  "timezone": {Object}
}
```

</td></tr><tr><td>

result.nbhBuildingsTreeData.data.sysId

</td><td>

Sys\_id of the associated entity record.Data type: String

</td></tr><tr><td>

result.nbhBuildingsTreeData.data.table

</td><td>

Table in which the associated record is located.Data type: String

</td></tr><tr><td>

result.nbhBuildingsTreeData.data.timezone

</td><td>

Information about the time zone in which the associated entity resides.Data type: Object

```
"timezone": {
  "displayValue": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.nbhBuildingsTreeData.data.timezone.displayValue

</td><td>

Time zone value to use in a user interface.Data type: String

</td></tr><tr><td>

result.nbhBuildingsTreeData.data.timezone.value

</td><td>

Internal time zone value.Data type: String

</td></tr><tr><td>

result.nbhBuildingsTreeData.isSelectable

</td><td>

Flag that indicates whether the associated entity is available \(selectable\) for the reservable model.Valid values:

-   true: Entity is available for the reservable module.
-   false: Entity isn't available for the reservable module.

Data type: Boolean

</td></tr><tr><td>

result.nbhBuildingsTreeData.isValid

</td><td>

Flag that indicates whether the associated entity is valid for the reservable model.Valid values:

-   true: Entity is valid for the reservable module.
-   false: Entity isn't valid for the reservable module.

Data type: Boolean

</td></tr><tr><td>

result.nbhBuildingsTreeData.label

</td><td>

Name of the reservable view.Data type: String

</td></tr><tr><td>

result.nbhBuildingsTreeData.uId

</td><td>

Sys\_id of the associated entity.Data type: String

</td></tr><tr id="override_approval_policy-reserv_mod-row"><td>

result.override\_approval\_policy

</td><td id="override_approval_policy-reserv_mod-entry">

Option to specify how to implement the approval policy. Choices:

-   No override: The approval policy is implemented as set in the **Requires approval** field of a workplace space or room.
-   Always require approval: The approval policy is required regardless of what is set in the **Requires approval** field of a workplace space or room.
-   Never require approval: The approval policy is removed regardless of what is set in the **Requires approval**l field of a workplace space or room.

Data type: String

</td></tr><tr id="require_cancel_notes-reserv_mod-row"><td>

result.require\_cancel\_notes

</td><td id="require_cancel_notes-reserv_mod-entry">

Flag that indicates whether users must enter a cancellation note before cancelling a reservable module.Valid values:

-   true: Cancellation note required.
-   false: Cancellation note not required.

Data type: Boolean

</td></tr><tr id="require_cc_dept_check-reserv_mod-row"><td>

result.require\_cc\_dept\_check

</td><td id="require_cc_dept_check-reserv_mod-entry">

Flag that indicates whether to check if there's a cost center or department mismatch between the workspace item and the logged in user. Valid values:

-   true: Check for a mismatch.
-   false: Don't check for a mismatch.

Data type: Boolean

</td></tr><tr id="require_subject-reserv_mod-row"><td>

result.require\_subject

</td><td id="require_subject-reserv_mod-entry">

Flag that indicates whether the user must enter a subject when making the reservation.Valid values:

-   true: Subject required.
-   false: Subject isn't required.

Data type: Boolean

</td></tr><tr id="reservable_columns-reserv_mod-row"><td>

result.reservable\_columns

</td><td id="reservable_columns-reserv_mod-entry">

List of the columns of a reservable.Data type: Array

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr id="reservable_container_field-reserv_mod-row"><td>

result.reservable\_container\_field

</td><td id="reservable_container_field-reserv_mod-entry">

Level of the container, such as a group of desks in a specific area.Data type: String

</td></tr><tr id="reservable_filter-reserv_mod-row"><td>

result.reservable\_filter

</td><td id="reservable_filter-reserv_mod-entry">

Filter conditions used to filter out reservable items in the associated Reservable table. Reservable table is a field in the Reservable Module \[sn\_wsd\_rsv\_reservable\_module\] table. These filter conditions were applied to the table contained in the field Reservable table.Data type: String

</td></tr><tr id="reservable_quantity_field-reserv_mod-row"><td>

result.reservable\_quantity\_field

</td><td id="reservable_quantity_field-reserv_mod-entry">

Reservable quantity of all the spaces. The quantity is used when assigning neighbourhood spaces to an area. For additional information, see [Assign neighborhood spaces to an area](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/add-neighbourhood-spaces-to-an-area.md).Data type: String

</td></tr><tr id="reservable_table-reserv_mod-row"><td>

result.reservable\_table

</td><td id="reservable_table-reserv_mod-entry">

Table that contains the reservable workplace items.Data type: String

</td></tr><tr id="reservable_type-reserv_mod-row"><td>

result.reservable\_type

</td><td id="reservable_type-reserv_mod-entry">

Type of the reservable item, such as location.Data type: String

</td></tr><tr id="reservable_views-reserv_mod-row"><td>

result.reservable\_views

</td><td id="reservable_views-reserv_mod-entry">

Details about the different views associated with the reservable module, such as card view or schedule view.Data type: Object

```
"reservable_views": {
  "iconClass": "String",
  "isDefault": Boolean,
  "label": "String",
  "order": Number,
  "type": "String"
}
```

Table: Reservable View \[sn\_wsd\_rsv\_reservable\_view\]

</td></tr><tr id="reservable_views_iconClass-reserv_mod-row"><td>

result.reservable\_views.iconClass

</td><td id="reservable_views_iconClass-reserv_mod-entry">

Icon class of the reservable view.Data type: String

</td></tr><tr id="reservable_views_isDefault-reserv_mod-row"><td>

result.reservable\_views.isDefault

</td><td id="reservable_views_isDefault-reserv_mod-entry">

Flag that indicates whether to make this reservable view the default for reservable modules. Valid values:

-   true: Make default.
-   false: Don't make default.

Data type: Boolean

</td></tr><tr id="reservable_views_label-reserv_mod-row"><td>

result.reservable\_views.label

</td><td id="reservable_views_label-reserv_mod-entry">

Name of the reservable view.Data type: String

</td></tr><tr id="reservable_views_order-reserv_mod-row"><td>

result.reservable\_views.order

</td><td id="reservable_views_order-reserv_mod-entry">

Order in which the views are displayed for the reservable module in the UI. The lower order number come first in the UI. In case of the same order number, it is assigned random ordering.Data type: Number

</td></tr><tr id="reservable_views_type-reserv_mod-row"><td>

result.reservable\_views.type

</td><td id="reservable_views_type-reserv_mod-entry">

Backend name of the reservable view. Used for internal processing.Data type: String

</td></tr><tr id="reservation_paths-reserv_mod-row"><td>

result.reservation\_paths

</td><td id="reservation_paths-reserv_mod-entry">

Reservation paths associated with the reservable modules such as Browse all, Browse near a person.Data type: Array of Objects

```
"reservation_paths": [
  {
    "displayValue": "String",
    "value": "String"
  }
]
```

</td></tr><tr id="reservation_paths_displayValue-reserv_mod-row"><td>

result.reservation\_paths.displayValue

</td><td id="reservation_paths_displayValue-reserv_mod-entry">

Display value for the reservation path, such as "Browse near a person".Data type: String

</td></tr><tr id="reservation_paths_value-reserv_mod-row"><td>

result.reservation\_paths.value

</td><td id="reservation_paths_value-reserv_mod-entry">

Internal value for the reservation path, such as "browse\_near\_a\_person".Data type: String

</td></tr><tr id="search_limit-reserv_mod-row"><td>

result.search\_limit

</td><td id="search_limit-reserv_mod-entry">

Maximum number of search results to return when a user searches for a workplace location.Data type: Number

</td></tr><tr id="selection_type-reserv_mod-row"><td>

result.selection\_type

</td><td id="selection_type-reserv_mod-entry">

Type of selection to display in the search results.

 Can be one of the following options:

-   Specific unit: The search result displays every workplace item.
-   Container: The search result displays the parent or container of the workplace items.

 Data type: String

</td></tr><tr id="short_description-reserv_mod-row"><td>

result.short\_description

</td><td id="short_description-reserv_mod-entry">

Brief description of the reservable module.Data type: String

</td></tr><tr id="show_map_view-reserv_mod-row"><td>

result.show\_map\_view

</td><td id="show_map_view-reserv_mod-entry">

Flag that indicates whether to enable the map view for reservable modules. Valid values:

-   true: Enable map view.
-   false: Don't enable map view.

Data type: Boolean

</td></tr><tr id="sys_id-reserv_mod-row"><td>

result.sys\_id

</td><td id="sys_id-reserv_mod-entry">

Sys\_id of the reservable module.Data type: String

</td></tr><tr id="timeSlots-reserv_mod-row"><td>

result.timeSlots

</td><td id="timeSlots-reserv_mod-entry">

Details about the time slots associated for a reservable module.Data type: Array of Objects

```
[
  {
    "name": "String",
    "short_description": "String",
    "slot_end": "String",
    "slot_start": "String",
    "sys_id": "String"
  }
]
```

</td></tr><tr id="timeSlots_name-reserv_mod-row"><td>

result.timeSlots.name

</td><td id="timeSlots_name-reserv_mod-entry">

Name of the time slot.Data type: String

</td></tr><tr id="timeSlots_short_description-reserv_mod-row"><td>

result.timeSlots.short\_description

</td><td id="timeSlots_short_description-reserv_mod-entry">

Brief description of the time slot.Data type: String

</td></tr><tr id="timeSlots_slot_end-reserv_mod-row"><td>

result.timeSlots.slot\_end

</td><td id="timeSlots_slot_end-reserv_mod-entry">

End time of the time slot.Data type: String

</td></tr><tr id="timeSlots_slot_start-reserv_mod-row"><td>

result.timeSlots.slot\_start

</td><td id="timeSlots_slot_start-reserv_mod-entry">

Start time of the slot.Data type: String

</td></tr><tr id="timeSlots_slot_sys_id-reserv_mod-row"><td>

result.timeSlots.sys\_id

</td><td id="timeSlots_slot_sys_id-reserv_mod-entry">

Sys\_id of the time slot record.Data type: String

Table: Time Slot \[sn\_wsd\_rsv\_time\_slot\]

</td></tr><tr id="title-reserv_mod-row"><td>

result.title

</td><td id="title-reserv_mod-entry">

Title of the reservable module.Data type: String

</td></tr><tr id="virtual_meeting_provider-reserv_mod-row"><td>

result.virtual\_meeting\_provider

</td><td id="virtual_meeting_provider-reserv_mod-entry">

Details about the virtual provider associated with the reservable module.Data type: Object

```
"virtual_meeting_provider": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="virtual_meeting_provider_display_value-reserv_mod-row"><td>

result.virtual\_meeting\_provider.display\_value

</td><td id="virtual_meeting_provider_display_value-reserv_mod-entry">

Display value of the virtual meeting provider.Data type: String

</td></tr><tr id="virtual_meeting_provider_sys_id-reserv_mod-row"><td>

result.virtual\_meeting\_provider.sys\_id

</td><td id="virtual_meeting_provider_sys_id-reserv_mod-entry">

Sys\_id of the virtual meeting provider.Data type: String

</td></tr></tbody>
</table>### cURL request

This code example shows how to request a reservable module with the buildings tree data.

```
curl "http://instance.servicenow.com/api/sn_wsd_rsv/reservable_module/5db44502dbb650106c731dcd13961937&is_buildings_tree_data_required=true" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Response body:

```
{
  "result": {
    "sys_id": "5db44502dbb650106c731dcd13961937", "name": "Desks",
    "title": "Desks",
    "inline_title": "desk",
    "font_awesome_icon": "fa-desktop",
    "reservable_table": "sn_wsd_core_space",
    "reservable_filter": "active=true^is_reservable=true^location_type=5f017383eb512010b89bfdfc9c5228c8^building.is_reservable=true^floor.is_reservable=true^EQ",
    "short_description": "Reserve a single desks",
    "reservable_type": "location",
    "require_subject": null,
    "require_cancel_notes": false,
    "virtual_meeting_provider": {
      "sys_id": "e33d9e6853c201103cf7ddeeff7b1205",
      "display_value": "Template"
    },
    "allow_invitees": null,
    "display_number_of_attendees": null,
    "display_on_behalf_of": null,
    "display_sensitivity": null,
    "max_days_in_future": "90",
    "allow_whole_day": "1",
    "selection_type": "unit",
    "reservable_container_field": null,
    "reservable_quantity_field": null,
    "apply_to_shift": null,
    "max_occurrences": "90",
    "enable_facet_filter": false,
    "search_limit": 10000,
    "enable_ical_generation": null,
    "enable_group_reservations": null,
    "enable_browse_near_a_person": "1",
    "enable_browse_by_area": "1",
    "enable_browse_by_neighborhood": "1",
    "show_map_view": false,
    "require_cc_dept_check": false,
    "display_value": "Desks",
    "browse_near_a_person_enabled": true,
    "browse_by_area_enabled": true,
    "browse_by_neighborhood_enabled": true,
    "reservable_columns": [
      "sys_id",
      "external_id",
      "email",
      "name",
      "title",
      "description",
      "image",
      "number",
      "site",
      "campus",
      "building",
      "floor",
      "area",
      "capacity",
      "reservable_quantity",
      "location_type",
      "order",
      "requires_check_in",
      "is_reservable"
    ],
    "layout_mapping": { 
      "title": [
        "name"
      ],
      "description": [ 
        "description"
      ],
      "subtitle": [
        "campus",
        "building",
        "floor",
        "area"
      ],
      "subtitle_asc": [
        "area",
        "floor",
        "building",
        "campus"
      ],
      "image": "image",
      "body": [
        {
          "label": "Capacity",
          "icon": "fa-users",
          "field": "capacity",
          "field_to_display": ""
        },
        {
          "label": "Standard services",
          "icon": "fa-check",
          "field": "standard_services",
          "field_to_display": "name"
        },
        {
          "label": "Reservable purposes",
          "icon": "fa-tags",
          "field": "reservable_purposes",
          "field_to_display": "name"
        }
      ]
    },
    "timeSlots": [
      {
        "sys_id": "d5331cf2dbb5f01038e42b24ca961906",
        "name": "All day",
        "short_description": "8am - 6pm",
        "slot_start": "08:00",
        "slot_end": "18:00"
      },
      {
        "sys_id": "de131cf2dbb5f01038e42b24ca961931",
        "name": "Before noon",
        "short_description": "8am - 12pm",
        "slot_start": "08:00",
        "slot_end": "12:00"
      },
      {
        "sys_id": "6e99ab5ddbb930102e8e853e68961929",
        "name": "After noon",
        "short_description": "1pm - 6pm",
        "slot_start": "13:00",
        "slot_end": "18:00"
      }
    ],
    "buildingSysIds": [
      "9e0364cedb3650106c731dcd1396192b"
    ],
    "buildingsTreeData": [
      {
        "isValid": true,
        "label": "Europe",
        "uId": "2d626c4edb3650106c731dcd1396194b",
        "isSelectable": false,
        "children": [
          {
            "isValid": true,
            "label": "Western Europe",
            "uId": "b17220cedb3650106c731dcd1396197a",
            "isSelectable": false,
            "children": [
              {
                "isValid": true,
                "label": "Amsterdam Campus",
                "uId": "44d2e0cedb3650106c731dcd13961988",
                "isSelectable": false,
                "children": [
                  {
                    "isValid": true,
                    "label": "AMS-B1",
                    "uId": "9e0364cedb3650106c731dcd1396192b",
                    "isSelectable": true,
                    "children": [],
                    "data": {
                      "sysId": "9e0364cedb3650106c731dcd1396192b",
                      "table": "sn_wsd_core_building",
                      "timezone": {
                        "value": "Europe/Amsterdam",
                        "displayValue": "Europe/Amsterdam"
                      }
                    }
                  }
                ],
                "data": {
                  "sysId": "44d2e0cedb3650106c731dcd13961988",
                  "table": "sn_wsd_core_campus",
                  "timezone": null
                }
              }
            ],
            "data": {
              "sysId": "b17220cedb3650106c731dcd1396197a",
              "table": "sn_wsd_core_site",
              "timezone": null
            }
          }
        ],
        "data": {
          "sysId": "2d626c4edb3650106c731dcd1396194b",
          "table": "sn_wsd_core_region",
          "timezone": null
        }
      }
    ],
    "reservable_views": [
      {
        "type": "card",
        "label": "Card view",
        "iconClass": "fa-th-large",
        "isDefault": true,
        "order": "1"
      },
      {
        "type": "schedule",
        "label": "Schedule view",
        "iconClass": "fa-calendar-o",
        "isDefault": false,
        "order": "2"
      }
    ],
    "checkin_before_minutes": 30,
    "reservation_paths": [
      {
        "value": "browse_all",
        "displayValue": "Browse all"
      },
      {
        "value": "browse_near_a_person",
        "displayValue": "Browse near a person"
      },
      {
        "value": "browse_by_area",
        "displayValue": "Browse by area"
      }
    ],
    "override_approval_policy": "never_required"
  }
}
```

