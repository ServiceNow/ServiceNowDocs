---
title: Enforce field ACLs for inbound query requests
description: Manage how incoming queries are validated on your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-enforce-field-acls-for-inbound-query-requests.html
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-05-26"
reading_time_minutes: 1
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Enforce field ACLs for inbound query requests

Manage how incoming queries are validated on your instance.

Use the **glide.export.query.enforce\_field\_acl** property to control whether field-level ACLs are enforced on the fields referenced in an inbound query requests. When set to **true**, field ACLs are checked against fields used in the incoming query, and the query is rejected if the user is unauthorized to access those fields. When set to **false**, field ACLs are not checked on query conditions, and the query executes regardless of field-level access restrictions.

This property applies only to field ACL enforcement on query conditions. Setting this property to **false** does not affect whether users can read field values they are not otherwise authorized to view. Field-level read ACLs remain enforced regardless of this setting.

Set the property **glide.export.query.enforce\_field\_acl** to **true**.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.export.query.enforce\_field\_acl**

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

true

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Architecture, design, and threat modeling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-architecture-design-threat-molding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.4
-   CVSS score: Medium
-   Security risk details: This can result in information disclosure to unauthorized parties.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Architecture, design, and threat modeling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-architecture-design-threat-molding.md)

