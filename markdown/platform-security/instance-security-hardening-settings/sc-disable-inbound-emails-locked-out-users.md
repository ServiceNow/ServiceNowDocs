---
title: Disable inbound emails for locked out users
description: Use the glide.pop3.process\_locked\_out property to control inbound email actions for locked out, active users.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Disable inbound emails for locked out users

Use the **glide.pop3.process\_locked\_out** property to control inbound email actions for locked out, active users.

The **glide.pop3.process\_locked\_out** system property controls inbound email actions for locked out users. If **glide.pop3.process\_locked\_out** is set to **true**, there may be an information disclosure as inbound emails would be received by users with locked accounts.

Ensure that the property **glide.pop3.process\_locked\_out** is set to **false**.

**Note:** Consider the security implications of allowing users from untrusted domains, and why they were locked out, before allowing emails from them to trigger inbound email actions.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.pop3.process\_locked\_out**

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

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.5
-   CVSS rating: High
-   Security risk details: Allows locked-out users to continue submitting inbound emails that may create records or trigger workflows, posing a security risk by enabling potentially unauthorized actions.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Access control](sc-access-control.md)

