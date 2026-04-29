---
title: Name-value pairs field type
description: You can access the values stored in a name-value pairs field in scripts using the name.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Name-value pairs field type

You can access the values stored in a name-value pairs field in scripts using the name.

## Sample script

The following example demonstrates how to add mappings to a name-value pairs field, and how to query existing values using the name.

```
// Script example demonstrating setting and getting values
var gr = new GlideRecord('u_nv_table');
gr.initialize();

gr.nv_field.name1 = "value1"; //add a name-value Pair mapping with the name "name1" and value "value1"
gr.nv_field.name2 = "value2"; //add another name-value Pair mapping with the name "name2" and value "value2"

// Access by dot notation
gs.print("name1 = " + gr.nv_field.name1); // Expected output: name1 = value1

// Iterate over each property and print name and value
for(var name in gr.nv_field) {
    gs.print(name + " = " + gr.nv_field[name]);
}

gs.print(gr.nv_field); // Expected output: {"name1":"value1","name2":"value2"}
```

