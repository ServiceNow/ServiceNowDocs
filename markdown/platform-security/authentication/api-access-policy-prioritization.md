---
title: API access policy prioritization
description: Learn about the policy prioritization logic if there are multiple API access policy configured for your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/api-access-policy-prioritization.html
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create REST API access policy, REST API access policies, API access policy, Authentication, Access Management]
---

# API access policy prioritization

Learn about the policy prioritization logic if there are multiple API access policy configured for your ServiceNow® instance.

API access policies are prioritized based on the type of REST API policy set on your ServiceNow® instance.

The approach is defining different weights for each part of the API such as,method, resource, and version.

The API policy is prioritized for non-global first, then global. In other words, a non-global access policy will always override a global API access policy.

Prioritization logic are as follows:

<table id="table_cb3_5nh_bwb"><thead><tr><th>

Fields

</th><th>

Priority

</th><th>

Prioritization Logic

</th></tr></thead><tbody><tr><td>

Method, resource, and version

</td><td>

1

</td><td>

If the 3 fields matches with the policy then that policy takes the 1st priority.

</td></tr><tr><td>

Method+ resource

</td><td>

2

</td><td>

If the 2 fields matches with the policy then that policy takes the 1st priority.

</td></tr><tr><td>

Resource + version

</td><td>

3

</td><td>

If the 2 fields along with the field **Apply to all methods** matches with the policy then that policy takes the 3rd priority.

</td></tr><tr><td>

Resource

</td><td>

4

</td><td>

If the field along with the field **Apply to all methods** matches with the policy then that policy takes the 4th priority.

</td></tr><tr><td>

Method + version

</td><td>

5

</td><td>

If the 2 fields along with the field **Apply to all resources** matches with the policy then that policy takes the 5th priority.

</td></tr><tr><td>

Method

</td><td>

6

</td><td>

If the field along with the field **Apply to all resources** matches with the policy then that policy takes the 5th priority.

</td></tr><tr><td>

Version

</td><td>

7

</td><td>

If the field along with the fields **Apply to all methods** and **Apply to all versions** matches with the policy then that policy takes the 7th priority.

</td></tr><tr><td>

Global but not Apply to all methods

</td><td>

8

</td><td>

If the fields **Global** is `true` and **Apply to all methods** is `false` then that policy takes the 8th priority.

</td></tr><tr><td>

Global and Apply to all methods

</td><td>

9

</td><td>

If the fields **Global** is `true` and **Apply to all methods** is `true` then that policy takes the 9th priority.

</td></tr></tbody>
</table>