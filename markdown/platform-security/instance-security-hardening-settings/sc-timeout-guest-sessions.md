---
title: Timeout guest sessions
description: Use a system property to control the inactive session timeout for unauthenticated users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-timeout-guest-sessions.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Business Logic, Hardening settings, Platform Security]
---

# Timeout guest sessions

Use a system property to control the inactive session timeout for unauthenticated users.

The **glide.guest.session\_timeout** property controls the inactive session timeout for unauthenticated \(guest\) users, specified in minutes. New instances are provisioned with a default of 5 minutes. If the property does not exist in the sys\_properties table, the effective value defaults to 0. When set to 0, the guest-specific override is disabled and the session instead uses the general UI session timeout \(**glide.ui.session\_timeout**\).

Setting the **glide.guest.session\_timeout** property greater than 30 minutes increases the number of sessions persisted by the instance, which may cause minor availability concerns.

To configure this property:

-   Navigate to `/sys_properties_list.do` on the instance.
-   Ensure the **glide.guest.session\_timeout** property exists and is set to a value greater than 0 and less than or equal to 30 minutes.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.guest.session\_timeout**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Integer \(in minutes\)

</td></tr><tr><td>

Recommended value

</td><td>

30

</td></tr><tr><td>

Default value

</td><td>

5

</td></tr><tr><td>

Fallback value

</td><td>

0

</td></tr><tr><td>

Category

</td><td>

[Business Logic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-business-logic.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score:4.3
-   CVSS score: Medium
-   Security risk details: Setting the **glide.guest.session\_timeout** property greater than 30 minutes increases the number of sessions persisted by the instance, which may cause minor availability concerns.

</td></tr><tr><td>

Functional Impact

</td><td>

Guest sessions that remain idle longer than the configured timeout are ended, and any session-scoped state is lost. The guest user must start a new session to continue. Small timeout values can result in an undesirable user experience as sessions expire too rapidly. If there are availability concerns from persisting too many sessions in memory, the **glide.guest.session\_timeout** property can be lowered to 5.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

The **glide.guest.session\_timeout** property interacts with the **glide.ui.session\_timeout** property. When **glide.guest.session\_timeout** is set to 0, guest sessions do not receive an independent idle timeout — they fall back to using **glide.ui.session\_timeout** instead.

</td></tr></tbody>
</table>**Parent Topic:**[Business Logic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-business-logic.md)

