---
title: Query records
description: Retrieves multiple records from a specified table.
locale: en-US
release: australia
product: ServiceNow CLI
classification: servicenow-cli
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Perform record operations using ServiceNow CLI, ServiceNow CLI, Building low-code applications, Developing your application, Building applications]
---

# Query records

Retrieves multiple records from a specified table.

## Before you begin

Role required: sn\_cli\_metadata.cli\_admin, sn\_cli\_metadata.cli\_user, or admin

## Procedure

1.  Open your system's command-line tool and execute this command.

    ```
    $ snc record query [--displayvalue displayValue --fields fields --limit limit --offset offset --query query --table table]
    ```

    Pass in values for these arguments.

    |Parameter|Description|
    |---------|-----------|
    |displayValue|Include `--displayvalue` to retrieve the display value from the database for reference and choice fields. Do not include this parameter to retrieve the actual values.|
    |fields|Comma-separated list of field names to return from the database.|
    |limit|Maximum number of records to return.|
    |offset|Starting record index for which to begin retrieving records. Use this value to paginate record retrieval.|
    |query|Required. Encoded query used to filter the result set in the following format: `--query '<column_name><operator><value>'`.|
    |table|Required. Name of the table in which to query the records.|


## Example

```
$ snc record query --displayvalue --fields short_description,state --query '123TEXTQUERY321=email' --table incident
```

The CLI returns any records that match the query.

```
{
   "result": [
      {
         "short_description": "Unable to connect to email",
         "state": "Closed"
      }
   ]
}
```

**Parent Topic:**[Perform record operations using ServiceNow CLI](manage-records.md)

