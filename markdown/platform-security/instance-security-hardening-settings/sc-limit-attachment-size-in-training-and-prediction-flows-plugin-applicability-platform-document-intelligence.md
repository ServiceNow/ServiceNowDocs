---
title: Limit attachment size in training and prediction flows \[New in Security Center 1.3 and updated in 1.5\]
description: The glide.platform\_ml\_di.max\_attachment\_size property controls the maximum allowed size limit for returning attachments in training and prediction flows.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [File and resources, Hardening settings, Platform Security]
---

# Limit attachment size in training and prediction flows \[New in Security Center 1.3 and updated in 1.5\]

The **glide.platform\_ml\_di.max\_attachment\_size** property controls the maximum allowed size limit for returning attachments in training and prediction flows.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.platform\_ml\_di.max\_attachment\_size**

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

4,000,000

</td></tr><tr><td>

Default value

</td><td>

4,000,000

</td></tr><tr><td>

Category

</td><td>

[File and resources](sc-file-resources.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.3
-   CVSS score: Medium
-   Security risk details: If **glide.platform\_ml\_di.max\_attachment\_size** is not set to the recommended value of 4,000,000 or less, then returning large files could cause a denial of service \(DoS\) attack.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[File and resources](sc-file-resources.md)

