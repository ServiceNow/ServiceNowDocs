---
title: Require Authentication on Event Management HTTP Processor \[New in Security Center 1.3, Updated in 1.5, and removed in 2.0\]
description: Learn how to establish secure basic authentication for inbound Amazon Simple Notification Service \(SNS\) requests when the Event Management plugin \(com.glideapp.itom.snac\) is enabled.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Require Authentication on Event Management HTTP Processor \[New in Security Center 1.3, Updated in 1.5, and removed in 2.0\]

Learn how to establish secure basic authentication for inbound Amazon Simple Notification Service \(SNS\) requests when the Event Management plugin \(**com.glideapp.itom.snac**\) is enabled.

If the **glide.basicauth.required.evtmgmthttpprocessor** property isn’t set to the recommended value of **true**, and the Event Management plugin \(**com.glideapp.itom.snac**\) is active, then basic authentication is not required for all inbound Amazon Simple Notification Service \(SNS\) requests. This can lead to unauthenticated access to instance data.

To remediate this security risk, ensure that **glide.basicauth.required.evtmgmthttpprocessor** is set to**true** and that **com.glideapp.itom.snac** is active.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.basicauth.required.evtmgmthttpprocessor**

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

[API and web service](sc-api-web-service.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7
-   CVSS score: High
-   Security risk details: Not setting**glide.basicauth.required.evtmgmthttpprocessor** to the recommended value of true, and not activating the **com.glideapp.itom.snac** plugin causes basic authentication not to be enabled for inbound SNS requests. This could lead to unauthenticated access to instance data.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

-   [https://docs.aws.amazon.com/sns/latest/dg/welcome.html](https://docs.aws.amazon.com/sns/latest/dg/welcome.html)
-   [Access control](https://www.servicenow.com/docs/access?context=access-control&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)

</td></tr><tr><td>

Functional impact

</td><td>

If **glide.basicauth.required.evtmgmthttpprocessor** is not set to the recommended value of True, and if the Event Management plugin \(com.glideapp.itom.snac\) is active, then basic authentication is not required for all Inbound Amazon Web Services SNS requests. This can lead to unauthenticated access to instance data.

</td></tr></tbody>
</table>**Parent Topic:**[API and web service](sc-api-web-service.md)

