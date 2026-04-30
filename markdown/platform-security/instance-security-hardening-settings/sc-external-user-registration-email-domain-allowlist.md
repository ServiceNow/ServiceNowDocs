---
title: Restrict email domains for external user registration \[Updated in Security Center 1.3, 1.5, and 2.0\]
description: Use the sn\_ext\_usr\_reg.allowed\_email\_domains property to list acceptable external email domains.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict email domains for external user registration \[Updated in Security Center 1.3, 1.5, and 2.0\]

Use the **sn\_ext\_usr\_reg.allowed\_email\_domains** property to list acceptable external email domains.

The **sn\_ext\_usr\_reg.allowed\_email\_domains** system property defines which email addresses are allowed to self-register to a ServiceNow instance. The format should be a comma separated list of acceptable email domains such as `domain1.com,domain2.com` where emails such as `example@domain2.com` will be accepted. If **sn\_ext\_usr\_reg.allowed\_email\_domains** is not set with a list of acceptable domains, then users with any email address are allowed to register accounts on the instances. If not defined, malicious actors could perform registration using emails addresses from unwanted domains to gain authenticated access to the instance.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**sn\_ext\_usr\_reg.allowed\_email\_domains**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\), Communities Properties

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Purpose

</td><td>

List email domains to allow user email for registration.

</td></tr><tr><td>

Recommended value

</td><td>

Enter a list of domains in a comma-separated format, for example `domain1.com, domain2.com, domain3.com`. This format works with or without spaces between elements.

</td></tr><tr><td>

Configuration type

</td><td>

String

</td></tr><tr><td>

Security risk

</td><td>

\(High\) Malicious actors could perform registration using emails addresses from unwanted domains. Ensure that **sn\_ext\_usr\_reg.allowed\_email\_domains** is not set to an empty value.

</td></tr><tr><td>

Functional impact

</td><td>

Email addresses from domains that are not included in the comma separated list defined in the property aren't allowed to self-register to a ServiceNow instance.

</td></tr><tr><td>

Security risk rating

</td><td>

7.5

</td></tr><tr><td>

References

</td><td>

[Communities](https://www.servicenow.com/docs/access?context=servicenow-communities&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Access control](sc-access-control.md)

