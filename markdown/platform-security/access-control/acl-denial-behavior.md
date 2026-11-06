---
title: Deny-Unless ACL
description: A Deny-Unless ACL grants access only when a user meets all defined role, condition, and script requirements. If any requirement is unmet, access is denied.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/access-control/acl-denial-behavior.html
release: australia
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2026-10-27"
reading_time_minutes: 1
breadcrumb: [Configure an ACL, Access Control Lists \(ACLs\), Access Management]
---

# Deny-Unless ACL

A Deny-Unless ACL grants access only when a user meets all defined role, condition, and script requirements. If any requirement is unmet, access is denied.

Deny-Unless ACLs are evaluated with a "deny-unless" approach. The ACL defines the users that aren't denied. Said another way, the user is denied access unless the role, condition, and script requirements are met.

**Warning:** Deny-Unless ACLs take priority over Allow-If ACLs in ACL evaluation and are evaluated first.

A Deny-Unless ACL produces two outcomes.

<table id="table_jnn_5pl_zbc"><thead><tr><th>

Evaluation outcome

</th><th>

Result

</th></tr></thead><tbody><tr><td>

Pass

</td><td>

The defined roles, data conditions, security attributes, and script requirements are met. The ACL proceeds to further evaluation. **Warning:** Even if a Deny-Unless ACL matches, access is only granted when an Allow-If ACL explicitly permits it. If no Allow-If ACL is matched and the Deny-Unless ACL passes, the system grants access by default.

</td></tr><tr><td>

Fail

</td><td>

The Deny-Unless ACL is marked as failing and access will be denied.

</td></tr></tbody>
</table>The following is an example of a Deny-Unless ACL:

-   ACL has roles `sn_hr_core.manager` or `itil`
-   Condition has active = `true`
-   script has answer = `gs.isLoggedIn();`

The user is denied access unless all three requirements for this ACL are satisfied. For this Deny-Unless ACL to pass, a user must have the sn\_hr\_core.manager or itil role, be accessing an active record, and be logged in. The Deny-Unless ACL fails if any of the three requirements is not met.

If there are multiple Deny-Unless ACLs on a specific resource, none of them must deny access during evaluation.

