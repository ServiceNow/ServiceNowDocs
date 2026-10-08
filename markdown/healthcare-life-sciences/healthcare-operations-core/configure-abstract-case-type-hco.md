---
title: Configure the abstract case type for Healthcare Operations Core case types
description: Extend the Healthcare Operations case \[sn\_hco\_case\] to create custom case types for use with Healthcare Operations Core and related plugins by creating a child table from the Healthcare Operations Core case type.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/healthcare-life-sciences/healthcare-operations-core/configure-abstract-case-type-hco.html
release: zurich
product: Healthcare Operations Core
classification: healthcare-operations-core
topic_type: task
last_updated: "2026-03-12"
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

    \[Omitted image "abstract-case-hco.png"\] Alt text: Healthcare operations case in search menu.

3.  Set **Extends table** to Healthcare Operations Case \[sn\_hco\_case\].

4.  Fill in the other fields as needed.

    For information on these fields, see Create a table in the ServiceNow platform documentation.

5.  Click **Submit**.

    **Note:**To add a field to the extended child tables, refer to the Add and customize a field in a table in the ServiceNow platform documentation.


