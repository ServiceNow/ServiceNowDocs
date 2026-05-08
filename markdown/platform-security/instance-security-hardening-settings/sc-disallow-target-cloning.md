---
title: Disallow target cloning \[New in Security Center 1.3\]
description: Configure the glide.db.clone.allow\_clone\_target property to prevent your instance from being used as a clone target.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuration, Hardening settings, Platform Security]
---

# Disallow target cloning \[New in Security Center 1.3\]

Configure the **glide.db.clone.allow\_clone\_target** property to prevent your instance from being used as a clone target.

Protect your instance from being used as a clone target by setting the **glide.db.clone.allow\_clone\_target** system property to **false**. A system clone copies everything in a database from a source instance to the target instance. This is a security risk because the instance database on the target instance is overwritten in the cloning process, leading to data loss and lack of data integrity.

Set the **glide.db.clone.allow\_clone\_target** system property to **false** on production instances to disallow your instance from being selected as a clone target.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.db.clone.allow\_clone\_target**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

false

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Configuration](sc-configuration.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.4
-   CVSS score: Medium
-   Security risk details: Not setting this property to the recommended value of false enables the instance to be used as a clone target. This is a security risk because the instance database can be overwritten in the cloning process.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

-   Instance Clone
-   Register target instance \(legacy\)

</td></tr><tr><td>

Functional impact

</td><td>

This property provides an additional safeguard which prevents a production instance from being cloned to. The default value is false for production instances and true for sub production instances such as dev or qa. To enable an instance to be used as a clone target set this property to true.

</td></tr></tbody>
</table>**Parent Topic:**[Configuration](sc-configuration.md)

