---
title: Variables to collect data for record producer fields
description: Use variables to collect data for record producer fields.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Variables to collect data for record producer fields

Use variables to collect data for record producer fields.

You can use the following variable types to collect data for the corresponding record producer fields.

|Field type|Recommended variable type|
|----------|-------------------------|
|True/False|Yes/No|
|Reference|Reference|
|Date or Due Date|Date|
|Date/Time|Date/Time|
|Choice or any field with an associated choice list|Select Box|
|Email address|Email|
|URL|URL|
|HTML|HTML|
|List or UI Action List|List Collector|
|String with length greater than 256|Multi-Line Text|
|String, Integer, Decimal, Floating Point Number|Single-Line Text|
|File Attachment|Attachment|
|All other field types|Multi-Line Text|

**Note:**

-   If the record producer variable is mapped to an encrypted field of another table, then this variable value is not stored in Question Answer \[question\_answer\] table. So, it is also not available in the variable editor of the target record.
-   If the record producer variable is masked and encrypted, and also mapped to an encrypted field of another table:
    -   The variable value is not stored in Question Answer \[question\_answer\] table.
    -   The decrypted value of the variable is copied to the encrypted field of the target record.

## Values Returned

When you construct a record producer, be aware of the return value.

Most of these field types return a string. However, there are some exceptions. For example, a **Reference** value returns the `sys_id` of the target object, and a **List** value returns a comma-separated list of `sys_ids`.

Example 1: For a **List** value, return an array which can be iterated to retrieve the individual values submitted by your user:

```
var sys_id_string  = producer.glide_list_field;
var sys_id_list = sys_id_string.split(',');
```

Example 2: For a **Date** or **Date/Time** value, return a date which GlideDate can evaluate.

```
var glideDateTime  = new GlideDateTime(producer.date_field);
```

**Parent Topic:**[Service Catalog Reference](../concept/service-catalog-reference.md)

