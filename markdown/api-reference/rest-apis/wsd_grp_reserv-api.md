---
title: WSD Group Reservation API
description: The Workplace Service Delivery \(WSD\) Group Reservation API provides endpoints for managing group reservations.Returns the parent and all child reservations for a specified group reservation.Cancels a specified group reservation.Updates a specified group reservation.Creates a group reservation.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 28
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# WSD Group Reservation API

The Workplace Service Delivery \(WSD\) Group Reservation API provides endpoints for managing group reservations.

Group reservations allow you to reserve different locations for various people \(groups\) for the same meeting.

This API runs in the `sn_wsd_rsv` namespace. To access this API, the caller must have the sn\_wsd\_core.workplace\_user role and the Workplace Reservation Management \(sn\_wsd\_rsv\) plugin must be activated.

For additional information on Workplace Reservation Management, see Workplace Reservation Management.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## WSD Group Reservation - GET /api/sn\_wsd\_rsv/group\_reservation/\{parent\_id\}

Returns the parent and all child reservations for a specified group reservation.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/group_reservation/{parent_id}`

Default URL: `/api/sn_wsd_rsv/group_reservation/{parent_id}`

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

parent\_id

</td><td>

Sys\_id of the parent reservation record.

When a group reservation is created, one group parent record and one or more child reservation records are created. Reservation records contain a field called reservation\_subtype, that indicates the type of reservation record. For group parent records, this field is set to "Group parent" to indicate that it is a group parent record. For child records, this field is set to "Single".

Within a child record, the sys\_id of the associated parent reservation record is in the source\_reservation field.

Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

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

</td><td id="accept-reserv-entry">

Data format of the request body. Supported types: **application/json**, **application/xml** or, **text/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. Invalid or no parent reservation sys\_id provided.|
|404|Access denied. Unable to cancel group reservation. User has insufficient rights to cancel the requested group reservation.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Details about the parent and children reservations associated with the group reservation.Data type: Object

```
{
  "result": {
    "parent": {Object},
    "children": [Array]
}
```

</td></tr></tbody>
</table>### cURL request

The following code example shows how to retrieve the details for a group reservation.

```
curl "http://instance.servicenow.com/api/sn_wsd_rsv/group_reservation/e2245051533b01103cf7ddeeff7b12d6" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "parent": {
      "sys_id": "e2245051533b01103cf7ddeeff7b12d6",
      "number": "WRES0001142",
      "start": "2022-05-30T04:30:00Z",
      "end": "2022-05-30T05:30:00Z",
      "sys_created_on": "2022-05-30T04:19:02Z",
      "sys_updated_on": "2022-05-30T04:19:04Z",
      "source_reservation": null,
      "check_in_state": {
        "value": "not_required",
        "display_value": "Not required"
      },
      "external_id": null,
      "external_ical": null,
      "active": true,
      "state": {
        "value": "confirmed",
        "display_value": "Confirmed"
      },
      "sensitivity": {
        "value": "normal",
        "display_value": "Normal"
      },
      "reservation_type": {
        "value": "space",
        "display_value": "Space"
      },
      "reservation_subtype": {
        "value": "group_parent",
        "display_value": "Group parent"
      },
      "reservation_purpose": {
        "value": "meeting",
        "display_value": "Meeting"
      },
      "attendees": null,
      "number_of_attendees": 1,
      "is_parent": true,
      "subject": "Test#52",
      "virtual_meeting": null,
      "recording_details": [],
      "sync_state": {
        "value": "not_required",
        "display_value": "Synchronization not required"
      },
      "sub_source": {
        "value": "servicenow_workplace_service_delivery",
        "display_value": "ServiceNow Workplace Service Delivery"
      },
      "last_updated_sub_source": {
        "value": "servicenow_workplace_service_delivery",
        "display_value": "ServiceNow Workplace Service Delivery"
      },
      "reservable_module": {
        "sys_id": "5db44502dbb650106c731dcd13961937",
        "name": "Desks",
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
        "display_on_behalf_of": "1",
        "display_sensitivity": null,
        "max_days_in_future": "90",
        "allow_whole_day": "1",
        "require_whole_day": null,
        "selection_type": "unit",
        "reservable_container_field": null,
        "reservable_quantity_field": null,
        "apply_to_shift": null,
        "max_occurrences": "90",
        "enable_facet_filter": false,
        "search_limit": 10000,
        "enable_ical_generation": null,
        "enable_group_reservations": "1",
        "enable_browse_near_a_person": "1",
        "enable_browse_by_area": "1",
        "display_value": "Desks",
        "browse_near_a_person_enabled": true,
        "browse_by_area_enabled": true,
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
      },
      "notification_recipients": null,
      "notification_custom_message": null,
      "opened_by": {
        "sys_id": "6816f79cc0a8016401c5a33be04be441",
        "value": "6816f79cc0a8016401c5a33be04be441",
        "displayValue": "System Administrator",
        "display_value": "System Administrator",
        "name": "System Administrator",
        "user_name": "admin",
        "table": "sys_user",
        "avatar": "c148e1d13741310042106710ce41f149.iix?t=small",
        "initials": "SA",
        "email": "admin@example.com",
        "label": "System Administrator, Finance"
      },
      "requested_for": {
        "sys_id": "6816f79cc0a8016401c5a33be04be441",
        "value": "6816f79cc0a8016401c5a33be04be441",
        "displayValue": "System Administrator",
        "display_value": "System Administrator",
        "name": "System Administrator",
        "user_name": "admin",
        "table": "sys_user",
        "avatar": "c148e1d13741310042106710ce41f149.iix?t=small",
        "initials": "SA",
        "email": "admin@example.com",
        "label": "System Administrator, Finance"
      },
      "edit_restriction": {
        "value": "no_restriction",
        "display_value": "No restriction"
      },
      "source": {
        "value": "servicenow",
        "display_value": "Workplace Services"
      },
      "source_icon": {
        "classNames": "fa fa-calendar-check-o",
        "tooltip": "Reservation is confirmed",
        "imgSrc": ""
      },
      "shift": null,
      "locations": [
        {
          "sys_id": "73c2698adb7210106c731dcd13961968",
          "name": "B1-03-03",
          "description": "Desk reserved for the Team-C. After 10am, free to reserve for everyone.",
          "display_value": "B1-03-03",
          "capacity": 1,
          "label_value": "Workspace/Desk name",
          "email": null,
          "reservable_module": {
            "sys_id": "5db44502dbb650106c731dcd13961937",
            "name": "Desks",
            "title": "Desks",
            "inline_title": "desk"
          },
          "region": {
            "sys_id": "2d626c4edb3650106c731dcd1396194b",
            "display_value": "Europe",
            "active": true
          },
          "site": {
            "sys_id": "b17220cedb3650106c731dcd1396197a",
            "display_value": "Western Europe",
            "active": true
          },
          "campus": {
            "sys_id": "44d2e0cedb3650106c731dcd13961988",
            "display_value": "Amsterdam Campus",
            "active": true
          },
          "building": {
            "sys_id": "9e0364cedb3650106c731dcd1396192b",
            "display_value": "AMS-B1",
            "active": true,
            "timezone": {
              "value": "Europe/Amsterdam",
              "displayValue": "Europe/Amsterdam"
            }
          },
          "floor": {
            "sys_id": "5373a8cedb3650106c731dcd1396198a",
            "display_value": "Floor 3",
            "active": true
          },
          "area": {
            "sys_id": "410ff04edb7650106c731dcd13961973",
            "display_value": "Desks C1",
            "active": true
          },
          "reservation": {
            "sys_id": "2a24d0d1533b01103cf7ddeeff7b126b",
            "number_of_attendees": 1,
            "state": {
              "value": "confirmed",
              "display_value": "Confirmed"
            },
            "requested_for": {
              "sys_id": "62826bf03710200044e0bfc8bcbe5df1",
              "value": "62826bf03710200044e0bfc8bcbe5df1",
              "displayValue": "Abel Tuter",
              "display_value": "Abel Tuter",
              "name": "Abel Tuter",
              "user_name": "abel.tuter",
              "table": "sys_user",
              "avatar": "063e38383730310042106710ce41f13b.iix?t=small",
              "initials": "AT",
              "email": "abel.tuter@example.com",
              "label": "Product Management"
            },
            "number": "WRES0001143",
            "active": true
          },
          "number_of_attendees": 1,
          "state": {
            "value": "confirmed",
            "display_value": "Confirmed"
          },
          "number": "WRES0001143",
          "requested_for": {
            "sys_id": "62826bf03710200044e0bfc8bcbe5df1",
            "value": "62826bf03710200044e0bfc8bcbe5df1",
            "displayValue": "Abel Tuter",
            "display_value": "Abel Tuter",
            "name": "Abel Tuter",
            "user_name": "abel.tuter",
            "table": "sys_user",
            "avatar": "063e38383730310042106710ce41f13b.iix?t=small",
            "initials": "AT",
            "email": "abel.tuter@example.com",
            "label": "Product Management"
          }
        },
        {
          "sys_id": "32f2a98adb7210106c731dcd13961972",
          "name": "B1-03-04",
          "description": "Desk reserved for the Team-C. After 10am, free to reserve for everyone.",
          "display_value": "B1-03-04",
          "capacity": 1,
          "label_value": "Workspace/Desk name",
          "email": null,
          "reservable_module": {
            "sys_id": "5db44502dbb650106c731dcd13961937",
            "name": "Desks",
            "title": "Desks",
            "inline_title": "desk"
          },
          "region": {
            "sys_id": "2d626c4edb3650106c731dcd1396194b",
            "display_value": "Europe",
            "active": true
          },
          "site": {
            "sys_id": "b17220cedb3650106c731dcd1396197a",
            "display_value": "Western Europe",
            "active": true
          },
          "campus": {
            "sys_id": "44d2e0cedb3650106c731dcd13961988",
            "display_value": "Amsterdam Campus",
            "active": true
          },
          "building": {
            "sys_id": "9e0364cedb3650106c731dcd1396192b",
            "display_value": "AMS-B1",
            "active": true,
            "timezone": {
              "value": "Europe/Amsterdam",
              "displayValue": "Europe/Amsterdam"
            }
          },
          "floor": {
            "sys_id": "5373a8cedb3650106c731dcd1396198a",
            "display_value": "Floor 3",
            "active": true
          },
          "area": {
            "sys_id": "410ff04edb7650106c731dcd13961973",
            "display_value": "Desks C1",
            "active": true
          },
          "reservation": {
            "sys_id": "6a24d0d1533b01103cf7ddeeff7b126e",
            "number_of_attendees": 1,
            "state": {
              "value": "confirmed",
              "display_value": "Confirmed"
            },
            "requested_for": {
              "sys_id": "a8f98bb0eb32010045e1a5115206fe3a",
              "value": "a8f98bb0eb32010045e1a5115206fe3a",
              "displayValue": "Abraham Lincoln",
              "display_value": "Abraham Lincoln",
              "name": "Abraham Lincoln",
              "user_name": "abraham.lincoln",
              "table": "sys_user",
              "avatar": null,
              "initials": "AL",
              "email": "abraham.lincoln@example.com",
              "label": ""
            },
            "number": "WRES0001144",
            "active": true
          },
          "number_of_attendees": 1,
          "state": {
            "value": "confirmed",
            "display_value": "Confirmed"
          },
          "number": "WRES0001144",
          "requested_for": {
            "sys_id": "a8f98bb0eb32010045e1a5115206fe3a",
            "value": "a8f98bb0eb32010045e1a5115206fe3a",
            "displayValue": "Abraham Lincoln",
            "display_value": "Abraham Lincoln",
            "name": "Abraham Lincoln",
            "user_name": "abraham.lincoln",
            "table": "sys_user",
            "avatar": null,
            "initials": "AL",
            "email": "abraham.lincoln@example.com",
            "label": ""
          }
        }
      ],
      "reservationAcl": {
        "write": {
          "record": true,
          "fields": {
            "subject": true,
            "sensitivity": true,
            "requested_for": true,
            "number_of_attendees": true,
            "location": true
          },
          "allFields": true
        },
        "read": true
      }
    },
    "children": [
      {
        "sys_id": "2a24d0d1533b01103cf7ddeeff7b126b",
        "number": "WRES0001143",
        "location": {
          "sys_id": "73c2698adb7210106c731dcd13961968",
          "name": "B1-03-03",
          "description": "Desk reserved for the Team-C. After 10am, free to reserve for everyone.",
          "display_value": "B1-03-03",
          "capacity": 1,
          "label_value": "Workspace/Desk name",
          "email": null,
          "reservable_module": {
            "sys_id": "5db44502dbb650106c731dcd13961937",
            "name": "Desks",
            "title": "Desks",
            "inline_title": "desk"
          },
          "region": {
            "sys_id": "2d626c4edb3650106c731dcd1396194b",
            "display_value": "Europe",
            "active": true
          },
          "site": {
            "sys_id": "b17220cedb3650106c731dcd1396197a",
            "display_value": "Western Europe",
            "active": true
          },
          "campus": {
            "sys_id": "44d2e0cedb3650106c731dcd13961988",
            "display_value": "Amsterdam Campus",
            "active": true
          },
          "building": {
            "sys_id": "9e0364cedb3650106c731dcd1396192b",
            "display_value": "AMS-B1",
            "active": true,
            "timezone": {
              "value": "Europe/Amsterdam",
              "displayValue": "Europe/Amsterdam"
            }
          },
          "floor": {
            "sys_id": "5373a8cedb3650106c731dcd1396198a",
            "display_value": "Floor 3",
            "active": true
          },
          "area": {
            "sys_id": "410ff04edb7650106c731dcd13961973",
            "display_value": "Desks C1",
            "active": true
          },
          "reservation": {
            "sys_id": "2a24d0d1533b01103cf7ddeeff7b126b",
            "number_of_attendees": 1,
            "state": {
              "value": "confirmed",
              "display_value": "Confirmed"
            },
            "requested_for": {
              "sys_id": "62826bf03710200044e0bfc8bcbe5df1",
              "name": "Abel Tuter",
              "user_name": "abel.tuter"
            },
            "number": "WRES0001143",
            "active": true
          },
          "number_of_attendees": 1,
          "state": {
            "value": "confirmed",
            "display_value": "Confirmed"
          },
          "number": "WRES0001143",
          "requested_for": {
            "sys_id": "62826bf03710200044e0bfc8bcbe5df1",
            "name": "Abel Tuter",
            "user_name": "abel.tuter"
          }
        },
        "start": "2022-05-30T04:30:00Z",
        "end": "2022-05-30T05:30:00Z",
        "sys_created_on": "2022-05-30T04:19:02Z",
        "sys_updated_on": "2022-05-30T04:19:04Z",
        "source_reservation": {
          "sys_id": "e2245051533b01103cf7ddeeff7b12d6",
          "display_value": "WRES0001142",
          "name": "WRES0001142"
        },
        "check_in_state": {
          "value": "awaiting_check_in",
          "display_value": "Awaiting check-in"
        },
        "external_id": null,
        "external_ical": null,
        "active": true,
        "state": {
          "value": "confirmed",
          "display_value": "Confirmed"
        },
        "sensitivity": {
          "value": "normal",
          "display_value": "Normal"
        },
        "reservation_type": {
          "value": "space",
          "display_value": "Space"
        },
        "reservation_subtype": {
          "value": "single",
          "display_value": "Single"
        },
        "reservation_purpose": {
          "value": "meeting",
          "display_value": "Meeting"
        },
        "attendees": null,
        "number_of_attendees": 1,
        "is_parent": false,
        "subject": "Test#52",
        "virtual_meeting": null,
        "recording_details": [],
        "sync_state": {
          "value": "not_required",
          "display_value": "Synchronization not required"
        },
        "sub_source": {
          "value": "servicenow_workplace_service_delivery",
          "display_value": "ServiceNow Workplace Service Delivery"
        },
        "last_updated_sub_source": {
          "value": "servicenow_workplace_service_delivery",
          "display_value": "ServiceNow Workplace Service Delivery"
        },
        "reservable_module": {
          "sys_id": "5db44502dbb650106c731dcd13961937",
          "name": "Desks",
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
          "display_on_behalf_of": "1",
          "display_sensitivity": null,
          "max_days_in_future": "90",
          "allow_whole_day": "1",
          "require_whole_day": null,
          "selection_type": "unit",
          "reservable_container_field": null,
          "reservable_quantity_field": null,
          "apply_to_shift": null,
          "max_occurrences": "90",
          "enable_facet_filter": false,
          "search_limit": 10000,
          "enable_ical_generation": null,
          "enable_group_reservations": "1",
          "enable_browse_near_a_person": "1",
          "enable_browse_by_area": "1",
          "display_value": "Desks",
          "browse_near_a_person_enabled": true,
          "browse_by_area_enabled": true,
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
        },
        "notification_recipients": null,
        "notification_custom_message": null,
        "opened_by": {
          "sys_id": "6816f79cc0a8016401c5a33be04be441",
          "value": "6816f79cc0a8016401c5a33be04be441",
          "displayValue": "System Administrator",
          "display_value": "System Administrator",
          "name": "System Administrator",
          "user_name": "admin",
          "table": "sys_user",
          "avatar": "c148e1d13741310042106710ce41f149.iix?t=small",
          "initials": "SA",
          "email": "admin@example.com",
          "label": "System Administrator, Finance"
        },
        "requested_for": {
          "sys_id": "62826bf03710200044e0bfc8bcbe5df1",
          "value": "62826bf03710200044e0bfc8bcbe5df1",
          "displayValue": "Abel Tuter",
          "display_value": "Abel Tuter",
          "name": "Abel Tuter",
          "user_name": "abel.tuter",
          "table": "sys_user",
          "avatar": "063e38383730310042106710ce41f13b.iix?t=small",
          "initials": "AT",
          "email": "abel.tuter@example.com",
          "label": "Product Management"
        },
        "edit_restriction": {
          "value": "fully_restricted",
          "display_value": "Fully restricted"
        },
        "source": {
          "value": "servicenow",
          "display_value": "Workplace Services"
        },
        "source_reservation_requester": {
          "sys_id": "6816f79cc0a8016401c5a33be04be441",
          "name": "System Administrator",
          "user_name": "admin"
        },
        "source_icon": {
          "classNames": "fa fa-calendar-check-o",
          "tooltip": "Reservation is confirmed",
          "imgSrc": ""
        },
        "shift": null,
        "reservationAcl": {
          "write": {
            "record": true,
            "fields": {
              "subject": true,
              "sensitivity": true,
              "requested_for": true,
              "number_of_attendees": true,
              "location": true
            },
            "allFields": true
          },
          "read": true
        }
      },
      {
        "sys_id": "6a24d0d1533b01103cf7ddeeff7b126e",
        "number": "WRES0001144",
        "location": {
          "sys_id": "32f2a98adb7210106c731dcd13961972",
          "name": "B1-03-04",
          "description": "Desk reserved for the Team-C. After 10am, free to reserve for everyone.",
          "display_value": "B1-03-04",
          "capacity": 1,
          "label_value": "Workspace/Desk name",
          "email": null,
          "reservable_module": {
            "sys_id": "5db44502dbb650106c731dcd13961937",
            "name": "Desks",
            "title": "Desks",
            "inline_title": "desk"
          },
          "region": {
            "sys_id": "2d626c4edb3650106c731dcd1396194b",
            "display_value": "Europe",
            "active": true
          },
          "site": {
            "sys_id": "b17220cedb3650106c731dcd1396197a",
            "display_value": "Western Europe",
            "active": true
          },
          "campus": {
            "sys_id": "44d2e0cedb3650106c731dcd13961988",
            "display_value": "Amsterdam Campus",
            "active": true
          },
          "building": {
            "sys_id": "9e0364cedb3650106c731dcd1396192b",
            "display_value": "AMS-B1",
            "active": true,
            "timezone": {
              "value": "Europe/Amsterdam",
              "displayValue": "Europe/Amsterdam"
            }
          },
          "floor": {
            "sys_id": "5373a8cedb3650106c731dcd1396198a",
            "display_value": "Floor 3",
            "active": true
          },
          "area": {
            "sys_id": "410ff04edb7650106c731dcd13961973",
            "display_value": "Desks C1",
            "active": true
          },
          "reservation": {
            "sys_id": "6a24d0d1533b01103cf7ddeeff7b126e",
            "number_of_attendees": 1,
            "state": {
              "value": "confirmed",
              "display_value": "Confirmed"
            },
            "requested_for": {
              "sys_id": "a8f98bb0eb32010045e1a5115206fe3a",
              "name": "Abraham Lincoln",
              "user_name": "abraham.lincoln"
            },
            "number": "WRES0001144",
            "active": true
          },
          "number_of_attendees": 1,
          "state": {
            "value": "confirmed",
            "display_value": "Confirmed"
          },
          "number": "WRES0001144",
          "requested_for": {
            "sys_id": "a8f98bb0eb32010045e1a5115206fe3a",
            "name": "Abraham Lincoln",
            "user_name": "abraham.lincoln"
          }
        },
        "start": "2022-05-30T04:30:00Z",
        "end": "2022-05-30T05:30:00Z",
        "sys_created_on": "2022-05-30T04:19:02Z",
        "sys_updated_on": "2022-05-30T04:19:04Z",
        "source_reservation": {
          "sys_id": "e2245051533b01103cf7ddeeff7b12d6",
          "display_value": "WRES0001142",
          "name": "WRES0001142"
        },
        "check_in_state": {
          "value": "awaiting_check_in",
          "display_value": "Awaiting check-in"
        },
        "external_id": null,
        "external_ical": null,
        "active": true,
        "state": {
          "value": "confirmed",
          "display_value": "Confirmed"
        },
        "sensitivity": {
          "value": "normal",
          "display_value": "Normal"
        },
        "reservation_type": {
          "value": "space",
          "display_value": "Space"
        },
        "reservation_subtype": {
          "value": "single",
          "display_value": "Single"
        },
        "reservation_purpose": {
          "value": "meeting",
          "display_value": "Meeting"
        },
        "attendees": null,
        "number_of_attendees": 1,
        "is_parent": false,
        "subject": "Test#52",
        "virtual_meeting": null,
        "recording_details": [],
        "sync_state": {
          "value": "not_required",
          "display_value": "Synchronization not required"
        },
        "sub_source": {
          "value": "servicenow_workplace_service_delivery",
          "display_value": "ServiceNow Workplace Service Delivery"
        },
        "last_updated_sub_source": {
          "value": "servicenow_workplace_service_delivery",
          "display_value": "ServiceNow Workplace Service Delivery"
        },
        "reservable_module": {
          "sys_id": "5db44502dbb650106c731dcd13961937",
          "name": "Desks",
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
          "display_on_behalf_of": "1",
          "display_sensitivity": null,
          "max_days_in_future": "90",
          "allow_whole_day": "1",
          "require_whole_day": null,
          "selection_type": "unit",
          "reservable_container_field": null,
          "reservable_quantity_field": null,
          "apply_to_shift": null,
          "max_occurrences": "90",
          "enable_facet_filter": false,
          "search_limit": 10000,
          "enable_ical_generation": null,
          "enable_group_reservations": "1",
          "enable_browse_near_a_person": "1",
          "enable_browse_by_area": "1",
          "display_value": "Desks",
          "browse_near_a_person_enabled": true,
          "browse_by_area_enabled": true,
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
        },
        "notification_recipients": null,
        "notification_custom_message": null,
        "opened_by": {
          "sys_id": "6816f79cc0a8016401c5a33be04be441",
          "value": "6816f79cc0a8016401c5a33be04be441",
          "displayValue": "System Administrator",
          "display_value": "System Administrator",
          "name": "System Administrator",
          "user_name": "admin",
          "table": "sys_user",
          "avatar": "c148e1d13741310042106710ce41f149.iix?t=small",
          "initials": "SA",
          "email": "admin@example.com",
          "label": "System Administrator, Finance"
        },
        "requested_for": {
          "sys_id": "a8f98bb0eb32010045e1a5115206fe3a",
          "value": "a8f98bb0eb32010045e1a5115206fe3a",
          "displayValue": "Abraham Lincoln",
          "display_value": "Abraham Lincoln",
          "name": "Abraham Lincoln",
          "user_name": "abraham.lincoln",
          "table": "sys_user",
          "avatar": null,
          "initials": "AL",
          "email": "abraham.lincoln@example.com",
          "label": ""
        },
        "edit_restriction": {
          "value": "fully_restricted",
          "display_value": "Fully restricted"
        },
        "source": {
          "value": "servicenow",
          "display_value": "Workplace Services"
        },
        "source_reservation_requester": {
          "sys_id": "6816f79cc0a8016401c5a33be04be441",
          "name": "System Administrator",
          "user_name": "admin"
        },
        "source_icon": {
          "classNames": "fa fa-calendar-check-o",
          "tooltip": "Reservation is confirmed",
          "imgSrc": ""
        },
        "shift": null,
        "reservationAcl": {
          "write": {
            "record": true,
            "fields": {
              "subject": true,
              "sensitivity": true,
              "requested_for": true,
              "number_of_attendees": true,
              "location": true
            },
            "allFields": true
          },
          "read": true
        }
      }
    ]
  }
}

