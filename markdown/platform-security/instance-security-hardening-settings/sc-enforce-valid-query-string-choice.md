---
title: Enforce valid query string choice \[New in Security Center 7.0\]
description: Use a system property to ensure that any choice field value, when passed via a URL query string, is a valid active choice when a record is created.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Enforce valid query string choice \[New in Security Center 7.0\]

Use a system property to ensure that any choice field value, when passed via a URL query string, is a valid active choice when a record is created.

When the **glide.ui.query\_string.enforce\_valid\_choice\_on\_create** system property is set to **true**, the platform validates that any choice field value passed via a URL query string \(for example, from a list filter\) is a valid active choice when the record is created.

If invalid, the value is ignored and the field falls back to its default value. When the property is **false**, validation is inactive, and the system accepts any value, even invalid or inactive ones. This acceptance can potentially result in incorrect or unexpected data being stored on records.

Ensure **glide.ui.query\_string.enforce\_valid\_choice\_on\_create** exists in the System Properties \[sys\_properties\] table and is set to **true**. If the property doesn’t exist in the table, the fallback value is **false**.

## More information

<table><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.ui.query\_string.enforce\_valid\_choice\_on\_create**

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

Fallback value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 2.2
-   CVSS score: Low
-   Security Risk: Set this property to **true** to ensure that only valid choices are used for new record creation. Invalid choices may lead to minor and unexpected data integrity issues, where a user is able to select an unintended value.

</td></tr><tr><td>

Functional impact

</td><td>

Existing instances and workflows may rely on new records being created based on a filter that contains an invalid or inactive choice. Use the following process to observe this behavior:

 1.  Log in to an instance as an admin user.
2.  Create a String field on any table. For example, an incident with 2 choices: **Test1** and **Test2**.
3.  Create a list filter on incident table selecting the string field with value set to **Test2**.
4.  Go to dictionary field and deactivate the choice **Test2**.
5.  Go to the filter selected in step 3 and select **New** button.
6.  Check the value of the String type field in the newly opened record. When the property is set to **true**, the string field shouldn’t have a value or should show the default value.

 When the property is set to **false** \(default\), the string field has the value set to **Test2**.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see Add a system property.

**Parent Topic:**[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

