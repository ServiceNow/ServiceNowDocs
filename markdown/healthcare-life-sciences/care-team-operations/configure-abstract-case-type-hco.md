---
title: Configure the abstract case type for Healthcare Operations Core case types
description: Extend the Healthcare Operations case \[sn\_hco\_case\] to create custom case types for use with Healthcare Operations Core and related plugins by creating a child table from the Healthcare Operations Core case type.
locale: en-US
release: zurich
product: Care Team Operations
classification: care-team-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Configure the abstract case type for Healthcare Operations Core case types

Extend the Healthcare Operations case \[sn\_hco\_case\] to create custom case types for use with Healthcare Operations Core and related plugins by creating a child table from the Healthcare Operations Core case type.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Select **New**.

    ![](../image/abstract-case-hco.png)

3.  Set **Extends table** to Healthcare Operations Case \[sn\_hco\_case\].

4.  Fill in the other fields as needed.

    For information on these fields, see [Create a table](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/table-administration/task/t_CreateATable.html) in the ServiceNow platform documentation.

5.  Click **Submit**.

    **Note:**To add a field to the extended child tables, refer to the [Add and customize a field in a table](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/field-administration/task/t_CreatingNewFields.html) in the ServiceNow platform documentation.