```

## WSD Group Reservation - PATCH /api/sn\_wsd\_rsv/group\_reservation/cancel/\{id\}

Cancels a specified group reservation.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/group_reservation/cancel/{id}`

Default URL: `/api/sn_wsd_rsv/group_reservation/cancel/{id}`

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

Sys\_id of the parent reservation record.

When a group reservation is created, one group parent record and one or more child reservation records are created. Reservation records contain a field called reservation\_subtype, that indicates the type of reservation record. For group parent records, this field is set to "Group parent" to indicate that it is a group parent record. For child records, this field is set to "Single".

Within a child record, the sys\_id of the associated parent reservation record is in the source\_reservation field.

Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cancel\_notes

</td><td>

Reason for cancelling the reservation.Data type: String

 Default: "Canceled reservation via Group cancel"

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-reserv-entry">

Data format of the request body. Supported types: **application/json**, **application/xml** or, **text/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="content_type-JSON-only-entry-RESTAPI">

Data format of the request body. Only supports **application/json**.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. Invalid or no parent reservation sys\_id provided.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Access denied. Unable to cancel group reservation. User has insufficient rights to cancel the requested group reservation.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Results of the group reservation cancel request.Data type: Object

 ```
"result": {
  "allChildrenCanceled": Boolean,
  "cancelledParent": Boolean,
  "canceledReservations": [Array],
  "failedChildMeetings": [Array],
  "msg": "String",
  "parent": "String",
  "success": Boolean,
  "user_msg": "String"
}
```

