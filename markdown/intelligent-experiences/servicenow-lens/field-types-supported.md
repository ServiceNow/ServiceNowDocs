---
title: Field types supported
description: Learn about the field types that are currently supported with the ServiceNow AI Lens application.
locale: en-US
release: australia
product: ServiceNow Lens
classification: servicenow-lens
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, ServiceNow AI Lens, Enable AI experiences]
---

# Field types supported

Learn about the field types that are currently supported with the ServiceNow AI Lens application.

The following field types are currently supported with ServiceNow AI Lens:

-   name
-   due\_date
-   float
-   glide\_time
-   glide\_utc\_time
-   html
-   journal
-   journals\_input
-   longint
-   password
-   password2
-   simple\_name\_values
-   table\_name
-   translated\_html
-   translated\_text
-   boolean
-   choice
-   decimal
-   email
-   glide\_date
-   glide\_duration
-   insert\_timestamp
-   integer
-   ip\_addr
-   percent\_complete
-   phone\_number\_e164
-   price
-   script
-   script\_plain
-   string
-   string\_full\_utf8
-   url
-   reference
-   glide\_list

For more information about these fields, see [Field types reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_FieldTypes.md).

<table id="table_psc_fs3_mfc"><thead><tr><th>

Field

</th><th>

Formatting description

</th></tr></thead><tbody><tr><td>

glide\_date

</td><td>

-   Priority 1 - For a glide\_date field type on any record, ServiceNow AI Lens uses the format specified in the date\_format field on a user’s record of a user running the Lens session.
-   Priority 2 - If no date\_format is specified during user record creation or later, Lens uses the format specified in the system property `glide.sys.date_format`.
-   Priority 3 - If the system property is not available, the default format `YYYY-MM-DD` is used.

</td></tr><tr><td>

glide\_time

</td><td>

-   Priority 1 - For a glide\_time field type on any record, ServiceNow AI Lens uses the format specified in the time\_format field on a user’s record of a user running the Lens session.
-   Priority 2 - If no time\_format is specified during user record creation or later, Lens uses the format specified in the system property `glide.sys.time_format`.
-   Priority 3 - If the system property is not available, the default format `HH:mm:ss` is used.

</td></tr><tr><td>

glide\_utc\_time

</td><td>

The value is populated in the `HH:mm:ss` format.

</td></tr><tr><td>

glide\_duration

</td><td>

Duration is populated in the `D HH:mm:ss` format. For example, the duration of 1 day, 2 hours, 30 minutes is populated as 1 02:30:00.

</td></tr><tr><td>

due\_date

</td><td>

The value is populated using the formats of glide\_date and glide\_time, concatenated with a space.

</td></tr><tr><td>

table\_name

</td><td>

The value is only populated when the exact internal name of table is identified.

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow AI Lens reference](servicenow-lens-reference.md)

