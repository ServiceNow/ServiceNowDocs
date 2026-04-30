---
title: Datatype ACL
description: The datatype ACL enables you to write ACL rules that apply to all fields of a specific type.
locale: en-US
release: zurich
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ACL rule types, Explore Access Control Lists, Access Control List Rules, Access Management]
---

# Datatype ACL

The datatype ACL enables you to write ACL rules that apply to all fields of a specific type.

Datatype ACLs provide a targetted approach to access controls by restricting table fields based on data type. This allows for broader security constraints than wildcard\(\*\) ACLs. The syntax for datatype ACLs follows the format \*.\[`(field to be restricted)`\].

Conventional field ACLs are limited to specific table-field identifiers, all fields in a table, or all tables with a specific field name, in contrast the datatype ACLs enable you to apply security uniformly across fields that share certain metadata. This helps prevent creating additional ACLs to apply security uniformly across all fields.

When implementing datatype ACLs, its essential to validate all affected fields before and after adding them to avoid unexpected security issues. See [Create a datatype ACL](../task/create-a-datatype-acl.md) to create your own datatype ACL.

To review existing datatype ACLs navigate to **All** &gt; **System Security** &gt; **Access Controls** and use the **Name** field to search for ACLs that start with `*.[`.

**Note:** Scripting Governance uses datatype ACLs by default for scripting restrictions, see \_ for more details.