</td></tr><tr><td>

result.allChildrenCanceled

</td><td>

Flag that indicates whether all child reservations associated with the group reservation were successfully cancelled.Possible values:

-   true: Successfully cancelled.
-   false: Not all child reservations were cancelled. The **failedChildMeetings** parameter contains a list of the sys\_ids of the child reservations that were not cancelled.

 Data type: Boolean

</td></tr><tr><td>

result.cancelledParent

</td><td>

Flag that indicates whether the parent reservation for the group reservation were successfully cancelled.Possible values:

-   true: Parent reservation was cancelled.
-   false: Parent reservation was not cancelled.

 Data type: Boolean

</td></tr><tr><td>

result.canceledReservations

</td><td>

List of sys\_ids of the child reservations that were successfully canceled.Data type: Array

</td></tr><tr><td>

result.failedChildMeetings

</td><td>

List of sys\_ids of the child reservations that were not canceled.Data type: Array

</td></tr><tr><td>

result.msg

</td><td>

If any reservation failed to cancel, this parameter contains a message about the cause of failure.Data type: String

</td></tr><tr><td>

result.parent

</td><td>

Sys\_id of the parent reservation that was cancelled.Data type: String

</td></tr><tr><td>

result.success

</td><td>

Flag that indicates whether the group reservation was successfully cancelled.Possible values:

