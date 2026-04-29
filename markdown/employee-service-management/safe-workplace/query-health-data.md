---
title: Get employee or visitor health data
description: Send a GET request for Employee Health and Safety Status data to use in your third-party system. Get data to determine an employee or visitor's current health status.
locale: en-US
release: australia
product: Safe Workplace
classification: safe-workplace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrating with Safe Workplace suite, Safe Workplace, Health and Safety, Employee Service Management]
---

# Get employee or visitor health data

Send a GET request for Employee Health and Safety Status data to use in your third-party system. Get data to determine an employee or visitor's current health status.

## Before you begin

Role required: sn\_imt\_core.reader

## Procedure

1.  Send a GET request to the Table API on your instance.

    For more information, see [Table API](https://www.servicenow.com/docs/access?context=c_TableAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US).

    1.  Construct the endpoint using the Health and Safety User \[sn\_imt\_core\_health\_and\_safety\_user\] table.

        ```
        https://<your-instance>.servicenow.com/api/now/table/sn_imt_core_health_and_safety_user
        ```

    2.  Add a query parameter to query a specific user's email address.

        In the API explorer, you can enter one of the following strings in the **sysparm\_query** field to generate an endpoint that includes the correct query parameter:

        -   `user.email=<user-email-address>`: Queries the provided employee's email address.
        -   `visitor.email=<visitor-email-address>`: Queries the provided visitor's email address.
        ![Example sysparm_query value to query a specific user's email address.](../image/sysparm-query.png)

    This example cURL request queries the Health and Safety User table and returns records associated with Abel Tuter's email address.

    ```
    curl "http://<your-instance>.servicenow.com/api/now/table/sn_imt_core_health_and_safety_user?sysparm_query=user.email%3Dabel.tuter%40example.com&sysparm_limit=1" \
    --request GET \
    --header "Accept:application/json" \
    --user 'username':'password'
    ```


## Result

The Employee Health and Safety Status application returns the Health and Safety User record associated with the email address in the request. The JSON payload contains the following data.

```
{
  "result": [
    {
      "sys_mod_count": "0",
      "sys_updated_on": "2020-07-14 19:58:00",
      "sys_tags": "",
      "type": "employee",
      "sys_id": "33f184491bce9010e3730e16ec4bcb71",
      "sys_updated_by": "system.administrator",
      "manually_created": "true",
      "sys_created_on": "2020-07-14 19:58:00",
      "sys_domain": {
        "link": "https://<my-instance>.servicenow.com/api/now/table/sys_user_group/global",
        "value": "global"
      },
      "requirements_status": "cleared",
      "visitor": "",
      "user": {
        "link": "https://<my-instance>.servicenow.com/api/now/table/sys_user/62826bf03710200044e0bfc8bcbe5df1",
        "value": "62826bf03710200044e0bfc8bcbe5df1"
      },
      "sys_created_by": "system.administrator"
    }
  ]
}
```

All fields are internal, except for the following:

<table id="table_avk_r4p_3mb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

requirements\_status

</td><td>

Whether the visitor or employee has completed all requirements to return to the workplace. For more information, see [Create health and safety user records](create-readiness-user.md) and [Create a health and safety requirement](create-readiness-requirement.md).-   Cleared: The visitor or employee has completed all requirements to return to the workplace.
-   Not Cleared: The visitor or employee has not completed all requirements to return to the workplace.

 Data type: String

</td></tr><tr><td>

visitor

</td><td>

If present, this record represents a visitor instead of an employee. **Note:** Only used when returning visitor health data.

 Data type: Object

</td></tr><tr><td>

visitor.link

</td><td>

Link to the visitor record on the instance.**Note:** Only used when returning visitor health data.

 Data type: String

</td></tr><tr><td>

visitor.value

</td><td>

Sys\_id of the visitor record. **Note:** Only used when returning visitor health data.

 Data type: String

</td></tr><tr><td>

user

</td><td>

If present, this record represents an employee instead of a visitor.**Note:** Only used when returning employee health data.

 Data type: Object

</td></tr><tr><td>

user.link

</td><td>

Link to the user record on the instance.**Note:** Only used when returning employee health data.

 Data type: String

</td></tr><tr><td>

user.value

</td><td>

Sys\_id of the user record. **Note:** Only used when returning employee health data.

 Data type: String

</td></tr></tbody>
</table>