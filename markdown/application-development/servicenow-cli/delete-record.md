---
title: Delete a record
description: Deletes the specified record from the specified table.
locale: en-US
release: xanadu
product: ServiceNow CLI
classification: servicenow-cli
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Perform record operations using ServiceNow CLI, ServiceNow CLI, Building low-code applications, Developing your application, Building applications]
---

# Delete a record

Deletes the specified record from the specified table.

## Before you begin

Role required: sn\_cli\_metadata.cli\_admin, sn\_cli\_metadata.cli\_user, or admin

## Procedure

1.  Open your system's command-line tool and execute this command.

    ```
    $ snc record delete [--table table --sysid sys_id]
    ```

    Pass in values for these arguments.

    |Parameter|Description|
    |---------|-----------|
    |table|Required. Name of the table in which to delete the record.|
    |sysid|Required. Sys\_id of the record to delete.|


## Example

```
$ snc record delete --table incident --sysid 552c48888c033300964f4932b03eb092
```

**Parent Topic:**[Perform record operations using ServiceNow CLI](manage-records.md)

