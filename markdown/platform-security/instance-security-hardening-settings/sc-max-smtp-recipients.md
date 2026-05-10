---
title: Minimize SMTP Recipient Quantity
description: The glide.email.smtp.max\_recipients specifies the maximum number of recipients the instance can list in the To: line for a single email notification.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Business Logic, Hardening settings, Platform Security]
---

# Minimize SMTP Recipient Quantity

The **glide.email.smtp.max\_recipients** specifies the maximum number of recipients the instance can list in the **To:** line for a single email notification.

The **glide.email.smtp.max\_recipients** system property specifies the maximum number of recipients the instance can list in the To: line for a single email notification. Notifications that would exceed this limit instead create duplicate email notifications addressed to a subset of the recipient list. Each email notification has the same maximum number of recipients.

Ensure that the property **glide.email.smtp.max\_recipients** is set to `100` or less.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.email.smtp.max\_recipients**

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

An integer less than or equal to 100

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

100

</td></tr><tr><td>

Category

</td><td>

[Business Logic](sc-business-logic.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.9
-   CVSS rating: Medium
-   Security risk details: This can lead to resource exhaustion and potentially cause a Denial of Service \(DoS\) condition on the email subsystem or the instance itself. Limiting recipient counts is essential to prevent abuse and maintain system performance and availability.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

**Parent Topic:**[Business Logic](sc-business-logic.md)

