---
title: Restrict JSONP Requests to Trusted URLs \[Updated in Security Center 1.3\]
description: Specify trusted URLs for the AngularJS $http service to allow or reject JSONP requests.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict JSONP Requests to Trusted URLs \[Updated in Security Center 1.3\]

Specify trusted URLs for the AngularJS $http service to allow or reject JSONP requests.

Increase security on your instance by ensuring that only trusted URLs for the AngularJS $http service can allow/reject JSONP requests. JSONP requests are allowed to any URL if these properties are not configured and enabled.

Use the value of the **angular.jsonp.inclusion\_list.urls** system property to define a list of URLs that are trusted and allow for this purpose. Set the value of the **angular.jsonp.inclusion\_list.enabled** system property to **true** to limit allowed JSONP to only the URLs listed in **angular.jsonp.inclusion\_list.urls**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**angular.jsonp.inclusion\_list.enabled**

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

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: Medium
-   CVSS score: 5.4
-   Security risk details: Setting this property to **false** enables JSONP requests to any URL.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

