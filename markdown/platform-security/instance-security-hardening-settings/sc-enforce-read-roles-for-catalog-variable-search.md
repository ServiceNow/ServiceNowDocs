---
title: Enforce Read Roles for Catalog Variable Search \[New in Security Center 7.0\]
description: Use system properties to ensure that only catalog variables with an empty read role are indexed for search.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce Read Roles for Catalog Variable Search \[New in Security Center 7.0\]

Use system properties to ensure that only catalog variables with an empty read role are indexed for search.

When the property **glide.ais.ingestion.ignore\_catalog\_variables\_read\_roles** is set to the recommended value of **false**, only catalog variables with an empty read role are indexed for search. If this property is set to **true** then all variables are indexed for search regardless of any read roles specified on the variable.

Verify that the **glide.ais.ingestion.ignore\_catalog\_variables\_read\_roles** system property does not exist in the System Properties \[sys\_properties\] table, or exists and is set to **false**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.ais.ingestion.ignore\_catalog\_variables\_read\_roles**

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

false

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Functional impact

</td><td>

This property affects the indexing of searchable content from catalog variables that require specific roles for read access.

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 2.6
-   CVSS score: Low
-   Security risk details: Users will be able to search for variables that they do not have read roles to access to causing information disclosure.

</td></tr><tr><td>

Dependencies

</td><td>

None

</td></tr><tr><td>

References

</td><td>

Service catalog variables

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

