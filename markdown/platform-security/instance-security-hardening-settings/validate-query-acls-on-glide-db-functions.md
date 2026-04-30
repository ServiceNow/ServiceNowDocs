---
title: Validate query ACLs on Glide DB functions \[New in Security Center 7.0\]
description: Control whether query ACLs are applied to Glide DB functions using system properties.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Validate query ACLs on Glide DB functions \[New in Security Center 7.0\]

Control whether query ACLs are applied to Glide DB functions using system properties.

When the **glide.db.encoded\_query.check\_function\_field\_query\_acls** system property is set to **true**, query ACLs \(query\_range and query\_match\) are validated by default on these Glide DB functions:

-   glidefunction:position
-   glidefunction:substring
-   glidefunction:concat
-   glidefunction:coalesce
-   glidefunction:length

To validate these query ACLS on additional functions, add those functions to the **glide.db.encoded\_query.force\_query\_range\_on\_functions** system property.

Set the **glide.db.encoded\_query.check\_function\_field\_query\_acls** system property to **true**, or confirm that the property isn’t on the System Properties \[sys\_properties\] list.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

-   **glide.db.encoded\_query.check\_function\_field\_query\_acls**
-   **glide.db.encoded\_query.force\_query\_range\_on\_functions**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

-   Boolean
-   String list

</td></tr><tr><td>

Recommended value

</td><td>

-   true
-   glidefunction:position, glidefunction:substring, glidefunction:concat, glidefunction:coalesce, glidefunction:length

</td></tr><tr><td>

Default value

</td><td>

-   true
-   glidefunction:position, glidefunction:substring, glidefunction:concat, glidefunction:coalesce, glidefunction:length

</td></tr><tr><td>

Fallback value

</td><td>

-   true
-   glidefunction:position, glidefunction:substring, glidefunction:concat, glidefunction:coalesce, glidefunction:length

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score:5.3
-   CVSS score: Medium
-   If the **glide.db.encoded\_query.check\_function\_field\_query\_acls** system property exists and isn’t set to a value of **true**, a logged-in user may be able to infer data blindly, leading to sensitive information disclosure.


</td></tr><tr><td>

Functional impact

</td><td>

Users may expect to see values from function fields but get blocked due to ACLs enforced on the function fields.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Access control](sc-access-control.md)

