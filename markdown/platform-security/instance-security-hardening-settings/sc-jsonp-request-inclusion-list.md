---
title: Restrict JSONP requests to trusted URLs \[Updated in Security Center 1.3\]
description: Specify trusted URLs for the AngularJS $http service to allow or reject JSONP requests.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict JSONP requests to trusted URLs \[Updated in Security Center 1.3\]

Specify trusted URLs for the AngularJS $http service to allow or reject JSONP requests.

The **angular.jsonp.inclusion\_list.enabled** property specifies trusted URLs for the angularJS $http service to allow and or reject JSONP requests. This property is necessary because this is a potentially breaking change for customers, so they need a way to add their trusted URLs. If this property is not set to the recommended value of true, then JSONP requests are allowed to any URL.

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

boolean

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

