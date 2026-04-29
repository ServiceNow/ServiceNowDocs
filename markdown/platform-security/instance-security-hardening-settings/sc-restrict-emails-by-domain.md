---
title: Disable creating users from incoming emails
description: Use the glide.user.trusted\_domain property to specify the comma-separated list of trusted domains used in the creation of users from incoming emails.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Disable creating users from incoming emails

Use the **glide.user.trusted\_domain** property to specify the comma-separated list of trusted domains used in the creation of users from incoming emails.

An administrator can set the **glide.pop3readerjob.create\_caller** system property to automatically create users from incoming emails. If set this property to the insecure value, the instance automatically creates users from incoming email. Each user created will have the same hardcoded default password which makes bypassing authentication through brute force easier.

Ensure that the **glide.pop3readerjob.create\_caller** system property is set to **false**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.pop3readerjob.create\_caller**

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

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.4
-   CVSS rating: Medium
-   Security risk details: Allowing automatic user creation without strong password controls undermines authentication security and increases the likelihood of system compromise.

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

**Parent Topic:**[Authentication](sc-authentication.md)

