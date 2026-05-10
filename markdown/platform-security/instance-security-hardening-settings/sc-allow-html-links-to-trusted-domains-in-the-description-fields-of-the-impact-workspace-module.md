---
title: Allow HTML Links to Trusted Domains in the Description Fields of the Impact Workspace Module \[New in Security Center 7.0\]
description: Use a system property to help sanitize the HTML allowed in the descriptions fields. This property limits the allowed links to only those from the trusted domains listed in the property.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Allow HTML Links to Trusted Domains in the Description Fields of the Impact Workspace Module \[New in Security Center 7.0\]

Use a system property to help sanitize the HTML allowed in the descriptions fields. This property limits the allowed links to only those from the trusted domains listed in the property.

**Note:** This hardening setting is not a part of the hardening baseline. It does not appear in Security Center hardening pages and affect your hardening score.

The Impact Workspace module allows HTML in a number of description-related fields. When configured, the **sn\_impact\_common.whitelisted.url\_HTML\_injection** system property contains a comma-separated list of domain names. Description fields for the Impact Workspace module are allowed to contain HREFs with URLs only from the domains listed in the property.

Ensure the **sn\_impact\_common.whitelisted.url\_HTML\_injection** system property is set to a comma-separated list of domain names that represent the domains allowed in HTTP reference URLs of description fields for the Impact Workspace module.

To disallow HREFs in these fields, set the property to an empty string. If the property doesn’t exist on the System Properties \[sys\_properties\] table, it defaults to this list: `servicenow.com, service-now.com, youtube.com, google.com, youtu.be, soti.net, dpdhl.sharepoint.com, documentation.avaya.com, www.juniper.net, servicenow.sharepoint.com, servicenow-my.sharepoint.com, scaledagileframework.com`.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**sn\_impact\_common.whitelisted.url\_HTML\_injection**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

String list

</td></tr><tr><td>

Recommended value

</td><td>

servicenow.com, service-now.com, youtube.com, google.com, youtu.be, soti.net, dpdhl.sharepoint.com, documentation.avaya.com, www.juniper.net, servicenow.sharepoint.com, servicenow-my.sharepoint.com, scaledagileframework.com

</td></tr><tr><td>

Default value

</td><td>

servicenow.com, service-now.com, youtube.com, google.com, youtu.be, soti.net, dpdhl.sharepoint.com, documentation.avaya.com, www.juniper.net, servicenow.sharepoint.com, servicenow-my.sharepoint.com, scaledagileframework.com

</td></tr><tr><td>

Fallback value

</td><td>

servicenow.com, service-now.com, youtube.com, google.com, youtu.be, soti.net, dpdhl.sharepoint.com, documentation.avaya.com, www.juniper.net, servicenow.sharepoint.com, servicenow-my.sharepoint.com, scaledagileframework.com

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.4
-   CVSS score: Medium
-   If an untrusted domain is added to the property, this opens these fields up to containing links to risky sources which can lead HTML injection attacks. The exact risk is dependent on the customer instance.

</td></tr><tr><td>

Functional impact

</td><td>

If the property is empty, no HREFs are allowed in the field text and all HREFs are removed. Any links using domains not listed in the property are removed. An improper value for this field could result in corrupted data for the affected fields.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

If the **sn\_impact\_common.blacklist\_tags\_HTML\_injection** system property contains HTML tags that surround HREF links, then all links within those tags will be removed.

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

