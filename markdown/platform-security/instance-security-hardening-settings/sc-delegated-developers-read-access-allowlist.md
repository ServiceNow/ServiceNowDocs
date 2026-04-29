---
title: Restrict delegated developers read access \[Updated in Security Center 1.3\]
description: If com.glide.dd\_allow\_global\_access\_tables does not contain the recommended value of wf\_activity, wf\_activity\_definition, wf\_workflow, wf\_workflow\_version, sp\_portal, sp\_widget, and sp\_page, then those tables could be read by a delegated developer. This could provide the delegated developer read access to sensitive information.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict delegated developers read access \[Updated in Security Center 1.3\]

If **com.glide.dd\_allow\_global\_access\_tables** does not contain the recommended value of wf\_activity, wf\_activity\_definition, wf\_workflow, wf\_workflow\_version, sp\_portal, sp\_widget, and sp\_page, then those tables could be read by a delegated developer. This could provide the delegated developer read access to sensitive information.

## More information

<table><tbody><tr><td>

Attribute

</td><td>

Description

</td></tr><tr><td>

Property name

</td><td>

**com.glide.dd\_allow\_global\_access\_tables**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

string

</td></tr><tr><td>

Recommended value

</td><td>

wf\_activity, wf\_activity\_definition, wf\_workflow, wf\_workflow\_version, sp\_portal, sp\_widget, sp\_page

</td></tr><tr><td>

Default value

</td><td>

wf\_activity, wf\_activity\_definition, wf\_workflow, wf\_workflow\_version, sp\_portal, sp\_widget, sp\_page

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 2.7
-   CVSS score: Low
-   Security risk details: Ensure that **com.glide.dd\_allow\_global\_access\_tables** is set to wf\_activity, wf\_activity\_definition, wf\_workflow, wf\_workflow\_version, sp\_portal, sp\_widget, sp\_page.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