-   true: Group reservation was successfully cancelled.
-   false: One or more of the associated group reservations were not cancelled. Additional details are provided within the results.

 Data type: Boolean

</td></tr><tr><td>

result.user\_msg

</td><td>

Reserved for future use. If any reservation failed to cancel, this parameter contains a translated message about the cause of failure that you can display in the UI.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to cancel a group reservation.

```
curl "http://instance.servicenow.com/api/sn_wsd_rsv/group_reservation/cancel/22c1aee353af01103cf7ddeeff7b12d5" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
    \"cancel_notes\":\"Need to postpone until next quarter\"
}" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "success": true,
    "canceledReservations": [
      "6ec1aee353af01103cf7ddeeff7b12d8",
      "aac1aee353af01103cf7ddeeff7b12db"
    ],
    "failedChildMeetings": [],
    "cancelledParent": true,
    "allChildrenCanceled": true,
    "msg": "",
    "user_msg": "",
    "parent": "22c1aee353af01103cf7ddeeff7b12d5"
  }
}
```

## WSD Group Reservation - PATCH /api/sn\_wsd\_rsv/group\_reservation/update/\{id\}

Updates a specified group reservation.

You can update the following reservation parameters:

-   Subject
-   Start date and time
-   End date and time
-   Shift associated with the reservation
-   Workplace location of any child reservation

