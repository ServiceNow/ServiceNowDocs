---
title: Restrict access to specific IP ranges plugin \[Updated in Security Center 1.3\]
description: Use the com.snc.ipauthenticator plugin to restrict access to specific IP ranges. Unless public access is intended for the instance, administrators should limit access to their assigned IP net blocks.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict access to specific IP ranges plugin \[Updated in Security Center 1.3\]

Use the **com.snc.ipauthenticator** plugin to restrict access to specific IP ranges. Unless public access is intended for the instance, administrators should limit access to their assigned IP net blocks.

## Prerequisites

This plugin when set to true restricts access to specific IP ranges. Unless public access is intended for the instance, administrators should limit access to their assigned IP net blocks. An exclusion list \(Deny\) or an inclusion list \(Allow\) of IP addresses can be created through IP Address Access Control \(ip\_access\_list.do\).

Before setting this property, you must activate the IP Range Based Authentication \(com.snc.ipauthenticator\)**com.snc.ipauthenticator** plugin. To learn more, see [IP range based authentication](../../login/concept/c_IPRangeBasedAuthentication.md) and in the Steps to configure section \(below\).

Ensure the plugin **com.snc.ipauthenticator** is activated and there is at least one active IP access policy in the table ip\_access.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Plugin Name

</td><td>

-   com.snc.ipauthenticator
-   ip\_access

</td></tr><tr><td>

Configuration type

</td><td>

System Security &gt; IP Address Access Control

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Purpose

</td><td>

To add the range of IP address that can or can't access the instance to the trusted and untrusted domain lists.

</td></tr><tr><td>

Recommended value

</td><td>

Active

</td></tr><tr><td>

Default value

</td><td>

None. This is a plugin, not a Glide property; therefore, there is no default value.

</td></tr><tr><td>

Security risk rating

</td><td>

5.3

</td></tr><tr><td>

Functional Impact

</td><td>

Customer-denied IP ranges are used for this remediation item. No impact as customer defines the target list.

</td></tr><tr><td>

Security risk

</td><td>

\(Low\) Unnecessary exposure to the target instance on the internet should be restricted with the help of IP access controls functionality.

</td></tr><tr><td>

References

</td><td>

[IP range based authentication](../../login/concept/c_IPRangeBasedAuthentication.md)

</td></tr></tbody>
</table>## Steps to configure

1.  Ensure that the com.snc.ipauthenticator plugin is active.
2.  Navigate to **System Security** &gt; **IP Address Access Control**.
3.  Click **New** to create an exclusion list \(Deny\) or an inclusion list \(Allow\) of IP addresses.
4.  Click **Submit**.

**Parent Topic:**[Access control](sc-access-control.md)

