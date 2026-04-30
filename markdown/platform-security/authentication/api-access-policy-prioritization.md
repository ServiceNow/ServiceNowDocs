---
title: API access policy prioritization
description: Learn about the policy prioritization logic if there are multiple API access policy configured for your ServiceNow instance.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create REST API access policy, REST API access policies, API access policy, Authentication, Access Management]
---

# API access policy prioritization

Learn about the policy prioritization logic if there are multiple API access policy configured for your ServiceNow® instance.

API access policies are prioritized based on the type of REST API policy set on your ServiceNow® instance.

The approach is defining different weights for each part of the API such as,method, resource, and version.

The API policy is prioritized for non-global first, then global. In other words, a non-global access policy will always override a global API access policy.

Prioritization logic are as follows:

|Fields|Priority|Prioritization Logic|
|------|--------|--------------------|
|Method, resource, and version|1|If the 3 fields matches with the policy then that policy takes the 1st priority.|
|Method+ resource|2|If the 2 fields matches with the policy then that policy takes the 1st priority.|
|Resource + version|3|If the 2 fields along with the field **Apply to all methods** matches with the policy then that policy takes the 3rd priority.|
|Resource|4|If the field along with the field **Apply to all methods** matches with the policy then that policy takes the 4th priority.|
|Method + version|5|If the 2 fields along with the field **Apply to all resources** matches with the policy then that policy takes the 5th priority.|
|Method|6|If the field along with the field **Apply to all resources** matches with the policy then that policy takes the 5th priority.|
|Version|7|If the field along with the fields **Apply to all methods** and **Apply to all versions** matches with the policy then that policy takes the 7th priority.|
|Global and Apply to all methods|8|If the fields **Global** is `true` and **Apply to all methods** is `false` then that policy takes the 8th priority.|
|Global and Apply to all methods|9|If the fields **Global** is `true` and **Apply to all methods** is `true` then that policy takes the 9th priority.|

