---
title: Minimize Allowed Attachment Size
description: Configure the com.glide.attachment.max\_size property to control the maximum size \(in megabytes\) permitted for an uploaded attachment.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [File and resources, Hardening settings, Platform Security]
---

# Minimize Allowed Attachment Size

Configure the **com.glide.attachment.max\_size** property to control the maximum size \(in megabytes\) permitted for an uploaded attachment.

The **com.glide.attachment.max\_size** system property controls the maximum size of uploaded attachment in megabytes. If the value of property **com.glide.attachment.max\_size** is 1024 then the max allowed attachment size is 1Gb.

**Note:** A real attachment size is calculated through multiplication 1024 \* value of the **com.glide.attachment.max\_size** property.

Ensure that the property **com.glide.attachment.max\_size** is set to `1024` or less.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.attachment.max\_size**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Integer

</td></tr><tr><td>

Recommended value

</td><td>

An integer less than or equal to 1024

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

1024

</td></tr><tr><td>

Category

</td><td>

[File and resources](sc-file-resources.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.5
-   CVSS score: Medium
-   Security risk details: The platform can accept large files that could fill up storage or cause a denial of service.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[Attachment limit properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AttachmentLimitProperties.md)

</td></tr></tbody>
</table>**Parent Topic:**[File and resources](sc-file-resources.md)

