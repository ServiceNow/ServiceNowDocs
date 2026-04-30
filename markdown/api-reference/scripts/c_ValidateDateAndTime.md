---
title: Validation script use case - Date and time
description: To validate the input of all date/time fields, you can use the following in a validation script \( System Definition Validation Scripts \).
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-02-06"
reading_time_minutes: 1
breadcrumb: [Useful scripts, Scripting, API implementation, API implementation and reference]
---

# Validation script use case - Date and time

To validate the input of all date/time fields, you can use the following in a validation script \(**System Definition** &gt; **Validation Scripts**\).

Because the date/time format is hard-coded in this script, it must match your instance's date/time format. If your instance's date/time format changes, you must update your validation script.

Set the validation script's type to "`glide_date_time`". Then, with this validation script, if a user enters an incorrect format in a date/time field, they will receive an error message.

```
function validate (value){ 
 if (!value) {
    return true;
 }

 return (getDateFromFormat(value, 'yyyy-MM-dd HH:mm:ss') != 0);
}
```

For a comprehensive use case, see [Restricting record access](c_ExScptDftBfrQryBsnRu.md).

**Parent Topic:**[Useful scripts](usefulScripts.md)

