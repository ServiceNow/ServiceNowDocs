---
title: Request an exception using GRC: Policy and Compliance Management
description: Request policy exceptions using the GRC policy exception management capability in the Policy and Compliance Management application from within Vulnerability Response.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Configure Exception Management for Security Exposure Management, Implement, Unified Security Exposure Management, Security Operations]
---

# Request an exception using GRC: Policy and Compliance Management

Request policy exceptions using the GRC policy exception management capability in the Policy and Compliance Management application from within Vulnerability Response.

## Before you begin

Before you can use the Policy Exception Integration to request policy exceptions, you must download the GRC: Policy and Compliance Management application from the ServiceNow Store.

Role required: sn\_vul.remediation\_owner

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management** &gt; **findings** \(or **Remediation Tasks**\)&gt;**All**, and open the item or group for which you want to request an exception.

    The selected item or group must be in Open, Under investigation, or Awaiting implementation state.

2.  On the selected form, click **Request Exception**.

3.  On the form, fill in the fields.

<table id="table_stm_xty_flb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Policy

</td><td>

Vulnerability Management policy that you are requesting an exception for.

</td></tr><tr><td>

Control objective

</td><td>

Control objectives that are associated with the policy you selected. If a policy is not selected, all the control objectives are listed.

</td></tr><tr><td>

Valid from

</td><td>

Date when the exception will start. The default value is the current date. This date cannot be in the past.

</td></tr><tr><td>

Valid until

</td><td>

Date that the policy exception expires and the state of the vulnerable item or group changes from Deferred to Open.**Note:** The number of days that the policy exception is valid cannot exceed the **Maximum exception duration \(days\)** that you set for the policy in Policy and Compliance. For more information, see [Create a policy](https://www.servicenow.com/docs/bundle/zurich-governance-risk-compliance/page/product/grc-policy-and-compliance/task/t_DefineAPolicy.html).

</td></tr><tr><td>

Reason

</td><td>

Reason for requesting an exception.

</td></tr><tr><td>

Justification

</td><td>

Details that are related to the reason why this request is being made. This mandatory field must be filled in by the remediation owner.

</td></tr></tbody>
</table>4.  Click **Submit**.

    For more information on the Policy Exception Integration and the hand-off between the remediation owner and the compliance manager, see [Policy and Compliance optional setup](https://www.servicenow.com/docs/bundle/zurich-governance-risk-compliance/page/product/grc-policy-compliance-implementation/concept/policy-compliance-optional-steps.html).


**Parent Topic:**[Configure Exception Management for Security Exposure Management](sem-configure-exp-mngmt-vr.md)

