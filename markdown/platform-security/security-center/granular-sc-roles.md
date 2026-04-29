---
title: Granular roles for Security Center
description: Use the new Security Center admin role to grant users security center administrative capability without using the admin role.
locale: en-US
release: australia
product: Security Center
classification: security-center
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Center, Platform Security]
---

# Granular roles for Security Center

Use the new Security Center admin role to grant users security center administrative capability without using the admin role.

Beginning with the Security Center 3.2 update available in the ServiceNow Store, the Security Center Admin \(sn\_vsc.security\_center\_admin\) role is available. This role allows users to manage Security Center configurations and access controls while enhancing security through least-privileged access.

<table id="table_g14_xjy_2hc"><thead><tr><th>

Granular Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_vsc.security\_center\_admin

</td><td>

Provides admin level access to Security Center consoles and tools. Users with this role can also create and manage security tasks.

This role contains the following roles:-   mi\_admin
-   access\_analyzer\_admin
-   pa\_admin
-   scan\_user data\_classification\_auditor
-   sn\_ace.ace\_user
-   antivirus\_viewer
-   sn\_vsc.task\_manager
-   sn\_mif.mif\_read
-   sn\_cicd.sys\_ci\_automation

</td></tr></tbody>
</table>**Parent Topic:**[Security Center](../../security-center/concept/sec-center-v2.md)

