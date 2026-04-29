---
title: Disable legacy JQuery UI usage
description: Avoid the introduction of unpatched vulnerabilities in the library by disabling legacy JQuery UI usage.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuration, Hardening settings, Platform Security]
---

# Disable legacy JQuery UI usage

Avoid the introduction of unpatched vulnerabilities in the library by disabling legacy JQuery UI usage.

Prevent the use of older prepatched JQuery UI versions, which introduce unpatched vulnerabilities in the library. Using old versions can potentially lead to security risks arising from attacks on vulnerabilities discovered in outdated JQuery UI library versions.

Confirm that the **glide.jquery\_ui.legacy** system property is set to **false** to prevent older prepatched JQuery UI versions from being used. This system property is a failsafe in case organizations depend on the non-patched versions to run their custom implementations.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.jquery\_ui.legacy**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

String

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

[Configuration](sc-configuration.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.9
-   CVSS score: Low
-   Preventing older prepatched JQuery UI versions from being used can introduce unpatched vulnerabilities in the library.

</td></tr><tr><td>

Functional impact

</td><td>

This system property is a failsafe in case organizations depend on the non-patched versions to run their custom implementations.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Configuration](sc-configuration.md)

