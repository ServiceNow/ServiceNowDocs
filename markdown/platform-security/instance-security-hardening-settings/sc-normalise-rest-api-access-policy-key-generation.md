---
title: Normalise REST API access policy key generation
description: The glide.rest.policy.normalize\_apply\_all\_fields property controls how the platform builds lookup keys for REST API access policies when wildcard flags are set.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-normalise-rest-api-access-policy-key-generation.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [REST API access policy, policy normalization, access policy key generation, glide.rest.policy.normalize\_apply\_all\_fields]
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Normalise REST API access policy key generation

The **glide.rest.policy.normalize\_apply\_all\_fields** property controls how the platform builds lookup keys for REST API access policies when wildcard flags are set.

REST API endpoints on the platform can be protected by access policies. Each policy defines a scope by specifying which API path, HTTP method, and API version it covers. For each dimension, you can select either an exact value or an apply to all wildcard flag. When a request arrives, the platform builds a lookup key from the request attributes and searches a cache of active policies for a match.

This property controls a normalization step in the key-building process. A policy record can be in an inconsistent state where the **apply to all flag** for a dimension is set to `true`, but a specific value is also stored in the same record. This is a legacy data condition.

Without normalization enabled, the platform builds the lookup key using the specific value, even though the flag indicates all values should match. This causes the policy to only match requests with that exact value. With normalization enabled, when the **apply to all flag** is set, the specific value is discarded before the lookup key is built. This verifies the policy matches the full scope it declares.

<table id="table_9iu_9jk_2ik"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.rest.policy.normalize\_apply\_all\_fields**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \( `/sys_properties_list.do`\)

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

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[API and web service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-api-web-service.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.5
-   CVSS rating: Medium
-   Security risk details:

Access policies on this platform are authorization controls. They determine which authentication requirements apply to which API endpoints. A policy misconfiguration caused by the inconsistent data results in a policy that is registered as active but silently never matches incoming requests outside its stale specific value.

An administrator may believe a policy is enforcing an authentication requirement across all HTTP methods, all API versions, or all resources. But requests outside the stale specific value bypass the policy entirely. The attack surface is any API call that should have been governed by such a policy.


</td></tr><tr><td>

Functional impact

</td><td>

Setting this property to `true` changes how the policy lookup cache is populated at startup and after policy record change.

 Policies with the inconsistent data condition will have their effective scope corrected: they match all requests within the "apply to all" dimension. They no longer match only the stale specific value.

 Policies without the inconsistent data condition are unaffected. The cache is automatically invalidated when the property is toggled. The change takes effect without a restart.

 Enabling this property widens the enforcement scope of affected policies. This is the intended behavior. Before production rollout, verify that existing policy configurations see no unintended authentication requirements changes.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[API and web service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-api-web-service.md)

