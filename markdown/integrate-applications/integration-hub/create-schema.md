---
title: Create schema
description: Create schema to create delimited files in your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Utility Actions Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Create schema

Create schema to create delimited files in your ServiceNow instance.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Utility Actions spoke.
-   Role required: sn\_utility\_spoke.utility\_actions\_admin.

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub Utilities** &gt; **File Builder** &gt; **File Schemas**.

2.  Click **New**.

3.  On the form, fill these values.

<table id="table_iwg_wt4_gmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Schema Name

</td><td>

Name to identify the schema record. For example, `Incident Schema`.

</td></tr><tr><td>

Delimiter

</td><td>

Delimiter in the file. For example, `,` and `\t`. The default value is value is comma.

</td></tr><tr><td>

Has Header

</td><td>

Option to specify if the schema has header.

</td></tr><tr><td>

Quoted

</td><td>

Option to escape the delimiters and surround all values with quotation marks.

</td></tr><tr><td>

Columns

</td><td>

Columns of the schema as a JSON array. For each column, specify column name and data type. For example, ```
[
    {
        "name" : "Number",
        "type" : "string"
    },
    {
        "name" : "Caller First Name",
        "type" : "string"
    },
    {
        "name" : "Caller Last Name",
        "type" : "string"
    },
    {
        "name" : "Short Description",
        "type" : "string"
    },
    {
        "name" : "State",
        "type" : "choice",
        "choices" : [
            {
                "label" : "New",
                "value" : "New"
            },
            {
                "label" : "In Progress",
                "value" : "In Progress"
            },
           {
                "label" : "On Hold",
                "value" : "On Hold"
            },
            {
                "label" : "Resolved",
                "value" : "resolved"
            },
            {
                "label" : "Closed",
                "value" : "closed"
            }
        ]
    },
    {
        "name" : "Active",
        "type" : "boolean"
    }
]
```

. For more information, see Create a data gathering action for a dynamic template.**Note:** Ensure that you surround the key and value with quotation marks.

</td></tr></tbody>
</table>4.  Click **Submit**.


