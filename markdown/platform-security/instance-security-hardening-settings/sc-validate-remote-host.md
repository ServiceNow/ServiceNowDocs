---
title: Validate remote host
description: Set the property to true to prevent bad actors from using internal port scanning in your network.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Business Logic, Hardening settings, Platform Security]
---

# Validate remote host

Set the property to true to prevent bad actors from using internal port scanning in your network.

If the **glide.update\_set.remote.check\_host** property is not set to the recommended value of **true**, then the  remote instance test feature will allow internal port scanning which is a method bad actors can use to discover vulnerabilities in a network. It is then possible to enumerate all open ports on a given host, and in some cases pull response data which could lead to information leakage or unauthorized data access.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.update\_set.remote.check\_host**

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

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Business Logic](sc-business-logic.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.3
-   CVSS score: Medium
-   Security risk details: Not setting property to the recommended value of **true** could enable bad actors to use internal port scanning to gain access to unauthorized data.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB0755132](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0755132)

 [Define a remote instance](https://www.servicenow.com/docs/access?context=t_DefineARemoteInstance&version=zurich&pubname=zurich-application-development&ft:locale=en-US)

</td></tr></tbody>
</table>**Parent Topic:**[Business Logic](sc-business-logic.md)

