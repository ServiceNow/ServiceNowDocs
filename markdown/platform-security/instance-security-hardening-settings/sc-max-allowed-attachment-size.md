---
title: Maximum allowed attachment size \[Updated in Security Center 1.3\]
description: Configure the com.glide.attachment.max\_size property to control the maximum size \(in megabytes\) permitted for an uploaded attachment.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-03-20"
reading_time_minutes: 1
breadcrumb: [File and resources, Hardening settings, Platform Security]
---

# Maximum allowed attachment size \[Updated in Security Center 1.3\]

Configure the **com.glide.attachment.max\_size** property to control the maximum size \(in megabytes\) permitted for an uploaded attachment.

This property controls the maximum size \(in megabytes\) of an uploaded attachment. If this property is not set to the recommended value of **1024** \(1 gigabyte\) or less, the platform can accept large files that could fill up storage and lead to a Denial of Service \(DoS\) attack.

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

integer

</td></tr><tr><td>

Recommended value

</td><td>

1024

</td></tr><tr><td>

Default value

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
-   Security risk details: If this property is not set to **1024** \(1 gigabyte\) or less, the platform could accept large files which may lead to a DoS attack.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[Attachment limit properties](https://www.servicenow.com/docs/access?context=r_AttachmentLimitProperties&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

</td></tr></tbody>
</table>**Parent Topic:**[File and resources](sc-file-resources.md)

