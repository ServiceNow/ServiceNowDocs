---
title: Exclude Sensitive Tables and Fields from Data Generation \[New in Security Center 7.0\]
description: Use system properties to exclude tables and fields from Data Generation, which is used to generate fake data sets based on existing data. Tables and fields that are added to these exclusion lists can't be used for Data Generation feature.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Exclude Sensitive Tables and Fields from Data Generation \[New in Security Center 7.0\]

Use system properties to exclude tables and fields from Data Generation, which is used to generate fake data sets based on existing data. Tables and fields that are added to these exclusion lists can't be used for Data Generation feature.

Tables included in the **glide.data.generation.excluded.tables** system property are excluded from Data Generation in addition to metadata tables.

Fields included in a comma separated list for **glide.data.generation.excluded.fields.&lt;TABLE-NAME&gt;** are excluded from Data Generation in addition to any of these fields, if applicable:

-   number
-   roles
-   sys\_class\_name
-   sys\_created\_by
-   sys\_id
-   sys\_mod\_count
-   sys\_tags
-   sys\_updated\_by

Review the list of tables included in the property **glide.data.generation.excluded.tables**. Add any tables which should be excluded from Data Generation to the comma separated list of tables. In addition, metadata tables will be ignored for data generation.

Review the list of fields for each table by looking at properties with the format: `glide.data.generation.excluded.fields.<TABLE-NAME>`. Add any sensitive fields for the specified table as a comma-separated list of values.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

-   **glide.data.generation.excluded.tables**
-   **glide.data.generation.excluded.fields.\***

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

-   Comma-separated list of table names
-   Comma-separated list of fields for a given table

</td></tr><tr><td>

Recommended value

</td><td>

-   Comma-separated list of table names which should be excluded from Data Generation
-   Comma-separated list of field names which should be excluded from Data Generation for each applicable table

</td></tr><tr><td>

Default value

</td><td>

"",""

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 2.6
-   CVSS score: Low
-   Security risk details: Data in tables used in the Data Generation feature can have real or fake values populated as intended by the feature. Sensitive values in tables which should not be visible or replicated could be revealed to other instance users.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

Data Generation plugin is in use

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

