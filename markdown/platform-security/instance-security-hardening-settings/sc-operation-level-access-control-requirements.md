---
title: Disable raw database query execution \[Updated in Security Center 1.3 and removed in 2.0\]
description: Control whether a user can perform raw SQL queries on the database.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Disable raw database query execution \[Updated in Security Center 1.3 and removed in 2.0\]

Control whether a user can perform raw SQL queries on the database.

The **glide.db.allow\_unsafe\_dbi\_execute\_sql** property enables users to perform raw SQL queries on the database, which can give access to tables and data outside of GlideRecord restrictions. If this property is not set to the recommended value of **false**, this allows for the calling of **dbi.executeStatement\(\)** from a Glide Scriptable which can lead to malicious SQL statements being executed.

**Warning:** This property is both safe and no db override.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.db.allow\_unsafe\_dbi\_execute\_sql**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

boolean

</td></tr><tr><td>

Recommended value

</td><td>

false

</td></tr><tr><td>

Default value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.2
-   CVSS score: High
-   Security risk details: Not setting this property to **false** enables calling of **dbi.executeStatement\(\)** from a Glide Scriptable.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[Access Control List Rules](../../contextual-security/concept/access-control-rules.md)

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

