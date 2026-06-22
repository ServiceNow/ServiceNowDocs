---
title: Disable creating users from incoming emails \[Updated in Securty Center 1.3\]
description: Use the glide.user.trusted\_domain property to specify the comma-separated list of trusted domains used in the creation of users from incoming emails.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/instance-security-hardening-settings/sc-restrict-emails-by-domain.html
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Disable creating users from incoming emails \[Updated in Securty Center 1.3\]

Use the **glide.user.trusted\_domain** property to specify the comma-separated list of trusted domains used in the creation of users from incoming emails.

An administrator can set an email property to automatically create users from incoming emails. If set this property to the insecure value, the instance will automatically create users from incoming email. Each user created will have the same hard coded default password which makes bypassing authentication through brute force easier.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.pop3readerjob.create\_caller**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-authentication.md)

</td></tr><tr><td>

Recommended value

</td><td>

false

</td></tr><tr><td>

Default value

</td><td>

false

</td></tr><tr><td>

Security risk rating

</td><td>

5.4

</td></tr><tr><td>

Functional impact

</td><td>

Once this property is configured, the instance only accepts emails from trusted domains. If you do not include the domain in the trusted list, there is an impact to guest users because accounts are created automatically.

</td></tr><tr><td>

Security risk

</td><td>

\(Moderate\) If the property is not enabled, an attacker might use an email spoofing/spamming campaign to send multiple emails resulting in the creation of more unnecessary guest users.

</td></tr><tr><td>

References

</td><td>

[Inbound mail configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/r_InboundMailConfiguration.md)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/t_AddAPropertyUsingSysPropsList.md).

**Parent Topic:**[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-authentication.md)

