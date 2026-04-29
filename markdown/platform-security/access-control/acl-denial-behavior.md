---
title: Deny-Unless ACL
description: Learn details about Deny-Unless ACLs.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure an ACL rule, Access Control List Rules, Access Management]
---

# Deny-Unless ACL

Learn details about Deny-Unless ACLs.

Deny-Unless ACLs are evaluated with a "deny-unless" approach. The ACL defines the users that will NOT be denied. Said another way, the user will be denied access **unless** the role, condition, and script requirements are met.

**Important:** Deny-Unless ACLs will take priority against Allow-If ACLs in ACL Evaluation, as it will be evaluated first.

A Deny-Unless ACL produces two outcomes

<table id="table_jnn_5pl_zbc"><thead><tr><th>

Evaluation outcome

</th><th>

Result

</th></tr></thead><tbody><tr><td>

Pass

</td><td>

The defined roles, data conditions, security attributes, and script requirements are met. The ACL proceeds to further evaluation **Important:** Even if a Deny-Unless ACL matches, access is only granted when an Allow-If ACL explicitly permits it. If no Allow-If ACL is matched and the Deny-Unless ACL passes, the system grants access by default.

</td></tr><tr><td>

Fail

</td><td>

The Deny-Unless ACL is marked as failing and access will be denied.

</td></tr></tbody>
</table>The following is an explained example of a Deny-Unless ACL:

-   ACL has roles `sn_hr_core.manager` and `itil`
-   Condition has active = `true`
-   script has answer = `gs.isLoggedIn();`

The user is denied access unless all three requirements for this ACL are satisfied. In order for this Deny-Unless ACL to pass, a user needs either the `sn_hr_core.manager` or `itil` roles, be accessing a record that has active field = `true`, and be logged in. The Deny-Unless ACL will fail if any of the three requirements isn't met.

