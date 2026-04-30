---
title: Dictionary entry data types
description: You can only change a dictionary entry's data type when the change does not result in data loss. Use the following guidelines to change a dictionary entry's data type.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# Dictionary entry data types

You can only change a dictionary entry's data type when the change does not result in data loss. Use the following guidelines to change a dictionary entry's data type.

|Condition|Restrictions|
|---------|------------|
|The field is empty in all table records.|None. You can convert an empty field from any data type to another without restriction.|
|The table contains existing data for the field.|You can only convert between logical data types that map to the same physical data type in the database. For example, you can convert a glide duration to a glide datetime since both logical data types map to the DATETIME physical data type in the database.|
|The field is a string field you are converting to another type of string field.|You can change between string-based data types as long as length changes do not cause any data loss from truncation. For example, you can change from a MEDIUM database type to a VARCHAR\(100\) database type if none of the existing data is greater than 100.|
|The field is a string field you are converting to a globally unique ID \(GUID\).|You can only convert a string field to a GUID if all of the exiting data in the field are already **Sys ID** values.|
|The field is a GUID field you are converting to a string field.|None. You can convert a GUID field to a string field without restriction.|

