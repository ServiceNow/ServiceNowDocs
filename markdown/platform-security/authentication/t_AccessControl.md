---
title: IP Address Access Control
description: Apply an IP access control to outbound traffic, inbound traffic, or bidirectional traffic. The system only blocks an IP address if a matching Deny rule exists and no matching Allow rule exists. By default, there are no restrictions on access to your instance.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [IP range based authentication, Authentication, Access Management]
---

# IP Address Access Control

Apply an IP access control to outbound traffic, inbound traffic, or bidirectional traffic. The system only blocks an IP address if a matching Deny rule exists and no matching Allow rule exists. By default, there are no restrictions on access to your instance.

## Before you begin

**Note:** Use the Adaptive Authentication \(AA\) pre-authentication context policy to enforce IP based authentications and restrictions for additional capabilities. For more information, see [Adaptive authentication](../../../integrate/authentication/concept/adaptive-authentication.md).

Role required: admin

**Warning:** IP Address Control is configured only for external IPs and it will not block internal IP addresses from ServiceNow.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **IP Address Access Control** to see a list of your IP access controls.

    You might have to activate the IP Range Based Authentication \[com.snc.ipauthenticator\] plugin.

2.  Complete the form.

    **Note:** To find your instance IP information, Log in to [ServiceNow - NOW Support](https://support.servicenow.com/now), and Search for the **My IP Information** service catalog item.

<table id="table_mym_412_hlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Type of access control rule to include.

 -   Allow: Any IP address in this range can interact with this instance.
-   Deny: Any IP address in this range cannot interact with this instance unless it is listed in an Allow rule. Also, when adding deny rules, you cannot deny your own public IP address or your instance does not update a deny rule.
 **Note:** To support maintenance, upgrades, and Customer Service and Support, some ServiceNow internal IPs cannot be blocked by Deny rules.

</td></tr><tr><td>

Direction

</td><td>

Direction of the IP access control rule.-   **Inbound**: Choose Inbound to allow or deny inbound transactions. These are transactions initiated from outside of your instance.
-   **Outbound**: Choose Outbound to allow or deny outbound transactions. These are transactions initiated from within your instance.
-   **Bidirectional**: Choose Bidirectional for the configuration to apply for both Inbound and Outbound.


</td></tr><tr><td>

Active

</td><td>

When selected, the form is active.

</td></tr><tr><td>

Description

</td><td>

Description of the access control.

</td></tr><tr><td>

Range Start

</td><td>

Starting range of IP addresses to allow or deny. **Note:** These rules also affect transferring update sets. To ensure that IP address access control does not cause update sets to fail, add the target instance as an exception.

</td></tr><tr><td>

Range End

</td><td>

Ending range of IP addresses to allow or deny.**Note:** To limit access to specific VPN addresses only, enter a Deny range of **0.0.0.0** through **255.255.255.255** into the **Deny** field, and only enter the specific allowed VPN ranges.

</td></tr></tbody>
</table>3.  Click **Submit**.


