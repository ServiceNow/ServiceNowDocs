---
title: IP range based authentication
description: One way to secure a web-based application is to restrict access based on the IP address.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Authentication, Access Management]
---

# IP range based authentication

One way to secure a web-based application is to restrict access based on the IP address.

You can block access to a specific address or range of addresses that you suspect belong to malicious individuals. The instance allows you to control access by IP address.

**Note:** Use the Adaptive Authentication \(AA\) pre-authentication context policy to enforce IP based authentications and restrictions for additional capabilities. For more information, see [Adaptive authentication](../../../integrate/authentication/concept/adaptive-authentication.md).

Notes and Limitations:

-   The system won't let you lock yourself out, so if you try to add a rule such that your current address would be locked out, the system warns you and refuses your insert.
-   If you're inside of a corporate intranet, be very careful about setting up your IP rules. The IP address you see on your own computer \(like 10.10.10.25\) generally bears no relationship to the IP address you will actually appear as out on the internet. Your company likely proxies and/or NATs your address into a predictable set of outbound addresses which you will likely need to ask your network team about.
-   A user whose access is restricted based on an access rule gets a 403 error on their browser.
-   Restricted users do not use transactions, semaphores, or count towards any server resource counts.
-   This feature does not supersede or override your existing access control rules if, for example, you're running a VPN to our data center. It's an additional check that must be met in addition to any access controls we may have set up on your PIX.
-   Allow rules always supersede deny rules. So if an address is both allowed \(by one rule\) and denied \(by a second rule\) it is, in fact, allowed.
-   Asterisks and CIDR blocks are not currently supported.
-   Regarding forwarded proxy addresses, the allow rules are applied to each address in the chain and then the deny rules are applied to each address in the chain if none of the allow rules matched.
-   IP range based authentication can effect the transfer of update sets. If IP address access control is enabled on the source instance, add the IP addresses of all application nodes supporting your instance as exceptions.

    **Note:** To find your instance IP information, Log in to [ServiceNow - NOW Support](https://support.servicenow.com/now), and Search for the **My IP Information** service catalog item.


**Note:** To learn more about the **com.snc.ipauthenticator** and **glide.ip.authenticate.strict** properties, which restrict instance access to specific IP ranges, see the following topics in Instance Security Hardening Settings:

[Restrict access to specific IP ranges plugin](../../security-center/reference/sc-restrict-access-to-specific-ip-ranges-plugin.md)

