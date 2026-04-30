---
title: Restrict access to emails with empty target table
description: Activate the glide.email.email\_with\_no\_target\_visible\_to\_all property to restrict user access to emails, unless they were the one who sent the email or have an admin role.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-02-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict access to emails with empty target table

Activate the **glide.email.email\_with\_no\_target\_visible\_to\_all** property to restrict user access to emails, unless they were the one who sent the email or have an admin role.

Unauthorized users are able to access emails in the sys\_email\_list table that are missing a target record. Instead of enforcing ACLs on email entries, this property restricts access only to the email sender and users with the admin role.

**Note:** Emails sent to and received by the instance appear in the sys\_email\_list table. However, only received emails that were marked with an Error and Ignored state should have an empty target table.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.email.email\_with\_no\_target\_visible\_to\_all**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Configure

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Purpose

</td><td>

To block email client from showing emails when user doesn't authorize access.

</td></tr><tr><td>

Recommended value

</td><td>

false

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Security risk rating

</td><td>

6.5

</td></tr><tr><td>

Functional impact

</td><td>

Users are no longer able to see emails where target table is empty unless they are an admin or were the sender of the email.

</td></tr><tr><td>

Security risk

</td><td>

\(Moderate\) If the property is not enabled, unauthorized users are able to access any email where the target\_table field is empty.

</td></tr><tr><td>

References

</td><td>

[Advanced email properties](https://www.servicenow.com/docs/access?context=r_AdditionalProperties&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

 [https://support.servicenow.com/kb\_view.do?sysparm\_article=KB0690043](https://support.servicenow.com/kb_view.do?sysparm_article=KB0690043)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Access control](sc-access-control.md)