**Note:** You must specify at least one of these parameters in the request body of the endpoint call. Parameters that are not passed in are not modified in the associated records.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/group_reservation/update/{id}`

Default URL: `/api/sn_wsd_rsv/group_reservation/update/{id}`

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

Sys\_id of the parent reservation record.

When a group reservation is created, one group parent record and one or more child reservation records are created. Reservation records contain a field called reservation\_subtype, that indicates the type of reservation record. For group parent records, this field is set to "Group parent" to indicate that it is a group parent record. For child records, this field is set to "Single".

Within a child record, the sys\_id of the associated parent reservation record is in the source\_reservation field.

Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

children

</td><td>

Updated list of child reservations records to associate with the reservation.Data type: Array of Objects

 ```
"children": [
  {
    "is_private": Boolean,
    "location": "String",
    "requested_for": "String"
  }
]
```

</td></tr><tr><td>

children.is\_private

</td><td>

Flag that indicates whether the reservation is private. If private, the reservation doesn't appear to anyone except the owner.For additional information on these privacy settings, see Location privacy settings and impact.

Valid values:

-   true: Reservation is private.
-   false: Reservation isn't private.

Data type: Boolean

Default: Value set for privacy in the system properties.

</td></tr><tr><td>

children.location

</td><td>

Updated sys\_id of the location to reserve.Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

children.requested\_for

</td><td>

Updated sys\_id of the user for whom the reservation is being requested.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

end

</td><td>

Updated end time of the reservation.Data type: String

Format: UTC or local time \(yyyy-mm-dd hh:mm:ss\)

</td></tr><tr><td>

requested\_for

</td><td id="requested_for-update_reserv-entry">

Sys\_id or email address of the user for which the reservation is being made.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

reservable\_module

</td><td id="reservable_module-update_reserv-entry">

Required. Sys\_id of the reservable module to associate with the reservation. A reservable module defines the workplace items needed for a reservation.Data type: String

Table: Reservable Module \[sn\_wsd\_rsv\_reservable\_module\]

</td></tr><tr><td>

shift

</td><td id="shift-update_reserv-entry">

Updated sys\_id of the shift to associate with the reservation.For additional information on shift-based reservations, see Enable shift-based reservation.

Data type: String

Table: Shift \[sn\_wsd\_core\_shift\]

</td></tr><tr><td>

start

</td><td id="start-update_reserv-entry">

Updated start time of the reservation.Data type: String

Format: UTC or local time \(yyyy-mm-dd hh:mm:ss\)

Default: Empty - start time is specified in child reservations

</td></tr><tr><td>

subject

</td><td id="subject-update_reserv-entry">

Updated subject of the meeting associated with the reservation.Data type: String

Default: Empty

</td></tr><tr><td>

workplace\_location

</td><td>

Updated sys\_id of the workplace location to associate with the group reservation.Data type: String

Default: Empty - locations are specified in child reservations

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-reserv-entry">

Data format of the request body. Supported types: **application/json**, **application/xml** or, **text/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="content_type-JSON-only-entry-RESTAPI">

Data format of the request body. Only supports **application/json**.

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
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td id="result-multi-entry">

Return results from the multi-reservation creation or update.Data type: Object

```
"result": {
  "parent": "String",
  "success": Boolean,
  "successfulReservations": [Array],
  "unSuccessfulReservations": [Array]
}
```

</td></tr><tr><td>

result.parent

</td><td id="parent-multi-entry">

Sys\_id of the parent reservation that was updated.Data type: String

</td></tr><tr><td>

result.success

</td><td id="success-multi-entry">

Flag that indicates whether the reservation was successfully created.Possible values:

-   true: Successfully created.
-   false: Operation failed.

Data type: Boolean

</td></tr><tr><td>

result.successfulReservations

</td><td>

List of the reservations that were successfully updated.Data type: Array of Objects

```
"successfulReservations": [
  {
    "msg": "String",
    "operation": "String"
    "sys_id": "String",
    "user_msg": "String"
  }
]
```

</td></tr><tr><td>

result.successfulReservations.msg

</td><td>

Internal message about the update. Provides technical information about the operation.Data type: String

</td></tr><tr><td>

result.successfulReservations.operation

</td><td id="successfulReservations_reservable-multi-entry">

Type of operation that was performed, such as create or update. If a new reservable is added to the group reservation, such as an added room, this value is returned as `create`, otherwise it is set to `update`.Data type: String

</td></tr><tr><td>

result.successfulReservations.sys\_id

</td><td id="successfulReservations_sys_id-multi-entry">

Sys\_id of the reservation that was created.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr><td>

result.successfulReservations.user\_msg

</td><td>

User message about the update. This message may be translated based on the user's language preference and should be the one that appears in the UI.Data type: String

</td></tr><tr><td>

result.unSuccessfulReservations

</td><td>

List of the reservations that were unsuccessfully updated.Data type: Array of Objects

```
"unSuccessfulReservations": [
  {
    "msg": "String",
    "operation": "String"
    "sys_id": "String",
    "user_msg": "String"
  }
]
```

</td></tr><tr><td>

result.unSuccessfulReservations.msg

</td><td>

Message about the update error.Data type: String

</td></tr><tr><td>

result.unSuccessfulReservations.operation

</td><td>

Type of operation that was performed, such as create or update.Data type: String

</td></tr><tr id="successfulReservations_sys_id-multi-row"><td>

result.unSuccessfulReservations.sys\_id

</td><td>

Sys\_id of the reservation that was created.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr><td>

result.unSuccessfulReservations.user\_msg

</td><td>

Message about the update error.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to call this endpoint to update a group reservation.

```
curl "http://instance.servicenow.com/api/sn_wsd_rsv/group_reservation/update/b84e218a87586550cfaa99b73cbb35ec" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
    \"reservable_module\": \"5db44502dbb650106c731dcd13961937\",
    \"subject\": \"Test-123\",
    \"reservation_purpose\": \"meeting\",
    \"timezone\": \"US/Pacific\",
    \"children\": [
        {
            \"location\": \"6a11a94adb7210106c731dcd1396194e\",
            \"requested_for\": \"62826bf03710200044e0bfc8bcbe5df1\",
            \"is_private\": false
        },
        {
            \"location\": \"9841e94adb7210106c731dcd13961914\",
            \"requested_for\": \"6816f79cc0a8016401c5a33be04be441\",
            \"is_private\": false
        }
    ],
    \"start\": \"2023-02-12T11:30:00Z\",
    \"end\": \"2023-02-12T12:30:00Z\"
}" \
```

