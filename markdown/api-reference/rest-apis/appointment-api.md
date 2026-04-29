---
title: Appointment API
description: The Appointment API provides endpoints for interacting with the appointment booking application. Use this API to book and reschedule appointments, check available appointment slots, and fetch appointment booking configuration details.Returns the time range for which you can book appointments. The return results honor the lead time and maximum future bookable dates configured in the appointment booking service configuration.Returns the configuration defined in a specified Appointment Booking Service Configuration.Returns the sys\_id of the appointment booking service configuration rule that matches a specified task sys\_id or a set of specified catalog item data.Enables you to book and reschedule appointments for a Field Service Management task.Returns the slots that have been configured in the appointment booking service configuration along with their availability.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 30
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Appointment API

The Appointment API provides endpoints for interacting with the appointment booking application. Use this API to book and reschedule appointments, check available appointment slots, and fetch appointment booking configuration details.

Before using this API, the Appointment Booking Configuration and Service Configuration must be setup. In addition, a task for which the appointment is being booked must already exist. For additional information, see [Configuring Appointment Booking](https://www.servicenow.com/docs/access?context=appointment-booking-administer&version=australia&pubname=australia-field-service-management&ft:locale=en-US).

The Appointment API requires the Appointment Booking plugin \(com.snc.appointment\_booking\) and is provided within the `sn_apptmnt_booking` namespace. To access this API you must have the snc\_internal role.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Appointment - GET /sn\_apptmnt\_booking/appointment/calendar

Returns the time range for which you can book appointments. The return results honor the lead time and maximum future bookable dates configured in the appointment booking service configuration.

For additional information on lead time and maximum future bookable dates configuration, see [Create or modify an application configuration for Appointment Booking](https://www.servicenow.com/docs/access?context=appt-booking-create-app-config&version=australia&pubname=australia-field-service-management&ft:locale=en-US).

You must have either the snc\_internal or snc\_external role to access this endpoint.

### URL format

Versioned URL: `/api/sn_apptmnt_booking/{api_version}/appointment/calendar`

Default URL: `/api/sn_apptmnt_booking/appointment/calendar`

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

catalog\_id

</td><td>

Required. Sys\_id of the record producer configured with an appointment booking service configuration.Table: Record Producer \[sc\_cat\_item\_producer\]

Data type: String

</td></tr><tr><td>

location

</td><td>

Required. Sys\_id of the location of the appointment.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

opened\_for

</td><td>

Required. Sys\_id of the user for whom the appointment is being booked.Table: User \[sys\_user\]

Data type: String

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

result

</td><td>

Information about the results of the endpoint request.Data type: Object

```
"result": {
  "range_end": "String",
  "range_start": "String"
}
```

</td></tr><tr><td>

result.range\_end

</td><td>

End of the range in which the appointments can be booked. `Range End = Today + Maximum future bookable days`

Data type: String

Format: Appointment’s time zone in internal date time format.

</td></tr><tr><td>

result.range\_start

</td><td>

Start of the range in which the appointments can be booked.`Range Start = Today + Lead time`

Data type: String

Format: Appointment’s time zone in internal date time format.

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl "http://instance.servicenow.com/api/sn_apptmnt_booking/v1/appointment/calendar?catalog_id=e4c1116b3b810300ce8a4d72f3efc40f&location=32e8499cdb2d2200d75270f5bf9619d6&opened_for=6816f79cc0a8016401c5a33be04be441" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Result:

```
{
  "result": {
    "range_start": "2023-02-08 03:52:27",
    "range_end": "2023-02-21 23:52:27"
  }
}
```

## Appointment - GET /sn\_apptmnt\_booking/appointment/configuration

Returns the configuration defined in a specified Appointment Booking Service Configuration.

In addition, it returns the translations and user date and time preferences required to render the slots on the appointment booking widgets.

You must have either the snc\_internal or snc\_external role to access this endpoint.

### URL format

Versioned URL: `/api/sn_apptmnt_booking/{api_version}/appointment/configuration`

Default URL: `/api/sn_apptmnt_booking/appointment/configuration`

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

catalog\_id

</td><td>

Required. Sys\_id of the record producer configured with the appointment booking service configuration.Data type: String

Table: Record Producer \[sc\_cat\_item\_producer\]

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

result

</td><td>

Results of the endpoint request.Data type: Object

```
"result": {
  "active": Boolean,
  "active_string": "String",
  "advanced_calendar_view_portal": Boolean,
  "auto_acceptance": Boolean,
  "locale_language": "String",
  "service_config": {Object},
  "task_table": "String",
  "translations": {Object},
  "userDateFormatOptions": {Object},
  "useRR": Boolean,
  "userTimeFormat": {Object},
  "userTimeFormatOptions": {Object},
  "view_scale": "String"
}
```

</td></tr><tr><td>

result.active

</td><td>

Flag that indicates whether the service configuration setup for the associated catalog ID is active.Possible values:

-   true: Service configuration setup for the catalog ID is active.
-   false: Service configuration setup for the catalog ID isn't active.

Data type: Boolean

</td></tr><tr><td>

result.active\_string

</td><td>

Text representation of the status of the service configuration setup for the associated catalog ID.Data type: String

</td></tr><tr><td>

result.advanced\_calendar\_view\_portal

</td><td>

Flag that indicates whether the advanced calendar view displays on the portal or displays the base view. For additional information on the advanced calendar view, see [Create or modify an application configuration for Appointment Booking](https://www.servicenow.com/docs/access?context=appt-booking-create-app-config&version=australia&pubname=australia-field-service-management&ft:locale=en-US).Possible values:

-   true: Advanced calendar view displays on the portal.
-   false: Basic view displays on the portal.

Data type: Boolean

</td></tr><tr><td>

result.auto\_acceptance

</td><td>

Flag that indicates whether the appointment automatically transitions to the accepted state.Possible values:

-   true: Appointment automatically transitions to the accepted state.
-   false: Agent must manually accept the appointment.

Data type: Boolean

</td></tr><tr><td>

result.locale\_language

</td><td>

User's language setting.Data type: String

Format: ISO 639.1 language code

</td></tr><tr><td>

result.service\_config

</td><td>

Details about the service configuration.Data type: Object

```
"service_config": {
  "active": Boolean,
  "active_string": "String",
  "appointment_booking_config": "String",
  "appointment_duration": "String",
  "appointments_per_bookable_slot": "String",
  "bookable_days": "String",
  "cancel_by_time": "String",
  "default_timezone": "String",
  "enable_advanced_config": Boolean,
  "field_mapping": {Object},
  "future_bookable_max_days": "String",
  "lead_time": "String",
  "mandatory": "String",
  "use_slot_end_time_as": "String",
  "work_duration": "String"
}
```

</td></tr><tr><td>

result.service\_config.active

</td><td>

Flag that indicates the active status of the appointment booking service configuration.Possible values:

-   true: Active
-   false: Inactive

Data type: Boolean

</td></tr><tr><td>

result.service\_config.active\_string

</td><td>

Text representation of the status of the appointment booking service configuration.Data type: String

</td></tr><tr><td>

result.service\_config.​appointment\_booking\_config

</td><td>

Sys\_id of the appointment booking service configuration setup for the associated catalog ID.Data type: String

Table: Appointment Booking Service Configuration \[sn\_apptmnt\_booking\_service\_config\]

</td></tr><tr><td>

result.service\_config.​appointment\_duration

</td><td>

Length of the appointment.Data type: String

Unit: Minutes

</td></tr><tr><td>

result.service\_config.​appointments\_per\_bookable\_slot

</td><td>

Number of appointments that can be booked for the associated slot.Data type: String

</td></tr><tr><td>

result.service\_config.​bookable\_days

</td><td>

Comma-separated values representing the days on which appointments can be booked. Days are represented as integers where, Monday = 1 and Sunday = 7.

Data type: String

</td></tr><tr><td>

result.service\_config.cancel\_by\_time

</td><td>

Minimum amount of time prior to the start of an appointment that a user can cancel the appointment. For example, if you have an appointment booked for 1:00pm and there's a 2 hour cancel by time, you must cancel the appointment no later than 10:59 am.Format: This value is the date and time difference from “1970-01-01 00:00:00”. So if the returned value is "1970-01-01 04:00:00, it means that the room must be canceled four hours before the meeting starts.

Data type: String

</td></tr><tr><td>

result.service\_config.default\_timezone

</td><td>

Time zone configuration that appointments are booked in. Possible values:

-   location: Use the time zone of the location of the appointment.
-   user: Use the time zone of the person for whom the appointment is being booked.

Data type: String

</td></tr><tr><td>

result.service\_config.​enable\_advanced\_config

</td><td>

Flag that indicates whether appointment booking configurations and appointment booking rules are considered when booking appointments. For additional information, see [Create appointment booking advanced configuration](https://www.servicenow.com/docs/access?context=appintment-booking-day-level-config&version=australia&pubname=australia-field-service-management&ft:locale=en-US).Possible values:

-   true: Appointment booking configurations and appointment booking rules are considered when booking appointments.
-   false: Appointment booking configurations and appointment booking rules aren't considered when booking appointments.

Data type: Boolean

</td></tr><tr><td>

result.service\_config.field\_mapping

</td><td>

Details about the catalog variables mapped to the location and contact values used to book the appointment.Data type: Object

```
"field_mapping": {
  "contact": "String",
  "contactRPVariable": {Object},
  "location": "String",
  "locationRPVariable": {Object}
}
```

</td></tr><tr><td>

result.service\_config.​field\_mapping.contact

</td><td>

Name of the catalog variable that contains the contact value.Data type: String

</td></tr><tr><td>

result.service\_config.field\_mapping.​contactRPVariable

</td><td>

Details about the location catalog variables data.Data type: Object

```
"contactRPVariable": {
  "displayName": "String",
  "label": "String",
  "name": "String"
}
```

</td></tr><tr><td>

result.service\_config.field\_mapping.​contactRPVariable.displayName

</td><td>

Display name of the contact catalog variable.Data type: String

</td></tr><tr><td>

result.service\_config.field\_mapping.​contactRPVariable.label

</td><td>

Label of the contact catalog variable.Data type: String

</td></tr><tr><td>

result.service\_config.field\_mapping.​contactRPVariable.name

</td><td>

Name of the contact catalog variable.Data type: String

</td></tr><tr><td>

result.service\_config.​field\_mapping.location

</td><td>

Name of the catalog variable that contains the location value.Data type: String

</td></tr><tr><td>

result.service\_config.field\_mapping.​locationRPVariable

</td><td>

Details about the location catalog variables data.Data type: Object

```
"locationRPVariable": {
  "displayName": "String",
  "label": "String",
  "name": "String"
}
```

</td></tr><tr><td>

result.service\_config.field\_mapping.​locationRPVariable.displayName

</td><td>

Display name of the location catalog variable.Data type: String

</td></tr><tr><td>

result.service\_config.field\_mapping.​locationRPVariable.label

</td><td>

Label of the location catalog variable.Data type: String

</td></tr><tr><td>

result.service\_config.field\_mapping.​locationRPVariable.name

</td><td>

Name of the location catalog variable.Data type: String

</td></tr><tr><td>

result.service\_config.​ future\_bookable\_max\_days

</td><td>

Maximum number of days in the future that an appointment can be booked.Data type: String

</td></tr><tr><td>

result.service\_config.lead\_time

</td><td>

Minimum amount of time prior to the start of an appointment that a user can book the appointment. For example, if you want to book an appointment at 1:00pm and there’s a 2-hour lead time, you must book the appointment no later than 10:59 am.Format: This value is the date and time difference from “1970-01-01 00:00:00”. So if the returned value is "1970-01-01 04:00:00, it means that the room must be booked four hours before the meeting starts.

Data type: String

</td></tr><tr><td>

result.service\_config.mandatory

</td><td>

Indicator for whether the appointment is mandatory.Possible values:

-   0: Appointment isn't mandatory.
-   1: Appointment is mandatory.

Data type: String

</td></tr><tr><td>

result.service\_config.​use\_slot\_end\_time\_as

</td><td>

Indicator as to when an agent will arrive or complete the work scheduled for the associated appointment.Possible values:

-   arrive\_by: Agent will arrive at the location for the appointment within the specified time slot.
-   complete\_by: Agent will complete the work for the appointment within the specified time slot.
-   empty: Same as completed\_by.

Data type: String

</td></tr><tr><td>

result.service\_config.work\_duration

</td><td>

Amount of time it takes to work on the appointment. Work duration is configured in the appointment booking service configuration. For additional information, see [Create or modify service configuration for Appointment Booking](https://www.servicenow.com/docs/access?context=appt-booking-create-service-config&version=australia&pubname=australia-field-service-management&ft:locale=en-US).Data type: String

Unit: Minutes

</td></tr><tr><td>

result.task\_table

</td><td>

Name of the table for which the appointment can be booked. Configured in the appointment booking service configuration.Data type: String

</td></tr><tr><td>

result.translations

</td><td>

Name-value pairs of text translations used by the appointment booking widget. Contains translated values for actions, messages, days, and months.Data type: Object

</td></tr><tr><td>

result.userDateFormatOptions

</td><td>

Describes the date format options that are needed to render JS date objects. These values are set in appointment booking constants which are not modifiable.Data type: Object

```
"userDateFormatOptions": {
  "day": "String",
  "month": "String",
  "week": "String",
  "weekday": "String"
}
```

</td></tr><tr><td>

result.userDateFormatOptions.day

</td><td>

Day date format.Data type: String

Format: Numeric \(Values or 1-31\)

</td></tr><tr><td>

result.userDateFormatOptions.month

</td><td>

Month date format.Data type: String

Format: Short \(Values on Jan, Feb, Mar, and so on\)

</td></tr><tr><td>

result.userDateFormatOptions.week

</td><td>

Week date format.Data type: String

Format: Numeric \(Values of 1-5\)

</td></tr><tr><td>

result.userDateFormatOptions.weekday

</td><td>

Weekday date format.Data type: String

Format: Short \(Values of Mon, Tue, Wed, and so on\)

</td></tr><tr><td>

result.useRR

</td><td>

Value of the sn\_apptmnt\_booking.use\_read\_replica\_from\_ui property. This value defines whether to use the read replica database to fetch appointment slots when the query is performed from the UI.Possible values:

-   true: Use the read replica database to fetch the slots.
-   false: Don't use the read replica database to fetch the slots.

Data type: Boolean

</td></tr><tr><td>

result.userTimeFormat

</td><td>

Describes the user's time format. The user is the person making the endpoint request. If made through the platform, it is an agent. If made through the portal, it is a customer.

Data type: Object

```
"userTimeFormat": {
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.userTimeFormat.type

</td><td>

Type of time format.Possible values:

-   12hr
-   24hr

Data type: String

</td></tr><tr><td>

result.userTimeFormat.value

</td><td>

Preferred time format, such as "HH:mm:ss".Data type: String

</td></tr><tr><td>

result.userTimeFormatOptions

</td><td>

Describes the time format options that are needed to render JS time objects. These values are set in the appointment booking constants which can't be modified.Data type: Object

```
"userTimeFormatOptions": {
  "hour": "String",
  "hourCycle": "String",
  "minute": "String"
}
```

</td></tr><tr><td>

result.userTimeFormatOptions.hour

</td><td>

Format for hours.Format: numeric \(Values 1-12\)

</td></tr><tr><td>

result.userTimeFormatOptions.hourCycle

</td><td>

Format for hour cycle.Only possible value is `h23`.

</td></tr><tr><td>

result.userTimeFormatOptions.minute

</td><td>

Format for minutes.Format: numeric \(Values of 1-60\)

</td></tr><tr><td>

result.view\_scale

</td><td>

View configured in the service configuration. Possible values:

-   day
-   week

Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl "http://instance.servicenow.com/api/sn_apptmnt_booking/v1/appointment/configuration?catalog_id=e4c1116b3b810300ce8a4d72f3efc40f" \
--request GET \
--header "Accept:application/json" \
--user ‘username':'password'
```

Response:

```
{
  "result": {
    "active": true,
    "activeString": "true"
    "view_scale": "day",
    "auto_acceptance": true,
    "task_table": "wm_order",
    "advanced_calendar_view_portal": false,
    "service_config": {
      "appointment_booking_config": "deb1d2fd3b033200ce8a4d72f3efc4c2",
      "future_bookable_max_days": "14",
      "appointments_per_bookable_slot": "20",
      "bookable_days": "1,2,3,4,5",
      "active": true,
      "activeString": "true",
      "mandatory": "1",
      "lead_time": "1970-01-01 04:00:00",
      "cancel_by_time": "1970-01-01 04:00:00",
      "appointment_duration": "120",
      "default_timezone": "location",
      "work_duration": "60",
      "enable_advanced_config": true,
      "field_mapping": {
        "location": "location"
        "opened_for": "contact",
        "locationRPVariable": {
          "name": "location",
          "label": "Location",
          "displayName": "location"
        },
        "contactRPVariable": {
          "name": "contact",
          "label": "Contact",
          "displayName": "contact"
        }
      },
      "use_slot_end_time_as": ""
    },
    "translations": {
      "submit_btn_text": "Select",
      "cancel_btn_text": "Cancel",
      "calendar_prev_text": "Previous",
      "select_appointment_calendar_text": "Select Appointment Calendar",
      "calendar_next_text": "Next",
      "previous_btn_text": "Previous day",
      "next_btn_text": "Next day",
      "date_input_placeholder_text": "Pick a date",
      "show_calendar_btn_text": "Show Calendar",
      "app_window_btn_text_start_time": "Start time",
      "app_window_btn_text_end_time": "End time",
      "appointment_window_aria_label_start_text": "Available appointment window ",
      "no_appointment": "No appointments",
      "time_zone": "Time zone",
      "selected_window": "The window which has been selected is ",
      "day_names": {
        "1": "Monday",
        "2": "Tuesday",
        "3": "Wednesday",
        "4": "Thursday",
        "5": "Friday",
        "6": "Saturday",
        "7": "Sunday"
      },
      "days": [
        "Sunday",
        "Monday",
        "Tuesday",
        "Wednesday",
        "Thursday",
        "Friday",
        "Saturday"
      ],
      "daysShort": [
        "Sun",
        "Mon",
        "Tue",
        "Wed",
        "Thu",
        "Fri",
        "Sat"
      ],
      "daysMin": [
        "Su",
        "Mo",
        "Tu",
        "We",
        "Th",
        "Fr",
        "Sa"
      ],
      "months": [
        "January",
        "February",
        "March",
        "April",
        "May",
        "June",
        "July",
        "August",
        "September",
        "October",
        "November",
        "December"
      ],
      "monthsShort": [
        "Jan",
        "Feb",
        "Mar",
        "Apr",
        "May",
        "Jun",
        "Jul",
        "Aug",
        "Sep",
        "Oct",
        "Nov",
        "Dec"
      ],
      "today": "Today",
      "clear": "Clear",
      "language": "en",
      "arrive_by_msg": "The agent will arrive within the selected slot."
    },
    "useRR": true,
    "locale_language": "en",
    "userTimeFormat": {
      "value": "HH:mm:ss",
      "type": "24hr"
    },
    "userDateFormatOptions": {
      "weekday": "short",
      "year": "numeric",
      "month": "short",
      "day": "numeric"
    },
    "userTimeFormatOptions": {
      "hour": "numeric",
      "minute": "numeric",
      "hourCycle": "h23"
    }
  }
}
```

## Appointment - GET /sn\_apptmnt\_booking/appointment/execute\_rule\_conditions

Returns the sys\_id of the appointment booking service configuration rule that matches a specified task sys\_id or a set of specified catalog item data.

The passed task ID or catalog item data is evaluated against the rules defined for a service configuration. The sys\_id for the first rule for which these conditions match is returned. You must then pass this rule sys\_id to subsequent availability requests to fetch the correct slots, which are defined in the rule.

You must have either the snc\_internal or snc\_external role to access this endpoint.

### URL format

Versioned URL: `/api/sn_apptmnt_booking/{api_version}/appointment/execute_rule_conditions`

Default URL: `/api/sn_apptmnt_booking/appointment/execute_rule_conditions`

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

catalogId

</td><td>

Required. Sys\_id of the record producer configured with the appointment booking service configuration.Data type: String

Table: Record Producer \[sc\_cat\_item\_producer\]

</td></tr><tr><td>

otherInputs

</td><td>

Required if the **taskId** parameter isn’t specified. Name-value pairs of catalog item variables to compare against the rules defined for a service configuration.

For example:

```
"otherInputs": {
  "u_sn_point_of_sale_variable_set": "true",
  "short_description": "Point-of-Sale Installation",
  "contact": "6816f79cc0a8016401c5a33be04be441",
  "description": "Install new point-of-sale system with cash tray",
  "location": "32e8499cdb2d2200d75270f5bf9619d6"
}
```

Data type: Object

</td></tr><tr><td>

taskId

</td><td>

Required if the **otherInputs** parameter isn’t specified.Sys\_id of the task record for which the appointment is being booked. Located in the task table for which the appointment is being booked. The **catalogId** corresponds to a particular appointment booking configuration and every config has a task table on which the appointment is booked.

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

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

result

</td><td>

Description of the information returned by the endpoint.Data type: Object

```
“result": {
  "dedicatedCapacity": Boolean,
  "futureMaxBookableDays": "String",
  "ruleId": "String",
  "ruleName": "String"
}
```

</td></tr><tr><td>

result.dedicatedCapacity

</td><td>

Flag that indicates whether the associated rule has dedicated capacity. For additional information on dedicated capacity, see [Create service configuration rules for a service configuration](https://www.servicenow.com/docs/access?context=create-appt-booking-service-config-rules&version=australia&pubname=australia-field-service-management&ft:locale=en-US).Possible values:

-   true: Rule has dedicated capacity.
-   false: Capacity is shared between the associated rule and the base configuration. It’s also shared with other rules that don't have dedicated capacity.

Data type: Boolean

</td></tr><tr><td>

result.futureMaxBookableDays

</td><td>

Maximum number of days in the future for which an appointment with the matching rule can be booked.Data type: String

</td></tr><tr><td>

result.ruleId

</td><td>

Sys\_id of the appointment booking service configuration rule that matches the **taskId** or **otherInputs** parameters passed in the request.Data type: String

Table: Service Configuration Rule \[sn\_apptmnt\_booking\_config\_rule\]

</td></tr><tr><td>

result.ruleName

</td><td>

Name of the rule that matched the passed parameters.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to use the **taskId** parameter to make the rule comparison request.

```
curl "http://instance.servicenow.com/api/sn_apptmnt_booking/v1/appointment/execute_rule_conditions" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"catalogId\": \"e4c1116b3b810300ce8a4d72f3efc40f\",
  \"taskId\": \"ce1f397c43b861105e0dbcba6ab8f298\"}" \
--user 'username':'password'
```

Response:

```
{
  "result": {
    "ruleId": "f7d5d98f437c21105e0dbcba6ab8f2fc",
    "ruleName": "Priority 1 rule",
    "dedicatedCapacity": true,
    "futureMaxBookableDays": "14"
  }
}
```

### cURL request

The following code example shows how to use the **otherInputs** parameter to make the rule comparison request.

```
curl "http://instance.servicenow.com/api/sn_apptmnt_booking/v1/appointment/execute_rule_conditions" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"catalogId\": \"e4c1116b3b810300ce8a4d72f3efc40f\",
  \"otherInputs\": {
    \"u_sn_point_of_sale_variable_set\": \"true\",
    \"short_description\": \"Point-of-Sale Installation\",
    \"contact\": \"6816f79cc0a8016401c5a33be04be441\",
    \"description\": \"Install new point-of-sale system with cash tray\",
    \"location\": \"32e8499cdb2d2200d75270f5bf9619d6\"
  }
}" \
--user 'username':'password'
```

Response:

```
{
  "result": {
    "ruleId": " 1d1bb72b4334a1105e0dbcba6ab8f275",
    "ruleName": "Lake View SC rule",
    "dedicatedCapacity": false,
    "futureMaxBookableDays": "21"
  }
}
```

## Appointment - POST /sn\_apptmnt\_booking/appointment/appointment

Enables you to book and reschedule appointments for a Field Service Management task.

**Note:** This endpoint only enables you to book and schedule appointments that have start and end times defined in the associated appointment booking service configuration and have available slots.

For additional information on Field Service Management tasks, see [Configuring Appointment Booking](https://www.servicenow.com/docs/access?context=appointment-booking-administer&version=australia&pubname=australia-field-service-management&ft:locale=en-US).

### URL format

Versioned URL: `/api/sn_apptmnt_booking/{api_version}/appointment/appointment`

Default URL: `/api/sn_apptmnt_booking/appointment/appointment`

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

actualEndDate

</td><td>

Required. End date and time for the appointment slot in the appointment's time zone.Date type: String

Format: YYYY-MM-dd HH:mm:ss

</td></tr><tr><td>

actualStartDate

</td><td>

Required. Start date and time for the appointment slot in the appointment's time zone.Date type: String

Format: YYYY-MM-dd HH:mm:ss

</td></tr><tr><td>

catalogId

</td><td>

Sys\_id of the record producer configured for the appointment booking service configuration.If you don't pass this parameter, the endpoint will attempt to discern this information from the **taskId** and **taskTable** parameters. If it can't, the endpoint fails, and an error is returned.

Date type: String

Table: The Catalog Item field of the Appointment Booking Service Configuration \[sn\_apptmnt\_booking\_service\_config\] table.

</td></tr><tr><td>

endDateUTC

</td><td>

Required. End date and time for the appointment slot in UTC time zone.Date type: String

Format: YYYY-MM-dd HH:mm:ss

</td></tr><tr><td>

location

</td><td>

Required. Sys\_id of the location record related to the appointment.Date type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

openedFor

</td><td>

Required. Sys\_id of the user for which the appointment is being booked.Date type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

reschedule

</td><td>

Required. Flag that indicates whether the appointment is being rescheduled.Valid values:

-   true: Appointment currently exists and is being rescheduled.
-   false: New appointment.

Data type: Boolean

</td></tr><tr><td>

service\_cofig\_rule

</td><td>

If the appointment is being booked under a rule, the sys\_id of the service configuration rule.Date type: String

Table: Service Configuration Rule \[sn\_apptmnt\_booking\_config\_rule\]

</td></tr><tr><td>

startDateUTC

</td><td>

Required. Start date and time for the appointment slot in UTC time zone.Date type: String

Format: YYYY-MM-dd HH:mm:ss

</td></tr><tr><td>

taskId

</td><td>

Required. Sys\_id of the task record for which the appointment is being booked.Date type: String

Table: Defined in the **taskTable** parameter.

</td></tr><tr><td>

taskTable

</td><td>

Required. Name of the table containing the task record for which the appointment is being booked.Date type: String

</td></tr><tr><td>

timezone

</td><td>

Required. Time zone to use when booking or updating the specified appointment slot.Format: Country/City or Area format, such as US/Eastern

Date type: String

</td></tr><tr><td>

validate\_request

</td><td>

Flag that indicates whether to validate the appointment request. If any of the validations fail, the endpoint fails and returns an error message that describes the problem.The following validations are performed:

-   Catalog ID validation: Verifies that the passed **catalogId** parameter is a valid sys\_id.
-   Time zone validation: Verifies that the passed **timezone** parameter is a valid time zone.
-   Task ID validation: Verifies that the passed **taskId** parameter is a valid sys\_id and the task is in the pending dispatch state.
-   Duplicate slot validation: For reschedules, if you pass the same slot as the original appointment, the slot is invalid as the slot is technically already booked.
-   Slot validation: Verifies that the passed slot information matches what is configured and that the slot has the same time frame. For example, if in the configuration a two-hour slot is configured, but you pass a three-hour slot, the slot is not valid. Similarly, if the 9:00 a.m. to 11:00 a.m. slot is available, but the passed slot is for 9:30 a.m. to 11:30 a.m., then the passed slot is invalid.

Valid values:

-   true: Validate the appointment information.
-   false: Don't validate the appointment information.

Data type: Boolean

Default: false

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

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

result

</td><td>

Information about the results of the endpoint request.Data type: Object

```
"result": {
  "data": "String",
  "message": "String",
  "reason": "String",
  "success": Boolean
}
```

</td></tr><tr><td>

result.data

</td><td>

Sys\_id of the appointment record that has been created or rescheduled.Data type: String

</td></tr><tr><td>

result.message

</td><td>

Message that explains whether the appointment request was scheduled or failed. For example, error responses might include:-   Your appointment cannot be scheduled.
-   Your appointment cannot be rescheduled.

If the operation is successful, a message similar to the following is returned: Your appointment has been scheduled successfully.Data type: String

</td></tr><tr><td>

result.reason

</td><td>

Additional information about the results of the appointment request.Data type: String

</td></tr><tr><td>

result.success

</td><td>

Flag that indicates whether the request was successful.Possible values:

-   true: Request succeeded
-   false: Request failed

Data type: Boolean

</td></tr></tbody>
</table>### cURL request

The following example shows how to create a new appointment booking for a task in the Work Order \[wm\_order\] table.

```
curl "https://instance.servicenow.com/api/sn_apptmnt_booking/appointment/appointment" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
\"startDateUTC\": \"2023-02-01 20:00:00\",
\"endDateUTC\": \"2023-02-01 22:00:00\",
\"actualStartDate\": \"2023-02-01 15:00:00\",
\"actualEndDate\": \"2023-02-01 17:00:00\",
\"taskTable\": \"wm_order\",
\"location\": \"32e8499cdb2d2200d75270f5bf9619d6\",
\"catalogId\": \"e4c1116b3b810300ce8a4d72f3efc40f\",
\"openedFor\": \"ddce70866f9331003b3c498f5d3ee417\"
\"taskId\": \"ce1f397c43b861105e0dbcba6ab8f298\",
\"reschedule\": false,
\"service_configuration_rule\": \"\",
\"timezone\": \"US/Eastern\"
}" \

--user 'username':'password'
```

Response:

```
{
"result": {
  "success": true,
  "message": "Your appointment has been scheduled successfully.",
  "reason": "Appointment created!",
  "data": "7a5f393c43b861105e0dbcba6ab8f29f"
  }
}
```

## Appointment - POST /sn\_apptmnt\_booking/appointment/availability

Returns the slots that have been configured in the appointment booking service configuration along with their availability.

If advanced configurations are enabled for the service configuration, the endpoint honors these configurations, and returns the data according to the rules and advanced configuration. You can also use this endpoint to find the first available slot by passing the **get\_next\_available\_slot** parameter or **get\_next\_available\_day\_data** parameter in the request body as `true`.

You must have either the snc\_internal or snc\_external role to access this endpoint.

### URL format

Versioned URL: `/api/sn_apptmnt_booking/{api_version}/appointment/availability`

Default URL: `/api/sn_apptmnt_booking/appointment/availability`

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

catalog\_id

</td><td>

Sys\_id of the record producer configured for the appointment booking service configuration.If you don't pass this parameter, the endpoint will attempt to discern this information from the **taskId** and **task\_table** parameters. If it can't, the endpoint fails, and an error is returned.

Data type: String

Table: In the Catalog Item field in the related record of the Appointment Booking Service Configuration \[sn\_apptmnt\_booking\_service\_config\] table.

</td></tr><tr><td>

end\_date

</td><td>

Required. End date and time for which to fetch appointments.Data type: String

Format: UTC time zone and in the format YYYY-MM-dd HH:mm:ss

</td></tr><tr><td>

fetch\_days\_slot

</td><td>

Flag that indicates whether to return the first available slot in each day for the requested date range.Valid values:

-   true: Return the first available slot for each day.
-   false: Don't return the first available slot for each day.

Data type: Boolean

Default: false

</td></tr><tr><td>

full\_day

</td><td>

Required. Flag that indicates whether to return all appointments for the specified date range passed regardless of the time values in start and end date.Valid values:

-   true: Return all appointments regardless of specified times.
-   false: Only return appointments that correspond to the specified dates and times.

Data type: Boolean

</td></tr><tr><td>

get\_next\_available\_slot

</td><td>

Flag that indicates whether to return the first available appointment slot with the response even if it isn't part of the passed-in **start\_date** and **end\_date** parameters.Valid values:

-   true: Return the first available appointment slots.
-   false: Don't return the first available appointment slots.

Data type: Boolean

Default: false

</td></tr><tr><td>

limit

</td><td>

Maximum number of appointments to return.Data type: Number

Default: Value specified in the sn\_apptmnt\_booking .max\_appointments\_ returned property or 1000 if the property is empty.

</td></tr><tr><td>

location

</td><td>

Required. Sys\_id of the location record associated with the appointment.Data type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

opened\_for

</td><td>

Required. Sys\_id of the user for which the appointment is being booked.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

otherInputs

</td><td>

Name-value pairs of any other values needed to calculate the availability in the scripted method. Typically these values are catalog item variables, however, if you customize your booking application you can pass any values needed by your implementation.For example:

```
"otherInputs": {
  "u_sn_point_of_sale_variable_set": "true",
  "short_description": "Point-of-Sale Installation",
  "contact": "6816f79cc0a8016401c5a33be04be441",
  "description": "Install new point-of-sale system with cash tray",
  "location": "32e8499cdb2d2200d75270f5bf9619d6"
}
```

Data type: Object

</td></tr><tr><td>

service\_config\_rule

</td><td>

Sys\_id of the service configuration rule to use to calculate the appointment slots and availability.Data type: String

Table: Service Configuration Rule \[sn\_apptmnt\_booking\_config\_rule\]

</td></tr><tr><td>

start\_date

</td><td>

Required. Start date and time for which to fetch appointments.Data type: String

Format: UTC time zone and in the format YYYY-MM-dd HH:mm:ss

</td></tr><tr><td>

taskId

</td><td>

Sys\_id of the task record for which the appointment is being booked.Date type: String

Table: Defined in the **taskTable** parameter.

</td></tr><tr><td>

task\_table

</td><td>

Required. Name of the table containing the task record for which the appointment is being booked.Data type: String

</td></tr><tr><td>

use\_read\_replica

</td><td>

Flag that indicates whether to use the read replica of the database when fetching the appointment slots and their availability.Valid values:

-   true: Use the read replica of the database.
-   false: Don't use the read replica of the database.

Default: false

</td></tr><tr><td>

view

</td><td>

Required. Origination point of the request.Valid values: \(case-sensitive\)

-   platform
-   portal

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

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

result

</td><td>

Details about the appointments that match the request.Data type: Object

```
"result": {
 "availability": [Array], 
 "has_more": Boolean,
 "next_available_slot": {Object},
 "no_appt_available": Boolean,
 "success": Boolean,
 "time_zone": "String",
 "time_zone_display_value": "String"
}
```

</td></tr><tr><td>

result.availability

</td><td>

List of appointment slots that meet the specified request. Data type: Array of Objects

```
"availability": [{
  "available": Boolean,
  "end_date": "String",
  "end_date_display": "String",
  "end_dateUTC": "String",
  "start_date": "String", 
  "start_date_display": "String",
  "start_dateUTC": "String"
}]
```

</td></tr><tr><td>

result.availability.available

</td><td>

Flag that indicates whether the associated time slot is available.Possible values:

-   true: Time slot is available.
-   false: Times slot isn't available.

Data type: Boolean

</td></tr><tr><td>

result.availability.end\_date

</td><td>

End date and time of the associated appointment. The time zone is based on the value in the **time\_zone** parameter.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

result.availability.end\_date\_display

</td><td>

Display end date and time of the associated appointment. The time zone is based on the value in the **time\_zone\_display\_value** parameter.Data type: String

Format: Requesting user's date time format.

</td></tr><tr><td>

result.availability.end\_dateUTC

</td><td>

End date and time of the associated appointment in UTC time.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

result.availability.start\_date

</td><td>

Start date and time of the associated appointment. The time zone is based on the value in the **time\_zone** parameter.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

result.availability.start\_date\_display

</td><td>

Display start date and time of the associated appointment. The time zone is based on the value in the **time\_zone\_display\_value** parameter.Data type: String

Format: Requesting user's date time format.

</td></tr><tr><td>

result.availability.start\_dateUTC

</td><td>

Start date and time of the associated appointment in UTC time.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

result.has\_more

</td><td>

Flag that indicates whether there are more appointment slots to fetch after returning the limit.Possible values:

-   true: More appointment slots are available.
-   false: No more slots are available.

Data type: Boolean

</td></tr><tr><td>

result.next\_available\_slot

</td><td>

If the **get\_next\_available\_slot** parameter was passed as true, details about the first available slot irrespective of the passed start and end date. Data type: Object

```
"next_available_slot": {
  "available": Boolean,
  "end_date": "String",
  "end_date_display": "String",
  "end_dateUTC": "String",
  "start_date": "String", 
  "start_date_display": "String",
  "start_dateUTC": "String"
}
```

</td></tr><tr><td>

result.next\_available\_slot.available

</td><td>

Flag that indicates whether the associated time slot is available.Possible values:

-   true: Time slot is available.
-   false: Times slot isn't available.

Data type: Boolean

</td></tr><tr><td>

result.next\_available\_slot.end\_date

</td><td>

End date and time of the associated appointment. The time zone is based on the value in the **time\_zone** parameter.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

result.next\_available\_slot.end\_date\_display

</td><td>

Display end date and time of the associated appointment. The time zone is based on the value in the **time\_zone\_display\_value** parameter.Data type: String

</td></tr><tr><td>

result.next\_available\_slot.end\_dateUTC

</td><td>

End date and time of the associated appointment in UTC time.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

result.next\_available\_slot.start\_date

</td><td>

Start date and time of the associated appointment. The time zone is based on the value in the **time\_zone** parameter.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

result.next\_available\_slot.start\_date\_display

</td><td>

Display start date and time of the associated appointment. The time zone is based on the value in the **time\_zone\_display\_value** parameter.Data type: String

</td></tr><tr><td>

result.next\_available\_slot.start\_dateUTC

</td><td>

Start date and time of the associated appointment in UTC time.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

result.no\_appt\_available

</td><td>

Flag that indicates whether there are more appointment slots available for the specified date and time.Possible values:

-   true: More appointment time slots are available.
-   false: No more appointment time slots are available.

Data type: Boolean

</td></tr><tr><td>

result.success

</td><td>

Flag that indicates whether the endpoint call was successful.Possible values:

-   true: Endpoint call was successful.
-   false: Endpoint call failed.

Data type: Boolean

</td></tr><tr><td>

result.time\_zone

</td><td>

Time zone in which the appointment slots were rendered. Based on the values in the appointment booking service configuration.Data type: String

</td></tr><tr><td>

result.time\_zone\_display\_value

</td><td>

Display time zone in which the appointment slots were rendered. Based on the values in the appointment booking service configuration.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl "http://instance.servicenow.com/api/sn_apptmnt_booking/v1/appointment/availability" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"start_date\": \"2023-02-05 05:00:00\",
  \"end_date\": \"2023-02-07 04:59:59\",
  \"location\": \"32e8499cdb2d2200d75270f5bf9619d6\",
  \"catalog_id\": \"e4c1116b3b810300ce8a4d72f3efc40f\",
  \"opened_for\": \"6816f79cc0a8016401c5a33be04be441\",
  \"full_day\": false,
  \"task_table\": \"wm_order\",
  \"view\": \"portal\",
  \"get_next_available_slot\": true,
  \"use_read_replica\": true,
  \"service_config_rule\": \"f7d5d98f437c21105e0dbcba6ab8f2fc\"
}" \
--user 'username':'password
```

Response:

```
{
"result": {
  "success": true,
  "availability": [
    {
      "start_date": "2023-02-06 09:00:00",
      "end_date": "2023-02-06 11:00:00",
      "start_date_display": "09:00",
      "end_date_display": "11:00",
      "start_dateUTC": "2023-02-06 14:00:00",
      "end_dateUTC": "2023-02-06 16:00:00",
      "available": false
    },
    {
      "start_date": "2023-02-06 13:00:00",
      "end_date": "2023-02-06 15:00:00",
      "start_date_display": "13:00",
      "end_date_display": "15:00",
      "start_dateUTC": "2023-02-06 18:00:00",
      "end_dateUTC": "2023-02-06 20:00:00",
      "available": false
    },
    {
      "start_date": "2023-02-06 15:00:00",
      "end_date": "2023-02-06 17:00:00",
      "start_date_display": "15:00",
      "end_date_display": "17:00",
      "start_dateUTC": "2023-02-06 20:00:00",
      "end_dateUTC": "2023-02-06 22:00:00",
      "available": false
    }
  ],
  "has_more": false,
  "no_appt_available": true,
  "time_zone": "US/Eastern",
  "time_zone_display_value": "US/Eastern",
  "next_available_slot": {
    "start_date": "2023-02-10 13:00:00",
    "end_date": "2023-02-10 15:00:00",
    "start_date_display": "13:00",
    "end_date_display": "15:00",
    "start_dateUTC": "2023-02-10 18:00:00",
    "end_dateUTC": "2023-02-10 20:00:00",
    "available": true
}
```