Return results:

```
{
  "result": {
    "parent": "b84e218a87586550cfaa99b73cbb35ec",
    "success": true,
    "successfulReservations": [
      {
        "operation": "create",
        "sys_id": "7b9e658a87586550cfaa99b73cbb357d",
        "msg": "",
        "user_msg": null,
        "location": "6a11a94adb7210106c731dcd1396194e"
      },
      {
        "operation": "create",
        "sys_id": "3b9e658a87586550cfaa99b73cbb3580",
        "msg": "",
        "user_msg": null,
        "location": "9841e94adb7210106c731dcd13961914"
      }
    ],
    "unSuccessfulReservations": []
  }
}
```

## WSD Group Reservation - POST /api/sn\_wsd\_rsv/group\_reservation/add

Creates a group reservation.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/group_reservation/add`

Default URL: `/api/sn_wsd_rsv/group_reservation/add`

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
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

children

</td><td>

Required. List of child reservations records to associate with the reservation.Data type: Array of Objects

```
"children": [
  {
    "is_private": Boolean,
    "location": "String",
    "requested_for": "String"
  }
]
```

</td></tr><tr><td>

children.is\_private

</td><td>

Flag that indicates whether the reservation is private. If private, the reservation doesn't appear to anyone except the owner.For additional information on these privacy settings, see Location privacy settings and impact.

Valid values:

-   true: Reservation is private.
-   false: Reservation isn't private.

Data type: Boolean

Default: Value set for privacy in the system properties.

</td></tr><tr><td>

children.location

</td><td>

Required. Sys\_id of the location to reserve.

Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

children.requested\_for

</td><td>

Required. Sys\_id of the user for whom the reservation is being requested.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

end

</td><td id="end-update_reserv-entry">

Required if the **shift** parameter isn't passed in. Requested end time of the reservation.Data type: String

Format: UTC or local time \(yyyy-mm-dd hh:mm:ss\)

</td></tr><tr><td>

requested\_for

</td><td id="requested_for-update_reserv-entry">

Sys\_id or email address of the user for which the reservation is being made.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

reservable\_module

</td><td id="reservable_module-update_reserv-entry">

Required. Sys\_id of the reservable module to associate with the reservation. A reservable module defines the workplace items needed for a reservation.Data type: String

Table: Reservable Module \[sn\_wsd\_rsv\_reservable\_module\]

</td></tr><tr><td>

shift

</td><td id="shift-update_reserv-entry">

Sys\_id of the shift to associate with the reservation. If this parameter is passed in, the **end** parameter isn't required.

For additional information on shift-based reservations, see Enable shift-based reservation.

Data type: String

Table: Shift \[sn\_wsd\_core\_shift\]

</td></tr><tr><td>

start

</td><td id="start-update_reserv-entry">

Required. Requested start time of the reservation.Data type: String

Format: UTC or local time \(yyyy-mm-dd hh:mm:ss\)

</td></tr><tr><td>

subject

</td><td id="subject-update_reserv-entry">

Required. Subject of the meeting associated with the reservation.

Data type: String

</td></tr><tr><td>

workplace\_location

</td><td>

Sys\_id of the workplace location to associate with the group reservation.Data type: String

Default: Empty - locations are specified in child reservations

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-reserv-entry">

Data format of the request body. Supported types: **application/json**, **application/xml** or, **text/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="content_type-JSON-only-entry-RESTAPI">

Data format of the request body. Only supports **application/json**.

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
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Details about the created group reservations.Data type: Object

```
"result": {
  "created_children": [Array],
  "failed_children": [Array],
  "msg": "String",
  "parent": "String",
  "success": Boolean,
  "user_msg": "String"
}
```

</td></tr><tr><td>

result.created\_children

</td><td>

Details about the child reservations that were created.Data type: Array of Objects

```
"created_children": [
  {
    "location": "String",
    "requested_for": "String",
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.created\_children.location

</td><td>

Sys\_id of the location to reserve.

Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

result.created\_children.requested\_for

</td><td>

Sys\_id of the user for whom the child reservation was created.Data type: String

</td></tr><tr><td>

result.created\_children.sys\_id

</td><td>

Sys\_id of the child reservation record that was created.Data type: String

</td></tr><tr><td>

result.failed\_children

</td><td>

Details about the child reservations that failed to be created.Data type: Array of Objects

```
"failed_children": [
  {
    "location": "String",
    "requested_for": "String",
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.failed\_children.location

</td><td>

Sys\_id of the location record associated with the failed reservation.Data type: String

</td></tr><tr><td>

result.failed\_children.requested\_for

</td><td>

Sys\_id of the user for whom the child reservation was requested.Data type: String

</td></tr><tr><td>

result.failed\_children.sys\_id

</td><td>

Always -1.Data type: String

</td></tr><tr><td>

result.msg

</td><td>

If the request fails, message that describes the error.Data type: String

</td></tr><tr><td>

result.parent

</td><td>

Sys\_id of the parent reservation record.

When a group reservation is created, one group parent record and one or more child reservation records are created. Reservation records contain a field called reservation\_subtype, that indicates the type of reservation record. For group parent records, this field is set to "Group parent" to indicate that it is a group parent record. For child records, this field is set to "Single".

Within a child record, the sys\_id of the associated parent reservation record is in the source\_reservation field.

Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr><td>

result.success

</td><td id="success-multi-entry">

Flag that indicates whether the reservation was successfully created.Possible values:

-   true: Successfully created.
-   false: Operation failed.

Data type: Boolean

</td></tr><tr><td>

result.userMsg

</td><td>

If the request fails, message that describes the error.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to use this endpoint to create a group reservations.

```
curl "http://instance.servicenow.com/api/sn_wsd_rsv/group_reservation/add" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
    \"reservable_module\": \"5db44502dbb650106c731dcd13961937\",
    \"subject\": \"Test-123\",
    \"reservation_purpose\": \"meeting\",
    \"timezone\": \"US/Pacific\",
    \"children\": [
        {
            \"location\": \"6a11a94adb7210106c731dcd1396194e\",
            \"requested_for\": \"62826bf03710200044e0bfc8bcbe5df1\",
            \"is_private\": false
        },
        {
            \"location\": \"9841e94adb7210106c731dcd13961914\",
            \"requested_for\": \"6816f79cc0a8016401c5a33be04be441\",
            \"is_private\": false
        }
    ],
    \"start\": \"2023-01-12T11:30:00Z\",
    \"end\": \"2023-01-12T12:30:00Z\"
}" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "parent": "b84e218a87586550cfaa99b73cbb35ec",
    "success": true,
    "created_children": [
      {
        "sys_id": "7c4e218a87586550cfaa99b73cbb35ee",
        "location": "6a11a94adb7210106c731dcd1396194e",
        "requested_for": "62826bf03710200044e0bfc8bcbe5df1"
      },
      {
        "sys_id": "3c4e218a87586550cfaa99b73cbb35f1",
        "location": "9841e94adb7210106c731dcd13961914",
        "requested_for": "6816f79cc0a8016401c5a33be04be441"
      }
    ],
    "failed_children": [],
    "user_msg": "",
    "msg": ""
  }
}
```

